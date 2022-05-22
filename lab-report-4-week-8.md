# Lab Report 4 Week 8

Here is the link to my [Markdown-Parse Repository](https://github.com/kieraliz/markdown-parser). <br>
Here is the link to the [Markdown-Parse Repository](https://github.com/anhthony/markdown-parser) I reviewed in Week 7.

## Testing Snippet 1

Snippet 1 *should* produce the following links:
> [%60google.com, google.com, ucsd.edu]

I used this code in MarkdownParseTest to turn Snippet 1 into a test:
![Capture](https://user-images.githubusercontent.com/103288140/169707012-28827fd4-6898-408b-9f62-f1ecdd5bac97.PNG)

On my implementation, the test failed because the expected output was not the same as the output that was returned. This was the JUnit output:
![Capture](https://user-images.githubusercontent.com/103288140/169707057-db5c505c-1f46-4318-9a0f-73214bbe2ec7.PNG)

TEST ON REVIEWED

## Testing Snippet 2

Snippet 2 *should* produce the following links:
> [a.com, a.com(()), example.com]

I used this code in MarkdownParse to turn Snippet 2 into a test:
![Capture](https://user-images.githubusercontent.com/103288140/169707166-31e2561d-74e4-4655-9b50-f75a56398a90.PNG)

On my implementation, the test failed because an IndexOutOfBoundsException was thrown. This was the JUnit output:
![Capture](https://user-images.githubusercontent.com/103288140/169707222-6c32b939-e2bb-4a1e-82fc-f25dec92521d.PNG)

TEST ON REVIEWED

## Testing Snippet 3

Snippet 3 *should* produce the following links:
> [https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]

I used this code in MarkdownParse to turn Snippet 3 into a test:
![Capture](https://user-images.githubusercontent.com/103288140/169707289-4266ec98-5add-4b6a-94c9-5030da3662dd.PNG)

On my implementation, the test failed because an IndexOutOfBoundsException was thrown. This was the JUnit output:
![Capture](https://user-images.githubusercontent.com/103288140/169707310-8437856b-2075-413a-aced-ea615fa878e9.PNG)

TEST ON REVIEWED
