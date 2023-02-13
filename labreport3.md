# Lab report Week 4/5

In this lab report we will explore different uses and command-line options for the `grep` command. 

### **Option -l: Prints file names only**

If we want to find a file that contains a certain word or phrase, we can use the `-l` option. 

Information about `-l` was found on the [tutorials point website](https://www.tutorialspoint.com/how-to-invert-a-grep-expression-on-linux). 

#### **Example 1**

<img width="416" alt="Screenshot 2023-02-12 at 8 01 20 PM" src="https://user-images.githubusercontent.com/122568668/218367546-be965d9f-e649-4d85-8d97-665ea600daeb.png">

These would be all the files that contain the word "Athens". 

#### **Example 2**

<img width="414" alt="Screenshot 2023-02-12 at 8 02 38 PM" src="https://user-images.githubusercontent.com/122568668/218367676-74ce30c0-e361-49e0-a5df-d26f1c862886.png">

This shows all files that contain the word "Fast".

This is especially helpful if you are looking to find information on something, this option will allow you to single out the documents that contain the information you need. 

### **Option -i: ignore uppercase vs lowercase**

Sometimes you want to look for where a certain word is used, regardless of wether it has been capatilized or not.

Information about `-i` was found on the [tutorials point website](https://www.tutorialspoint.com/how-to-invert-a-grep-expression-on-linux). 

#### **Example 1**

<img width="535" alt="Screenshot 2023-02-12 at 7 54 04 PM" src="https://user-images.githubusercontent.com/122568668/218366700-bb29c546-e5ca-4c4f-9b7b-fe626ebe6ee9.png">
This displays all the files with the word "Hello", but if it appears as "hello", or "HELLO", then we wouldn't be able to detect it. 

<img width="559" alt="Screenshot 2023-02-12 at 7 55 45 PM" src="https://user-images.githubusercontent.com/122568668/218366887-07daeaee-804e-425c-a9c6-6164d74a5910.png">
Using this allows us to detect more files in which this word is used. 

#### **Example 2**

Here we can find all of the lines in which "democracy" was used regardless of whether it was capitalized or not. 

<img width="1205" alt="Screenshot 2023-02-13 at 1 33 43 PM" src="https://user-images.githubusercontent.com/122568668/218579496-b67166dc-d515-463f-9c4e-164020fa071c.png">

`-i` is useful if we do not know whether the word we want to search is capatilized or not, so dislaying every use of this word would be helpful. 

### **Option -v: inverts match**

If we want to display all the files that do not have the pattern we are searching for, we can use `-v`. 

Information about `-v` was found on the [tutorials point website](https://www.tutorialspoint.com/how-to-invert-a-grep-expression-on-linux). 

#### **Example 1**

<img width="645" alt="Screenshot 2023-02-13 at 1 15 02 PM" src="https://user-images.githubusercontent.com/122568668/218576112-cdecbb67-9165-44f9-b09a-78da226062e4.png">
Here we search for all the files that do not contain the keyword "Alliance". This can be helpful if we want to isolate information. 

#### **Example 2**

<img width="723" alt="Screenshot 2023-02-13 at 1 22 51 PM" src="https://user-images.githubusercontent.com/122568668/218577488-50a7674d-32c5-4678-90ed-eee23fc9e540.png">
Here we search for all the lines within this file that does not contain the word "the". This could be helpful if we want to only see headlines without the word "the". 


### **Option -n: Precede each matching line with a line number**

Information about `-n` was found on the [tutorials point website](https://www.tutorialspoint.com/how-to-invert-a-grep-expression-on-linux). 

Here we searched the Berlin-history text for the word alliance and which line it resides on. 

#### **Example 1**

![Screenshot 2023-02-12 at 10 18 32 PM](https://user-images.githubusercontent.com/122568668/218384949-42405ecd-1237-4df7-b1b1-a43192a4a390.png)

This helpful if we want to know the exact line this word was written in, in this specific file. 

#### **Example 2**

Here we search the entire travel_guides directory for lines that contain "Alliance". As you can see, for each file that contains the word "Alliance" it displays the file name, the line number, and a snippet of the passage. 

<img width="1200" alt="Screenshot 2023-02-13 at 12 57 25 PM" src="https://user-images.githubusercontent.com/122568668/218572938-e3e60c67-9a16-427b-aa63-8fa8f956b659.png">

This is helpful if we want to do a wider search for a specific word and how it is used in different files. We can then go to the corresponding line in the file and read the context around that word. 

