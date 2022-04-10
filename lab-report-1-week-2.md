# Lab Report 1 Week 2: A Guide to Setting up Remote Access

Hello incoming CSE 15L students! Welcome to your guide to setting up Remote Access for logging into a couse-specific account on ieng6.

## Step 1: Installing VS Code
Virtual Studio Code (also known as VS Code) is a powerful programming tool used for creating code. To install VS Code, go to the [VS Code Download page](https://code.visualstudio.com/) and follow the instructions for your device. Once VS Code is fully installed, the app should look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162634613-fdc35664-fd35-4e2b-b32b-597ecfc05aaf.PNG)

## Step 2: Remotely Connecting

#### Course-Specific Account
UCSD's CSE courses uses course-specific accounts. We will learn how to Connect to a Remote Host using our course-specific account - a practice used by many institutions and future jobs.

To look up your course-specific account for CSE15L, go to this link: [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php) 

For CSE 15L your course-specific account should look start with *cs15lsp22* followed by three unique characters.

For example, if my three unique characters are "abc," then my course-specific account would read: cs15lsp22abc

*Note: The sixth character is the **lowercase letter l**, not the number one. This should read: c s e 1 5 l s p 2 2 . . .*


#### VS Code Terminal
The Terminal feature of VS Code allows you to run code. To open the terminal, find the upper tab *Terminal* &rarr; *New Terminal.* You can resize the terminal to your liking. 

Your screen should look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162635318-140ee022-0aca-4317-b37f-79a0b3a24ae5.PNG)

In the terminal replace the "abc" with your three unique characters to your course-specific account, and type the following command: 
> ssh cs15lsp22abc@ieng6.ucsd.edu

*Reminder: The sixth character is the lowercase letter l, not the number one!*

If you see a message like this:
> ssh cs15lsp22abc@ieng.ucsd.edu
> 
> The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
> 
> RSA key fingerprint is 
> SHA256.ksruYwhnYH+sySHnHAtLUHngrPEyZTD1/1x99wUQcec.
> 
> Are you sure you want to continue connecting
> (yes/no/[fingerprint])?

Type *yes* and press enter.

You will then be prompted to type your password. 
Type your password and press enter. 

Content will load onto your page and your screen may look something like this:



![screenshot](https://user-images.githubusercontent.com/103288140/162636340-bdcc58d6-1794-42de-ab6f-e0f3f6af6dbb.PNG)


Woohoo, you're logged in! Your terminal is now connected to a computer in the CSE basement. Your computer device is the *client* and the computer in the CSE basement is the *server* based on how you are connected. 

## Step 3: Trying Some Commands
Now that you are logged into the server, here are some commands to try in your terminal!

#### cd
The command *cd* stands for Change Directory and is used to change the current directory to another directory.

#### ls -lat
The *ls* command is used to list files. 
The command *ls -lat* will list all files with their respective dates and times. This command may look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162639061-cde4df08-5d4f-47e8-aca0-10b3f1b48abd.PNG)

#### ls -a

The command *ls -a* will list all files. This command may look like this: 



![Capture](https://user-images.githubusercontent.com/103288140/162639089-286d87a8-9d91-4bf7-a6c5-414fc3face1d.PNG)


#### ls /home/linux/ieng6/cs15lsp22/cs15lsp22abc
The command *ls /home/linux/ieng6/cs15lsp22/cs15lsp22abc* will list the directories in your ieng6 server account. 
After replacing the last three characters "abc" with your own three unique characters from your course-specific account, the command may look like this: 



![Capture](https://user-images.githubusercontent.com/103288140/162639150-b15b42e9-c409-4a94-8336-0f08af949f95.PNG)


#### cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
The command *cp* will copy a file. Interestingly, the command *cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/* will produce error messages. This is because we are trying to copy a file we do not have access to. Thus, the command may look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162640064-769d4022-9653-453a-aa6c-7341deee877f.PNG)


#### cat /home/linux/ieng6/cs15lsp22/public/hello.txt
The *cat* command will read a file and print their contents. Like the previous example, the command *cat /home/linux/ieng6/cs15lsp22/public/hello.txt* will produce error messages because we do not have access to the text file hello.txt. Thus, the command may look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162640167-9d5486f4-1198-48a5-bee0-98f1ce64c19d.PNG)



## Step 4: Moving Files with scp


## Step 5: Setting an SSH Key


## Step 6: Optimizing Remote Running



