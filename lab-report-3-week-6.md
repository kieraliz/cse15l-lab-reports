# Streamlining ssh Configuration

Rather than typing 
> ssh cs15lsp22zzz@ieng6.ucsd.edu <br>

to access UCSD's remote server, we shorten our login by creating file *config* in your .ssh file:
```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22agw
    IdentifyFile ~/.ssh/id_rsa
```

With this file, you can simply type in the command
> ssh ieng6 <br>

to login into UCSD's server, as shown below: 

![Capture](https://user-images.githubusercontent.com/103288140/167225046-69a03e05-98a9-4eb0-8a6f-fdf030af0824.PNG)

You can also use the alias ieng6 when copying a file, as shown below:

![Capture](https://user-images.githubusercontent.com/103288140/168168312-4b32a2f3-dec7-4975-a560-aa89d79b19da.PNG)


# Setup Github Access from ieng6

To make a new private and public key, I logged into the remote account and used ssh-keygen. The private key is stored in id_rsa, while the public key is stored in id_rsa.pub. These keys are now stored in my user account, as shown below: 

![Capture](https://user-images.githubusercontent.com/103288140/168169313-90399d91-1d55-4d8d-b174-63816da54103.PNG)

I then added the public key to my GitHub, as shown below: 

![ssh key](https://user-images.githubusercontent.com/103288140/167306435-126d250c-2a3c-459a-956e-625afcf1ad6f.PNG)

These steps allow me to make changes from the remote terminal and push/commit those changes to GitHub, as shown below: 

![Capture](https://user-images.githubusercontent.com/103288140/168170254-38da9f98-903e-4ddd-a9b6-fdfecc6267b7.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168170319-2dd2eb60-69f5-4468-864e-5e6bd486773d.PNG)


# Copy whole directories with scp -r

