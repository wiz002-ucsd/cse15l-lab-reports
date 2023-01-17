## Lab report Week 1

This lab report will detail the process I took in installing VS code and connecting to the remote access. 

**Step 1: Installing VS code**

Follow the instructions on the [VS code website](https://code.visualstudio.com) in order to install the software.

After opening VS code, a screen like this will appear. 
<img width="938" alt="Screen Shot 2023-01-16 at 4 58 46 PM" src="https://user-images.githubusercontent.com/122568668/212787271-014c81d2-81c0-40f3-bd26-fc58ca6dd340.png">

**Step 2: Remotely connecting**

First, you wll need to open the terminal in VS code by clicking on terminal on the menu bar and then selecting new terminal. 

<img width="1440" alt="Screen Shot 2023-01-16 at 4 09 17 PM (2)" src="https://user-images.githubusercontent.com/122568668/212787145-d4ea5fe9-8a84-4ea0-b82c-f3bcbc172044.png">

Then to connect remotely using ssh, type in the command following the %, but replacing the zz with your respective cse15L account number. 

``` % ssh cs15lwi23zz@ieng6.ucsd.edu ```

If you are connecting for the first time, you will see a message that asks 

```Are you sure you want to continue connecting?``` 

Type in “yes” and press enter. 

You will then be prompted to enter your password. When you are typing your password, it will not display in the terminal for security reasons, but they are still being entered.

A succesful connection should look like this... 
<img width="935" alt="Screen Shot 2023-01-16 at 5 07 01 PM" src="https://user-images.githubusercontent.com/122568668/212787938-abc4ecd2-dd3e-4f14-8287-74d7e1788f4a.png">

Now your terminal is successfully connected remotely to a CSE computer. 

***Step 3: Trying Some Commands*** 

Here are a list of common commands:

* cd - Change directory
    * cd ~ Goes to the home directory 
    * cd .. Goes to the previous directory

* ls - lists the files and directories within the current directory
* pwd - Shows the current directory pathway
* mkdir - Creates a new directory
* rmdir - Removes a directory

Here is an example of these basic commands:
<img width="939" alt="Screen Shot 2023-01-16 at 5 09 33 PM" src="https://user-images.githubusercontent.com/122568668/212788153-4830d88f-f388-4ccf-9215-edbdd97c6469.png">

Yay! You finished the first lab!


