# Lab report Week 2/3

This lab report will detail the process I took in creating a web server and using the Junit debugging program.

### **Part 1: Writing a web server**

I have written a web server called StringServer that supports features like adding a string message and removing a message on a web page. 

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
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

In this first screen shot, I add the message "How are you" to the webpage. 

<img width="577" alt="Screenshot 2023-01-30 at 1 02 32 AM" src="https://user-images.githubusercontent.com/122568668/215434642-2db03c3d-2c3b-49b5-b2da-fb870300662f.png">

This calls the StringServer and Handler classes, and the handleRequest method. Inside we see that the path contains `/add-message` so the program then takes the string in `paramteres[1]` and appends it to the StringBuilder that is initialized. 



