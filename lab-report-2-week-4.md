# Lab Report 2 Week 4: Debugging and Test-Driven Development

## Bug 1: 


## Bug 2: Distinguishing the Difference Between Links and Images
The code is unable to distinguish the difference between a Link and Image because the markdown syntax for Links and Images are nearly identical in that both use brackets followed by parenthesis. Other than the exclamation mark that distinguish an Image from a Link, the code is unable to distringuish the difference between Links and Images. 
> Links: []()
> Images: ![]()

The bug is that the code will always print out the contents of an input with the syntax [](), even if those lines are reserved for images and not links. 
As a result, the *failure-inducing input* is that when we run an input containing an image, the code will print the image's link when it is not supposed to. 

We can see this symptom by running this [Failure-Inducing Input](https://github.com/kieraliz/markdown-parser/blob/main/test5.md). 

The output: 
![test5 symptom](https://user-images.githubusercontent.com/103288140/165159855-c1d42b78-f311-4dd3-9c54-16272265c3d6.PNG)




This bug can be fixed by adding an additional if statement as shown below (lines 19-23):



![test5](https://user-images.githubusercontent.com/103288140/165159142-b941f7d0-9a39-4413-85dd-af5b78a9cc9a.PNG)


## Bug 3: 
