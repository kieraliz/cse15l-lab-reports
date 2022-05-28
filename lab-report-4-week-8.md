# Lab Report 4 Week 8

Here is the link to my [Markdown Parse Repository](https://github.com/kieraliz/markdown-parser). <br>
Here is the link to the [Markdown Parse Repository](https://github.com/anhthony/markdown-parser) I reviewed in Week 7.

## Testing Snippet 1

Using CommonMark, Snippet 1 *should* produce the following links:
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

Using CommonMark, Snippet 2 *should* produce the following links:
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

Using CommonMark, Snippet 3 *should* produce the following links:
> [https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]

I used this code in my implementation of MarkdownParse to turn Snippet 3 into a test: <br>
![Capture](https://user-images.githubusercontent.com/103288140/170833633-53d5c832-8741-4b8c-9054-d294e8824651.PNG)

On my implementation, the test failed because an IndexOutOfBoundsException was thrown. This was the JUnit output: <br>
![Capture](https://user-images.githubusercontent.com/103288140/170833660-8e6f719d-570c-4c50-b1bd-d221267e9dc7.PNG)

Similiarly, I used this code in the other implementation of MarkdownParse2Lab4 to turn Snippet 3 into a test: <br>
![Capture](https://user-images.githubusercontent.com/103288140/170833682-22eb72a6-75eb-4326-9643-cdc977d28a42.PNG)

On this implementation, the test failed because the expected output was not the same as the output that was returned. This was the JUnit output: <br>
![Capture](https://user-images.githubusercontent.com/103288140/170833710-364d6ebe-6d29-436d-9f6c-aa22bc6cda5c.PNG)

## Editing Snippet 1: All cases with Backticks

The problem is caused when backticks are inside and outside of the brackets. To fix this, you can create an if statement that catches the backtick before the first bracket, as shown below: <br>
![Capture](https://user-images.githubusercontent.com/103288140/170835319-aaa2b2e9-cf94-4d20-83e9-2076fe083bae.PNG)

## Editing Snippet 2: All cases with Nest Parentheses, Brackets, and Escaped Brackets

The problem is caused by multiple nested pairs that confuse the program. Fixing this problem would be a more involved change that would check for that each pair of parentheses were closed. You would also have to use the last parentheses and not the first, also by checking for the next open bracket. 

## Editing Snippet 3: All cases with Newlines in Brackets and Parenthesis

The problem is caused when new lines are inside the open and closed brackets. To fix this, you can use String methods .substring() and .replace to replace all the new lines, as shown below: <br>
![Capture](https://user-images.githubusercontent.com/103288140/170835911-38fd64b6-5fd0-4b27-94f7-e2fc8bffb7fd.PNG)


