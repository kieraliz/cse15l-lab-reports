# Lab Report 4 Week 8

Here is the link to my [Markdown Parse Repository](https://github.com/kieraliz/markdown-parser). <br>
Here is the link to the [Markdown Parse Repository](https://github.com/anhthony/markdown-parser) I reviewed in Week 7.

## Testing Snippet 1

Snippet 1 *should* produce the following links:
> [`google.com, google.com, ucsd.edu]

I used this code in my implementation of MarkdownParse to turn Snippet 1 into a test: <br>
![Capture](https://user-images.githubusercontent.com/103288140/169716411-32c09071-77df-49a5-abce-c6498a7b837f.PNG)

On my implementation, the test failed because the expected output was not the same as the output that was returned. This was the JUnit output: <br>
![Capture](https://user-images.githubusercontent.com/103288140/169716432-6f05374b-9b86-41c5-ae1c-41bd676d8f71.PNG)

Similarly, I used this code in the other implementation of MarkdownParse2Lab4 to turn Snippet 1 into a test: <br>
![Capture](https://user-images.githubusercontent.com/103288140/169716466-4c1962f0-6988-415f-8441-53f2db1bfad4.PNG)

On this implementation, the test failed because the expected output was not the same as the output that was returned. This was the JUnit output: <br>
![Capture](https://user-images.githubusercontent.com/103288140/169716494-d175627b-f397-4212-8323-191e297aa99d.PNG)


## Testing Snippet 2

Snippet 2 *should* produce the following links:
> [a.com, a.com(()), example.com]

I used this code in my implementation MarkdownParse to turn Snippet 2 into a test: <br>
![Capture](https://user-images.githubusercontent.com/103288140/169707166-31e2561d-74e4-4655-9b50-f75a56398a90.PNG)

On my implementation, the test failed because an IndexOutOfBoundsException was thrown. This was the JUnit output: <br>
![Capture](https://user-images.githubusercontent.com/103288140/169707222-6c32b939-e2bb-4a1e-82fc-f25dec92521d.PNG)

Similarly, I used this code in the other implementation of MarkdownParse2Lab4 to turn Snippet 2 into a test: <br> 
![Capture](https://user-images.githubusercontent.com/103288140/169716726-16abcf18-bd8e-47b7-9a58-52d5cebbbdca.PNG)

On this implementation, the test failed because the expected output was not the same as the output that was returned. This was the JUnit output: <br>
![Capture](https://user-images.githubusercontent.com/103288140/169716773-4e1e6684-bb9a-4ff3-bdaa-0ef7d3221cf6.PNG)

## Testing Snippet 3

Snippet 3 *should* produce the following links:
> [https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]

I used this code in my implementation of MarkdownParse to turn Snippet 3 into a test: <br>

On my implementation, the test failed because an IndexOutOfBoundsException was thrown. This was the JUnit output: <br>

Similiarly, I used this code in the other implementation of MarkdownParse2Lab4 to turn Snippet 3 into a test: <br>

On this implementation, the test failed because the expected output was not the same as the output that was returned. This was the JUnit output: <br>

## Editing Snippet 1: All cases with Backticks

The problem is caused when backticks are inside and outside of the brackets. To fix this, you can create an if statement that catches the backtick, and breaks from the while loop, as shown below: 

You can make the program account for all cases with backticks by having if statements to check the backticks are inside the brackets or parentheses, as shown below:

identifying everything inside the backticks. If the backticks contain 

if statement:

check the content inside the backticks:
if there is a backtick containing [ and no [ before the backticks --> bad 
similiar for the other bracket ]
otherwise, you can extract the link in the parentheses 

containing only one backtick, bad 

`[`]
[`]`
[`[`]
[`]`]

## Editting Snippet 2: All cases with Nest Parentheses, Brackets, and Escaped Brackets

checking that the next open bracket is past the next closed bracket
check that index of next closed bracket < index of next open bracket

checking everything in pairs, only evaluating the content inside the parentheses and not the brackets

## Editting Snippet 3: All cases with Newlines in Brackets and Parenthesis

check for \n, if found then move on
check if any brackets and parentheses index is -1, then move on


