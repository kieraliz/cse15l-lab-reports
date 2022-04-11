# Lab Report 1 Week 2: A Guide to Setting up Remote Access

Hello incoming CSE 15L students! This is your guide to set up Remote Access for logging into a couse-specific account on ieng6.

## Step 1: Installing VS Code
Virtual Studio Code (also known as VS Code) is a powerful programming tool used for creating code. To install VS Code, go to the [VS Code Download page](https://code.visualstudio.com/) and follow the instructions for your device. Once VS Code is fully installed, the app should look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162634613-fdc35664-fd35-4e2b-b32b-597ecfc05aaf.PNG)

## Step 2: Remotely Connecting

#### Course-Specific Account
UCSD's CSE courses uses course-specific accounts. We will learn how to Connect to a Remote Host using our course-specific account - a practice used by many institutions and future jobs.

To look up your course-specific account for CSE15L, go to this link: [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php) 

For CSE 15L your course-specific account should look start with *cs15lsp22* followed by a username of three unique characters.

For example, if my username of three unique characters is "abc," then my course-specific account would read: cs15lsp22abc

*Note: The sixth character is the **lowercase letter l**, not the number one. This should read: c s e 1 5 l s p 2 2 . . .*


#### VS Code Terminal
The Terminal feature of VS Code allows you to run code. To open the terminal, find the upper tab *Terminal* &rarr; *New Terminal.* You can resize the terminal to your liking. 

Your screen should look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162635318-140ee022-0aca-4317-b37f-79a0b3a24ae5.PNG)

In the terminal replace the "abc" with your three-character username, and type the following command: 
> ssh cs15lsp22abc@ieng6.ucsd.edu

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

You will then be prompted to type your password. Type your password and press enter. 

Content will load onto your page and your screen may look something like this:



![screenshot](https://user-images.githubusercontent.com/103288140/162636340-bdcc58d6-1794-42de-ab6f-e0f3f6af6dbb.PNG)


Your terminal is now connected to a computer in the CSE basement. Your computer device is the *client* and the computer in the CSE basement is the *server* based on how you are connected. 

## Step 3: Trying Some Commands
Now that you are logged into the server, here are some commands to try in your terminal!

#### cd
The command *cd* stands for Change Directory and is used to change the current directory to another directory.

#### ls -lat
The *ls* command is used to list files. 
The command *ls -lat* will list all files with their respective dates and times. Your command may look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162639061-cde4df08-5d4f-47e8-aca0-10b3f1b48abd.PNG)

#### ls -a

The command *ls -a* will list all files. Your command may look like this: 



![Capture](https://user-images.githubusercontent.com/103288140/162639089-286d87a8-9d91-4bf7-a6c5-414fc3face1d.PNG)


#### ls /home/linux/ieng6/cs15lsp22/cs15lsp22abc
The command *ls /home/linux/ieng6/cs15lsp22/cs15lsp22abc* will list the directories in your ieng6 server account. 
After replacing the last three characters "abc" with your own three-character username, your command may look like this: 



![Capture](https://user-images.githubusercontent.com/103288140/162639150-b15b42e9-c409-4a94-8336-0f08af949f95.PNG)


#### cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
The command *cp* will copy a file. Interestingly, the command *cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/* will produce error messages. This is because we are trying to copy a file we do not have access to. Thus, your command may look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162640064-769d4022-9653-453a-aa6c-7341deee877f.PNG)


#### cat /home/linux/ieng6/cs15lsp22/public/hello.txt
The *cat* command will read a file and print their contents. Like the previous example, the command *cat /home/linux/ieng6/cs15lsp22/public/hello.txt* will produce error messages because we do not have access to the text file hello.txt. Thus, your command may look like this:



![Capture](https://user-images.githubusercontent.com/103288140/162640167-9d5486f4-1198-48a5-bee0-98f1ce64c19d.PNG)



## Step 4: Moving Files over SSH with scp
We will now learn how to work remotely by copying files back and forth between the local and remote computers. This is done using the command *scp*, which will securely copy a file. 

#### WhereAmI.java
Create a file on your computer with the following content:
> class WhereAmI {
> 
>   public static void main(String[] args) {
>   
>     System.out.println(System.getProperty("os.name"));
>     
>     System.out.println(System.getProperty("user.name"));
>     
>     System.out.println(System.getProperty("user.home"));
>     
>     System.out.println(System.getProperty("user.dir"));
>     
>   }
>   
> }

Run this file using *javac* and *java* on your command.

Next, in the terminal run this command (using your username):
> scp WhereAmI.java cs15lsp22abc@ieng6.ucsd.edu:~/

When asked for your password, type in your password. 

Next, log out of ieng6 by typing *exit* into the terminal

Then, log into ieng6 with ssh again by entering the following command with your username into the terminal:
> ssh cs15lsp22abc@ieng6.ucsd.edu

Use the *ls* command and you should see the file WhereAmI in your home directory. This means that you can now run WhereAmI on the ieng6 computer using javac and java. 
After using the *ls* commands and running *javac* and *java*, your command may look like this:



![screenshot](https://user-images.githubusercontent.com/103288140/162643729-d04d6ace-bb32-433d-b4bd-389952f79ba9.PNG)



## Step 5: Setting an SSH Key
Just as websites such as Canvas save password account information, we can use an ssh key to create a *public key* and *private key* to save our server password information. This allows us to login into the server without having to enter our password information. To set this up, enter the command:
> ssh-keygen
> 
> Generating public/private rsa key pair.
> 
> Enter file in which to save the key
> (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
> 
> Enter passphrase (empty for no passphrase):
 
**Important: When asked for a passphrase DO NOT ADD A PASSPHRASE. Simply press *Enter***

Content will load onto the screen and the command may look like this:
	
  

![screenshot](https://user-images.githubusercontent.com/103288140/162644408-063a77c2-3d6d-4d18-bae0-01147bccfb4e.PNG)

These commands created two new files on your system:
* The *private key* in file id_rsa
* The *public key* in file id_rsa.pub

Using your three-character account username, enter the following commands into the terminal:
> ssh cs15lsp22abc@ieng6.ucsd.edu
>
> <Enter your Password>
>
> mkdir .ssh
> 
> exit
> 
> scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22abc@ieng6.ucsd.edu:~/.ssh/authorized_keys

Once you do this, you should be able to log into the server without entering a password, as shown below:



![screenshot](https://user-images.githubusercontent.com/103288140/162644698-136c9530-f493-489b-b6ee-04961f53b30a.PNG)

## Step 6: Optimizing Remote Running
Now that our remote server is set up, we can easily make local edits to *WhereAmI.java* to simply our code with 1 keystroke. 

Replace "abc" with your server username and enter the following code into the terminal:
> scp WhereAmI.java cs15sp22abc@ieng6.ucsd.edu:~/ ; ssh cs15lsp22abc@ieng6.ucsd.edu "javac WhereAmI.java" ; ssh cs15lsp22abc@ieng6.ucsd.edu "java WhereAmI"
 
This line of code will copy any local edits made to WhereAmI.java and return these changes to the remote server - all in one keystroke! 
 
## Concluding notes
In this tutorial we learned how to:
1. Install VS Code
2. Remotely Connect to Remote Servers
3. Try Commands such as ls, cd, and more
4. Move Files with scp
5. Set up an SSH Key 
6. Optimize Remote Running with one keystroke
 
Congrats on setting up Remote Access CSE 15L students! You are incredible!
