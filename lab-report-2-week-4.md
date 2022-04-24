# Lab Report 2

## First Code Change

**Failure:** When there is an image with the links in the same file

**Screenshot of code change:**


<img width="835" alt="Screen Shot 2022-04-24 at 2 14 39 PM" src="https://user-images.githubusercontent.com/103089880/164996873-848870ca-c4b2-4378-af02-776d9a8225b8.png">



**Test file for failure-inducing input:**  [Test file](https://github.com/megupta06/markdown-parser/blob/6eb16e74e7d2c49f11b34ed1c2e0d6b9a6ad27d7/test-file2.md)


**Failure-inducing optput:**  ```[img123.html, some-google.html]```



**Despriction:**  In this case, the bug is that markdown parser would consider the image path as a link because the syntax of adding an image and link is the same. Both of the syntax include brackets and paranthesis. The only difference is that the syntax for adding image include '!' in the beginning. So when we run the code using failure code we get image path with the link as the output. The fixed code catches '!' and differentiates the images path and the link and returns only the link.


****************************

## Second Code Change

**Failure:** When open paranthesis is not after close bracket


**Screenshot of code change:**

<img width="835" alt="Screen Shot 2022-04-24 at 2 16 59 PM" src="https://user-images.githubusercontent.com/103089880/164996958-8c542ea3-3492-4ddd-bce1-de73a5a373bd.png">


**Test file for failure-inducing input:** [Test file](https://github.com/megupta06/markdown-parser/blob/bffbfb0db3c81a5cbd3576dce4da571f6de1b023/test-file3.md)

**Failure-inducing optput:** ```[page.com]```


**Despriction:** 

*************************************


## Third Code Change

**Screenshot of code change:**

**Test file for failure-inducing input:** 

**Failure-inducing optput:**


**Despriction:** 
