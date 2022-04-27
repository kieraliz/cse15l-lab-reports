# Lab Report 2 Week 4: Debugging and Test-Driven Development

## Bug 1: Distinguishing the Difference Between Links and Images to Print the Correct Links
The code is unable to distinguish the difference between a Link and Image because the markdown syntax for Links and Images are nearly identical in that both use brackets followed by parenthesis. Other than the exclamation mark that distinguish an Image from a Link, the code is unable to distinguish Links from Images. 

Links: 

![links](https://user-images.githubusercontent.com/103288140/165162129-773c0f84-af37-4fbf-9932-c2854a2fc234.PNG)

Images:

![images](https://user-images.githubusercontent.com/103288140/165162141-2f12e5cd-eab0-4e80-8912-c818cdc3703c.PNG)


The bug lies in the fact that the code cannot distinguish links and images.
The symptom to this bug is that the code will always print out the contents of an input with brackets and parentheses, even if those lines are reserved for images and not links. Thus, when given a failure-inducing input containing an image reference, the code will print the image reference when it is not supposed to. 

We can see this symptom by running this [Failure-Inducing Input](https://github.com/kieraliz/markdown-parser/blob/main/test5.md). This output is the symptom to that [Failure-Inducing Input](https://github.com/kieraliz/markdown-parser/blob/main/test5.md): 



![test5 symptom](https://user-images.githubusercontent.com/103288140/165159855-c1d42b78-f311-4dd3-9c54-16272265c3d6.PNG)


This bug can be fixed by adding an additional if statement to catch the exclamation mark for images and only printing out the links, as shown below (lines 19-24):



![debugging test5](https://user-images.githubusercontent.com/103288140/165605388-b6138345-1502-481a-941e-a409e2a51992.PNG)

With these corerctions, when we rerun our failure-inducing input we will see that the code will no longer print the image references, and thus our bug has been fixed: 



![correct test5](https://user-images.githubusercontent.com/103288140/165162907-3bd1d3f8-dd23-44fa-be36-f6aa43c1a996.PNG)

## Bug 2: Trimming off Excess Lines to Print Links
The code returns the links by extracting all the content inside the input's parenthesis. This is problematic for the case in which there is an excessive amount of spare lines surrounding the link, in which case all the lines will be printed. 

The bug lies in the fact that there is no way to eliminate any excess lines before returning a link. As a result, the symptom to this bug is that the code will print the link and all its surrounding excess lines, when it is only supposed to print out the link. 

We can see this symptom by running this [Failure-Inducing Input](https://github.com/kieraliz/markdown-parser/blob/main/test4.md) that contains excess lines surrounding a link, which will return all the excess lines when it is not supposed to. This is the output:



![test4 symptom](https://user-images.githubusercontent.com/103288140/165167796-ffb9d0cb-ea10-47d9-931f-49aba9b4324d.PNG)

This bug can be resolved by using the String method ".trim()" to trim off the excess lines and space surrounding the code, as shown below (line 30):



![debugging test4](https://user-images.githubusercontent.com/103288140/165606127-76313cde-b3dd-422c-abdf-fe9a5995ac06.PNG)

With these corrections, when we rerun our failure-inducing input we will see that the code will only print the link without the excess lines, and thus our bug has been fixed:



![corrected test4](https://user-images.githubusercontent.com/103288140/165168326-93fc5ec6-5a0d-46b1-b03f-dcb1482c0866.PNG)

## Bug 3: Additional Line at the End of File Causes an Index Out of Bounds Exception
The current increment for currentIndex will increment currentIndex after the value of closeParen. This is problematic for the case in which extra lines are followed by links, or when the parenthesized link is not the last line of a file. Even though the code should only return the parenthesized links, the code still needs a way of processing those extra lines and characters without throwing an Index Out of Bounds Exception. 

The bug lies in the fact that it is increment the value of currentIndex once past the last parenthesis of a file. As a result, the symptom to this bug is that the terminal will fail and throw an IndexOutOfBoundsException when it is not supposed to, and also returns no links. 

We can see this symptom by running this [Failure-Inducing Input](https://github.com/kieraliz/markdown-parser/blob/main/test2.md?plain=1) that contains an extra line past the link, which will throw an IndexOutOfBoundsException when it is not supposed to. This is the output:



![symptom test2](https://user-images.githubusercontent.com/103288140/165619153-5d0a568d-8937-4caa-87cf-9a7013768efe.PNG)

This bug can be resolved by adjusting the increment of currentIndex to explicitly ensure that the value of currentIndex is being added past the last parenthesis, as shown below (lines 26-27):



![debugging test2](https://user-images.githubusercontent.com/103288140/165618831-081f7959-4ed8-4fe3-ac2e-3e00dca4d2ca.PNG)

With these corrections, when we rerun our failure-inducing input we will see that the terminal complies properly without any exceptions, and that the link is returned. Thus, our bug has been fixed:



![correct test2](https://user-images.githubusercontent.com/103288140/165619461-83875ae7-89b7-4a49-bb47-0e1cd9a47ec0.PNG)
