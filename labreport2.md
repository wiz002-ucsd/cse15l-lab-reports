# Lab report Week 2/3

This lab report will detail the process I took in creating a web server and using the Junit debugging program.

### **Part 1: Writing a web server**

I have written a web server called StringServer that supports features like adding a string message and removing a message on a web page. 

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    
    StringBuilder message = new StringBuilder();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return message.toString();
        
        } 
        else if (url.getPath().equals("/clear")) {
            message = new StringBuilder();
            return String.format("Message cleared!");
        }
        else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    message.append(parameters[1] + "\n");
                    return String.format(message.toString());
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
In order for me to add a message on each new line I decided to use a stringBuilder that appends a new string + a "\n". 

**Screen shot #1**

In this first screen shot, I add the message "How are you" to the webpage by typing in `localhost:4000/add-message?s=How are you`.

<img width="577" alt="Screenshot 2023-01-30 at 1 02 32 AM" src="https://user-images.githubusercontent.com/122568668/215434642-2db03c3d-2c3b-49b5-b2da-fb870300662f.png">

This calls the StringServer and Handler classes, and the handleRequest method. Inside we see that the path contains `/add-message` so the program then takes the string in `paramteres[1]` and appends it to the empty StringBuilder `message`. In this case I also use the stringBuilder's `append()` method and `toString()` method. 

**Screen shot #2**

In the second sreen shot, I added "Hello" onto a new line on the webpage by typing in `localhost:4000/add-message?s=Hello`. 

<img width="476" alt="Screenshot 2023-01-30 at 1 02 50 AM" src="https://user-images.githubusercontent.com/122568668/215589917-d8357300-43e4-4f93-b0f5-ec525ba4f4b4.png">

This takes the `message` stringBuilder and appends Hello onto it along with a new line. 

I have also included a `/clear` function that clears the webpage. In this case, a new stringBuilder object will be created which message will then point to. 

<img width="480" alt="Screenshot 2023-01-30 at 1 03 00 AM" src="https://user-images.githubusercontent.com/122568668/215591470-01992127-b45c-489f-9215-dcb5e5740d9d.png">

### **Part 2: Choose one of the bugs from lab 3**

```
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
For this code if we input an array with only one element, there is no error. 
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
 ```
However, if we input an array with more than one element, the array is not reversed properly. 
```
@Test
  public void testReverseInPlace2() {
    int[] test = {1,2,3,4};
    ArrayExamples.reverseInPlace(test);
    assertArrayEquals(new int[]{4,3,2,1}, test);
  }
```
<img width="569" alt="Screenshot 2023-01-30 at 1 19 07 PM" src="https://user-images.githubusercontent.com/122568668/215597499-ae4374a8-e02f-4820-937a-541ac5bfa2b4.png">

As shown in the screenshot, we expected 2, but got 3 at element 2. 
This is because the elements are not getting reversed properly. After the elements in the first half are reversed, the elements in the latter half will remain the same.

The bug lies in the for loop:

```
for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
```
To fix this we need to include a holder that remembers the element that is replaced, then the holder will replace the corresponding element on the other end of the array.

```
for(int i = 0; i < arr.length/2; i += 1) {

      int holder = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = holder;

    }
```
In this implementation, the element at `i` and `arr.length-i-1` will be swapped seemingly simultaneously. We will have a holder that will remember one of the elements while it is being replaced. This for loop also only needs to loop for arr.length/2. If it loops for arr.length, the elements will just be swapped back to its original positions. 

### **Part 3: Something new**

To me, everything in this lab was new. I have used JUnit before, but this my first time writing my own test. I learnt how to use assertEquals and assertArrayEquals to make tests in JUnit. This lab also taught me how to identify bugs using these tests, and the thought process needed to debug. 

I've also learnt how to write code for a webpage and link it to a webserver. The overall process is still slightly unclear to me, but I do understand how to write code such that the URL path of this webserver has certain functions. 






