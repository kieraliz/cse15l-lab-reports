# Lab Report 5 Week 10

## Finding the differences: 
I used *vimdiff* to find all differences in the two results.txt files from my implementation and the other implementation. <br>
Using the line <br>
> vimdiff my-markdown-parser/results.txt cse15lsp22agw-markdown-parser-fork/results.txt <br>


I got this output (plus many more lines): 
![Capture](https://user-images.githubusercontent.com/103288140/172065678-6d9fb3e0-7f60-454f-84ea-7f9e683d9fee.PNG)

## Test 1: 574.md

Looking at [Test 574.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/574.md?plain=1), my implementation produced a non-empty output while the other implementation produced nothing, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172068106-31ec19b1-c535-4bf8-a9d7-47569920d27b.PNG)

Using CommonMark, my implementation is correct and the other implementation is incorrect, because the test should not produce any links, as show below:
![Capture](https://user-images.githubusercontent.com/103288140/172068148-55d94357-07de-4610-923f-17ec7ba21065.PNG)

For the other implementation, the bug is that the code does not catch the exclamation mark to distinguish images from links. This can be fixed by adding an if statement to catch the exclamation mark before the first open bracket, as shown below: 
![Capture](https://user-images.githubusercontent.com/103288140/172068973-3fd61818-3fed-4389-8aa5-67c09ce12610.PNG)


## Test 2: 577.md

Looking at [Test 577.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/577.md?plain=1) my implementation produced nothing while the other implementation produced an non-empty output, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172067571-04d33165-0e55-49ca-9b5d-b789e01e22d6.PNG)

Using CommonMark, my implementation is correct and the other implementation is incorrect, because the test should not produce any links, as shown below:
![Capture](https://user-images.githubusercontent.com/103288140/172067647-7986cbd1-3586-4acf-8666-2b18c37d7292.PNG)

Like the previous example, the bug in the other implementation is that the code does not catch the exclamation mark before the first open bracket, and also does not catch the ".jpeg" or ".png" or any other indicators that the contents within the parentheses is an image. This can be fixed by adding an if statement to catch any special phrases, as shown below: 
![Capture](https://user-images.githubusercontent.com/103288140/172068712-64e5f9ee-d567-438a-a60b-54e18c0e6f16.PNG)
