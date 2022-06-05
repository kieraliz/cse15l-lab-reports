# Lab Report 5 Week 10

## Finding the differences: 
I used *vimdiff* to find all differences in the two results.txt files from my implementation and the other implementation, which produced the output shown below (plus many more lines): 
![Capture](https://user-images.githubusercontent.com/103288140/172065678-6d9fb3e0-7f60-454f-84ea-7f9e683d9fee.PNG)

## Test 1: 577.md

Looking at [Test 577.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/577.md) my implementation produced nothing while the other implementation produced an non-empty output, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172067571-04d33165-0e55-49ca-9b5d-b789e01e22d6.PNG)

Using CommonMark, my implementation is correct while the other implementation is incorrect because the test should not produce any links, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172067647-7986cbd1-3586-4acf-8666-2b18c37d7292.PNG)

For the other implementation, the bug is that the code did not catch the exclamation mark before the open bracket. This can potentially be fixed by adding an if statement that catches the exclamation mark at the index before the open bracket, and exiting if it is found. <br>
Also, we can check that the content inside the parentheses does not contain ".jpeg" or ".png" or any other indicators that it is an image.
![Capture](https://user-images.githubusercontent.com/103288140/172067786-850faf46-2721-4807-95f3-b3628bacea2e.PNG)

## Test 2: 574.md

Looking at [Test 574.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/574.md), my implementation produced a non-empty output while the other implementation produced nothing, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172068106-31ec19b1-c535-4bf8-a9d7-47569920d27b.PNG)

Using CommonMark, my implementation is correct while the other implementation is incorrect because the test should not produce any links, as show below:
![Capture](https://user-images.githubusercontent.com/103288140/172068148-55d94357-07de-4610-923f-17ec7ba21065.PNG)

Like the previous example, the bug in the other implementation lies in the fact that the codes does not catch any exclamation marks 
In my implementation, the bug lies in the fact that the code does not identify any spaces within the parentheses. If there are spaces in the parentheses, then it is not a link. <br>
This can be fixed by adding an if statement that checks for any spaces, and moves on if found, as shown below: 
![Capture](https://user-images.githubusercontent.com/103288140/172067336-9f5af60c-7eba-49f5-84a1-ccb7c5dcad4c.PNG)

