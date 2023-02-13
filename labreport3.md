# Lab report Week 4/5

In this lab report we will explore different uses and command-line options for the `grep` command. 

### **Option -l: Prints file names only**

If we want to find a file that contains a certain word or phrase, we can use the `-l` option. 

<img width="416" alt="Screenshot 2023-02-12 at 8 01 20 PM" src="https://user-images.githubusercontent.com/122568668/218367546-be965d9f-e649-4d85-8d97-665ea600daeb.png">
These would be all the files that contain the word "Athens". 

<img width="414" alt="Screenshot 2023-02-12 at 8 02 38 PM" src="https://user-images.githubusercontent.com/122568668/218367676-74ce30c0-e361-49e0-a5df-d26f1c862886.png">

This shows all files that contain the word "Fast".

This is especially helpful if you are looking to find information on something, this option will allow you to single out the documents that contain the information you need. 

### **Option -i: ignore uppercase vs lowercase**

Sometimes you want to look for where a certain word is used, regardless of wether it has been capatilized or not.

<img width="535" alt="Screenshot 2023-02-12 at 7 54 04 PM" src="https://user-images.githubusercontent.com/122568668/218366700-bb29c546-e5ca-4c4f-9b7b-fe626ebe6ee9.png">
This displays all the files with the word "Hello", but if it appears as "hello", or "HELLO", then we wouldn't be able to detect it. 

<img width="559" alt="Screenshot 2023-02-12 at 7 55 45 PM" src="https://user-images.githubusercontent.com/122568668/218366887-07daeaee-804e-425c-a9c6-6164d74a5910.png">
Using this allows us to detect more files in which this word is used. 

### **Option -v: inverts match**


### **Option -n: Precede each matching line with a line number**



