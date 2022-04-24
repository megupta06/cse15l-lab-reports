# Lab Report 2

## First code change
Screenshot of code change:
<img width="784" alt="Screen Shot 2022-04-24 at 12 53 58 PM" src="https://user-images.githubusercontent.com/103089880/164994131-916edde5-1e09-46ec-9f50-33a7fa96fc2e.png">

Test file for failure-including input: [Test file](/Users/mehakgupta/Documents/GitHub/markdown-parser/test-file2.md)
Failure-including optput: ```[img123.html, some-google.html]```
Despriction: In this case, the bug is that markdown parser would consider the image path as a link because the syntax of adding an image and link is the same. Both of the syntax include brackets and paranthesis. The only difference is that the syntax for adding image include '!' in the beginning. So when we run the code using failure code we get image path with the link as the output. The fixed code catches '!' and differentiates the images path and the link and returns only the link.



