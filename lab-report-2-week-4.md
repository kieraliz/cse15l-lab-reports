# Lab Report 2 Week 4: Debugging and Test-Driven Development

## Bug 1: 


## Bug 2: Distinguishing the Difference Between Links and Images

explain the bug (cannot distinguish links and images) --> explain symptom (will print out images when not supposed to) --> failure-inducing input (test5) --> symptom/ result of that input (screenshot printing results from incorrect test5) --> how to fix (additional changes)

The code is unable to distinguish the difference between a Link and Image because the markdown syntax for Links and Images are nearly identical in that both use brackets followed by parenthesis. Other than the exclamation mark that distinguish an Image from a Link, the code is unable to distinguish Links from Images. 

Links: 

![links](https://user-images.githubusercontent.com/103288140/165162129-773c0f84-af37-4fbf-9932-c2854a2fc234.PNG)

Images:

![images](https://user-images.githubusercontent.com/103288140/165162141-2f12e5cd-eab0-4e80-8912-c818cdc3703c.PNG)


The bug lies in the fact that the code cannot distinguish links and images.
The symptom to this bug is that the code will always print out the contents of an input with brackets and parentheses, even if those lines are reserved for images and not links. Thus, when given a failure-inducing input containing an image reference, the code will print the image reference when it is not supposed to. 

We can see this symptom by running this [Failure-Inducing Input](https://github.com/kieraliz/markdown-parser/blob/main/test5.md). This output is the symptom to that [Failure-Inducing Input](https://github.com/kieraliz/markdown-parser/blob/main/test5.md): 



![test5 symptom](https://user-images.githubusercontent.com/103288140/165159855-c1d42b78-f311-4dd3-9c54-16272265c3d6.PNG)


This bug can be fixed by adding an additional if statement to catch the exclamation mark for images and only printing out the links, as shown below (lines 19-23):



![test5](https://user-images.githubusercontent.com/103288140/165159142-b941f7d0-9a39-4413-85dd-af5b78a9cc9a.PNG)

With these corerctions, when we rerun our failure-inducing input we will see that the code will no longer print the image references, and thus our bug has been fixed: 



![correct test5](https://user-images.githubusercontent.com/103288140/165162907-3bd1d3f8-dd23-44fa-be36-f6aa43c1a996.PNG)

## Bug 3: 
