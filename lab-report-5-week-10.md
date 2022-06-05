# Lab Report 5 Week 10

## Finding the differences: 
I used *vimdiff* to find all differences in the two results.txt files from my implementation and the other implementation, which produced the output shown below (plus many more lines): 
![Capture](https://user-images.githubusercontent.com/103288140/172065678-6d9fb3e0-7f60-454f-84ea-7f9e683d9fee.PNG)

## Test 1: 519.md

Looking at [Test 519.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/519.md) my implementation produced nothing while the other implementation produced an non-empty output, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172066302-a6669295-e4ba-4053-9048-13c850bdff54.PNG)

Using CommonMark, my implementation is correct while the other implementation is incorrect because the test should not produce any links, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172066401-5db32516-964b-4bda-85cf-ec0e12a77060.PNG)

For the other implementation, the bug is that the code did not catch the exclamation mark before the open bracket. This can potentially be fixed by adding an if statement that catches the exclamation mark at the index before the open bracket, and exiting if it is found. <br>

## Test 2: 567.md

Looking at [Test 567.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/567.md), my implementation produced a non-empty output while the other implementation produced nothing, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172066825-cdf48c97-1bb9-4f6b-9ac8-3d0fc79edf1c.PNG)

Using CommonMark, my implementation is incorrect while the other implementation is correct because the test should not produce any links, as show below:
![Capture](https://user-images.githubusercontent.com/103288140/172066876-9a1ac269-182b-4b37-92c9-afadbbf4a5c2.PNG)

In my implementation, the bug lies in the fact that the code does not identify any spaces within the parentheses. If there are spaces in the parentheses, then it is not a link. <br>
This can be fixed by adding an if statement that checks for any spaces, and moves on if found, as shown below: 
![Capture](https://user-images.githubusercontent.com/103288140/172067336-9f5af60c-7eba-49f5-84a1-ccb7c5dcad4c.PNG)

