# Lab Report 3 Week 6

## Streamlining ssh Configuration

Rather than typing *ssh cs15lsp22zzz@ieng6.ucsd.edu* to access UCSD's remote server, we shorten our login by creating file *config* in your .ssh file:
```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22agw
    IdentifyFile ~/.ssh/id_rsa
```

With this file, you can simply type in the command *ssh ieng6* to login into UCSD's server, as shown below: 
![Capture](https://user-images.githubusercontent.com/103288140/167225046-69a03e05-98a9-4eb0-8a6f-fdf030af0824.PNG)

You can also use the alias ieng6 when copying a file, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/168168312-4b32a2f3-dec7-4975-a560-aa89d79b19da.PNG)


## Setup Github Access from ieng6

To make a new private and public key, you can log into the remote account and use the ssh-keygen commands. The private key is stored in id_rsa, while the public key is stored in id_rsa.pub. These keys are now stored in your user account, as shown below: 
![Capture](https://user-images.githubusercontent.com/103288140/168169313-90399d91-1d55-4d8d-b174-63816da54103.PNG)

You can then add the public key to your GitHub, as shown below: 
![ssh key](https://user-images.githubusercontent.com/103288140/167306435-126d250c-2a3c-459a-956e-625afcf1ad6f.PNG)

This allows you to make [successful commits from the remote server](https://github.com/kieraliz/markdown-parser/commit/d3958b9820f67580f31cca6b84dc48f419e15bf1) and push/commit those changes to GitHub, as shown below: 

![Capture](https://user-images.githubusercontent.com/103288140/168170254-38da9f98-903e-4ddd-a9b6-fdfecc6267b7.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168170319-2dd2eb60-69f5-4468-864e-5e6bd486773d.PNG)


## Copy whole directories with scp -r

The command *scp -r* allows you to copy an entire markdown-parser directory to the remote desktop, as shown below: 

![Capture](https://user-images.githubusercontent.com/103288140/168171996-f9ac1d53-a057-4f63-a32a-605fd837348b.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168172090-4ffeaa0f-f211-40a8-b715-7e4aa237babd.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168172162-9a1ba942-6964-46ba-a75b-357bfebc495c.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168172245-f2f21a97-5a6b-4b9d-93c7-13142055b102.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168172317-a4d927a7-274a-4e13-8026-1de26d28ab0e.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168172447-89e29bee-8138-4694-965b-140f79fe9b05.PNG)

Now, from the remote server you are able to complie and run test files, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/168173053-c773a1cf-d7ef-4a6f-a121-edc5a0765543.PNG)


To achieve this all in one line, you can use the following long line of code to run the JUnit Tests without logging into my account, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/168174027-3571cacd-1ab0-4a10-90af-06c4e722fda7.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168174145-f526b879-ee3f-49f0-9827-00aa099943e4.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168174213-b8fa80e7-ce2a-46bb-852f-b3f20b99ac82.PNG)
![Capture](https://user-images.githubusercontent.com/103288140/168174269-384b7eff-82e3-428e-bd95-b1de2107e351.PNG)

