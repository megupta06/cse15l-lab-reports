# Lab Report 5

## Using ```vimdiff``` to find the difference

To start you need to rename several files in the directory, and exclude them, due to some of them causing infinite loops. Moroever,I used ```vimdiff``` command to view differences between the results of both my markdown parser and the provided parser. I have picked out two tests to talk about in this report.

Use this command:
```
$ cd my-markdown-parser/
$ bash script.sh > results.txt

$ cd cse15ls2p22-markdown-parser/
$ bash script.sh > results.txt 

$ vimdiff my-markdown-parser/results.txt cse15lsp22-markdown-parser/results.txt
```
*********************************

## Discussing Testfiles with different outputs

* [test-files/22.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/22.md)

```
[foo](/bar\* "ti\*tle")
```

<img width="725" alt="Screen Shot 2022-06-04 at 5 33 40 PM" src="https://user-images.githubusercontent.com/103089880/172030101-7cc0256d-1841-4268-9338-69c250467c15.png">

My markdown parser (on the left) yielded the correct result. The problem with the other code is that after trimming, there's still space in the middle of the link, therefore failing the if condition. If the other special marks caused the link to be invalid, they can be excluded in similar ways as the backsticks.

<img width="725" alt="Screen Shot 2022-06-04 at 5 48 04 PM" src="https://user-images.githubusercontent.com/103089880/172030307-97c25b08-aedb-4d08-bdb5-819bca6a63a9.png">



* [test-files/32.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/32.md)

```
[foo](/f&ouml;&ouml; "f&ouml;&ouml;")
```


<img width="725" alt="Screen Shot 2022-06-04 at 5 34 02 PM" src="https://user-images.githubusercontent.com/103089880/172030351-9fbc286c-ae2e-4aa1-a86c-10c4e8256b7d.png">

My markdown parser (on the left) yielded the correct result. The way the code avoids invalid closing parenthesis/brackets in block codes can be also used to avoid potential errors caused by other symbols. The edits will be similar to what we made for the above test case. This a part of code, which can be modified to get the correct result.

<img width="725" alt="Screen Shot 2022-06-04 at 5 57 31 PM" src="https://user-images.githubusercontent.com/103089880/172030483-d7d8e490-d23d-4d22-86ee-47279f07685b.png">

