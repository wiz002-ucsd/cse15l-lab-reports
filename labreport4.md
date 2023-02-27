# Lab report Week 7

In this lab report I will reproduce the tasks from the week 8 lab competition.

### Log into ieng6
<img width="741" alt="Screenshot 2023-02-27 at 1 04 48 PM" src="https://user-images.githubusercontent.com/122568668/221685375-49b922f7-995f-48e4-a3dc-b51585337802.png">

In this step, I typed in my ieng6 log in with the ssh into the command terminal. 

`ssh cs15lwi23asz@ieng6.ucsd.edu` `<enter>`

### Clone your fork of the repository from your Github account
<img width="756" alt="Screenshot 2023-02-27 at 1 18 54 PM" src="https://user-images.githubusercontent.com/122568668/221687914-79d2321d-c6e6-4844-9a8a-f79df9cae8bd.png">

In this step, I first `cmd + c` to copy the github link "git@github.com:wiz002-ucsd/lab7.git" and then typed in `git clone` `cmd + v` `<enter>` to clone the repository.

### Run the tests, demonstrating that they fail
<img width="770" alt="Screenshot 2023-02-27 at 1 25 53 PM" src="https://user-images.githubusercontent.com/122568668/221689190-6d838f42-0292-4772-b547-d78def6735f7.png">

Then, I typed `cd lab7` to change to the lab7 directory. 
From the cse15l website, I copied pasted the Junit compile and run commands. 

Keys pressed: `cmd + c` + `cmd + v` `<enter>`, then `cmd + c`, `cmd + v` 

Those commands copy and pasted the lines below. 

`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`

`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore <TesterName>`

After this, I typed in the tester name, `ListExampleTests` and pressed `<enter>`. 

As shown in the picture, one of the tests has failed. 

### Edit the code file to fix the failing test

To edit the code, I used nano, and typed in `nano ListExamples.java` `<enter>`. 

This brought up the following display. 
<img width="789" alt="Screenshot 2023-02-27 at 1 42 46 PM" src="https://user-images.githubusercontent.com/122568668/221692372-21739857-1c60-40e2-9fc3-1d302bbe2ba5.png">

To fix the code, I typed in `cmd + f` `index1` `<enter>` to get me to the part of the code that needs fixing. 

<img width="773" alt="Screenshot 2023-02-27 at 1 45 09 PM" src="https://user-images.githubusercontent.com/122568668/221692836-be699791-9234-460a-a5a1-db44a932a3b4.png">

Then I pressed `<delete>`, `2` to fix the code. 

To save and exit, I pressed: `Cntrl + o` `<enter>` and then `Cntrl + x`. 

### Run the tests, demonstrating that they now succeed

<img width="776" alt="Screenshot 2023-02-27 at 1 48 47 PM" src="https://user-images.githubusercontent.com/122568668/221693530-c8ca8f41-75a6-440e-b5d7-9fa9b526b2d6.png">

To the run tests I pressed: `<up><up><up><enter><up><up><up><enter>`
First pressed up three times to get to the javac Junit compile command, and then repeated that to get to the java Junit run command. 

`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` was three up on the command history. 

`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` after running javac, this command was also 3 up on the command history. 


### Commit and push the resulting change to your Github account (you can pick any commit message)

To push I typed: `git add Li` `<tab>` `.java`. `<enter>`
After typeing "Li", tab allowed it to automatically finish typing `ListExamples`, but I had to additionally type in `.java`. 

To commmit I typed: `git commit -m "Finished"` `<enter>`. 

<img width="537" alt="Screenshot 2023-02-27 at 2 00 52 PM" src="https://user-images.githubusercontent.com/122568668/221695735-1a8b5d82-dcbc-45c0-9ff9-326e1b2d8e6f.png">

**I've finished the tasks**

