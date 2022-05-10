# Streamlining ssh Configuration

Rather than typing 
> ssh cs15lsp22zzz@ieng6.ucsd.edu <br>

to access UCSD's remote server, we shorten our login by creating file *config* in your .ssh file:



![config](https://user-images.githubusercontent.com/103288140/167225200-e391b29e-4d4d-4208-abbf-3156259e7582.PNG)

With this file, you can simply type in the command
> ssh ieng6 <br>

to login into UCSD's server, as shown below: 

![Capture](https://user-images.githubusercontent.com/103288140/167225046-69a03e05-98a9-4eb0-8a6f-fdf030af0824.PNG)


# Setup Github Access from ieng6

When making edits on the command line in the ieng6 server and you try to push and commit those edits, you get an error message explaining that you must a token-based login to commit those edits. <br>
To change this, we can create a *public* key as part of the remote access lab to GitHub. 

1. Begin by opening your terminal and typing the following line (as shown below). Copy the output that follws: 
> cat ~/.ssh/id_ed25519.pub <br>

2. In Github go to Settings &rarr; Access &rarr; SSH and GPG keys 

3. Click the green button that says *New SSH key*

4. Name your key in the *Title* field and paste your copied key in the *Key* field

5. Click *Add SSH Key* and confirm your GitHub password, and now you are done! 

By this point you should have two keys stored on GitHub: one private key and one public key



![ssh key](https://user-images.githubusercontent.com/103288140/167306435-126d250c-2a3c-459a-956e-625afcf1ad6f.PNG)



# Copy whole directories with scp -r

