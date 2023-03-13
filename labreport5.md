# Lab report Week 9

In this lab report we will explore different uses and command-line options for the `find` command. 

### **Option -name: Finds a single file by name**

If we want to find the location of a file by a specific name, you can use the `-name` command. 

Information about `-name` was found on the [ReadHat article "10 ways to use the Linux find command"](https://www.redhat.com/sysadmin/linux-find-command). 

#### **Example 1**

<img width="568" alt="Screenshot 2023-03-13 at 1 41 59 PM" src="https://user-images.githubusercontent.com/122568668/224827470-75472a22-21cd-4f99-89e1-31e44e3f1541.png">

This displays the location of the file, "whereToItaly.txt".

#### **Example 2**

<img width="586" alt="Screenshot 2023-03-13 at 1 43 19 PM" src="https://user-images.githubusercontent.com/122568668/224827713-360ea611-7327-4317-b7c8-d2e1de7db72c.png">

This shows the location and pathway of the file, "Bali-History.txt". 

This is especially helpful if you want to find a certain file, but forgot the location or folder it was in. It can be helpful in organizing your files or just finding files in general. 

### **Option -iname: Finds file by approximate name**

Sometimes you want to look for a file, but can't remember the entire name.

Information about `-iname` was found on the [ReadHat article "10 ways to use the Linux find command"](https://www.redhat.com/sysadmin/linux-find-command).

#### **Example 1**

<img width="563" alt="Screenshot 2023-03-13 at 2 03 49 PM" src="https://user-images.githubusercontent.com/122568668/224831826-7e8c276c-75b6-472a-80ac-3ba854767624.png">

This displays all the filenames that contain "athens", capitalized or lowercase.

#### **Example 2**

Here we can find all of files in which that contain "Beijing" in the name. 

<img width="562" alt="Screenshot 2023-03-13 at 2 05 34 PM" src="https://user-images.githubusercontent.com/122568668/224832198-34e4119b-32a3-403c-9e7b-4452d70c976a.png">

`-iname` is useful if we do not know whether the word we want to search is capatilized or not, or what the full exact name of the file is. 
This can also help us organize our search by keywords in the filename. 

### **Option -type d: list only directory**

We can use `-type d` to list only directories. 
Information about `-type d` was found on the [ReadHat article "10 ways to use the Linux find command"](https://www.redhat.com/sysadmin/linux-find-command).

#### **Example 1**

<img width="494" alt="Screenshot 2023-03-13 at 2 56 57 PM" src="https://user-images.githubusercontent.com/122568668/224841174-2c18bceb-9cff-4253-b6dd-a5b6f467095d.png">

Here we list out all the directories under the directory written_2. 

#### **Example 2**

<img width="551" alt="Screenshot 2023-03-13 at 2 59 34 PM" src="https://user-images.githubusercontent.com/122568668/224841613-ced81ba7-4260-4306-8d48-348c54ad99ae.png">

Here we list out all the directories under non-fiction. 

The `find -type d` can be used to make up for the limitations of the ls command's ability to filter result by file type. The `type d` command allows you to get only the listing of directories in a path.

### **Option -empty: Find empty files**

Information about `-empty` was found on the [ReadHat article "10 ways to use the Linux find command"](https://www.redhat.com/sysadmin/linux-find-command).

#### **Example 1**

<img width="464" alt="Screenshot 2023-03-13 at 3 08 28 PM" src="https://user-images.githubusercontent.com/122568668/224843031-8bf1bad9-8a53-49f1-9014-3ee734bac40a.png">

Here, we used to `-empty` to find the empty file in the current directory. 

#### **Example 2**

<img width="522" alt="Screenshot 2023-03-13 at 3 13 28 PM" src="https://user-images.githubusercontent.com/122568668/224844308-4b54438e-a5fb-475f-b6ed-bfdad3687d7c.png">

Here we search for the empty file in written_2. 

`-empty` can be helpful if we are trying to declutter our workflow and remove unused files. Also, if we created a new file for a certain purpose, but forgot where it was located, `-empty` can be used if we do not remember the file name. 
