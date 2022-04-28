# Lab Report 2

## First Code Change

**Failure:** When there is an image with the links in the same file

**Screenshot of code change:**


<img width="835" alt="Screen Shot 2022-04-24 at 2 14 39 PM" src="https://user-images.githubusercontent.com/103089880/164996873-848870ca-c4b2-4378-af02-776d9a8225b8.png">



**Test file for failure-inducing input:**  [Test file](https://github.com/megupta06/markdown-parser/blob/6eb16e74e7d2c49f11b34ed1c2e0d6b9a6ad27d7/test-file2.md)


**Failure-inducing optput:**  ```[img123.html, some-google.html]```



**Despriction:**  In this case, the bug is that markdown parser would consider the image path as a link because the syntax of adding an image and link is the same. Both of the syntax include brackets and paranthesis. The only difference is that the syntax for adding image include ```!``` in the beginning.  The failure-inducing input contains both links and images. When running the code with this input, the symptom caused by this bug is that the output contains both links and names of the image files instead of just links. The fixed code catches ```!``` and differentiates the images path and the link and returns only the links.


****************************

## Second Code Change

**Failure:** When open paranthesis is not after close bracket


**Screenshot of code change:**

<img width="835" alt="Screen Shot 2022-04-24 at 2 16 59 PM" src="https://user-images.githubusercontent.com/103089880/164996958-8c542ea3-3492-4ddd-bce1-de73a5a373bd.png">


**Test file for failure-inducing input:** [Test file](https://github.com/megupta06/markdown-parser/blob/bffbfb0db3c81a5cbd3576dce4da571f6de1b023/test-file3.md)

**Failure-inducing optput:** ```[page.com]```


**Despriction:** In this case, the bug is that markdown parser would consider this fa syntax is not right for link but since it contains brackets and paranthesis in right order, the output is the text in paranthesis. The failure-inducing input contains a space after the close bracket which makes the syntax faulty. When running the code with this input, the symptom caused by this bug is that the output contains the text in paranthesis though it should not.

*************************************


## Third Code Change

**Failure:** When there are no links in the file

**Screenshot of code change:**

<img width="835" alt="Screen Shot 2022-04-24 at 3 09 55 PM" src="https://user-images.githubusercontent.com/103089880/164998791-3ac7f536-df47-41e1-8c16-11adab3e1c5f.png">



**Test file for failure-inducing input:** [Test file](https://github.com/megupta06/markdown-parser/blob/e5ad76ea3acd141816062419e1346704fde3700e/test-file4.md)

**Failure-inducing optput:** 
```
Exception in thread "main" java.lang.StringIndexOutOfBoundsException: String index out of range: -2
        at java.base/java.lang.StringLatin1.charAt(StringLatin1.java:48)
        at java.base/java.lang.String.charAt(String.java:1512)
        at MarkdownParse.getLinks(MarkdownParse.java:22)
        at MarkdownParse.main(MarkdownParse.java:42)
      
```

**Despriction:** In this case, the bug is that there is no link. The failure-inducing file contains no link and has just text in it. When running the code with this input, it gives ```java.lang.StringIndexOutOfBoundsException``` since the file does not have any brackets and paranthesis to look for. For the fix, the updated code first checks if the file atleast has an open bracket.
