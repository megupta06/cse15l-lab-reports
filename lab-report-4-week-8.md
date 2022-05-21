# Lab Report 4

[My markdown-parse repository](https://github.com/megupta06/markdown-parser.git)


[Reviewed markdown-parse repository]()

## Snippet 1


```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```


It should produce:

```
[`google.com]
```

Added Test

<img width="767" alt="Screen Shot 2022-05-21 at 2 30 35 AM" src="https://user-images.githubusercontent.com/103089880/169645415-935804bd-b556-490f-b4a9-4d7fba27ec76.png">


 For my implementation, the corresponding output:
 
 
 
 <img width="1075" alt="Screen Shot 2022-05-21 at 2 46 05 AM" src="https://user-images.githubusercontent.com/103089880/169645938-63f4b4db-dff9-420a-af5b-8c4cf054979b.png">

 
 
 For the implementation reviewed, the corresponding output:




## Snippet 2


```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```

It should produce:
```
[a.com, a.com(()), example.com]
```

Added Test


<img width="766" alt="Screen Shot 2022-05-21 at 2 50 55 AM" src="https://user-images.githubusercontent.com/103089880/169646063-53f794f3-5ee5-466e-a78c-8a646b03021e.png">


 For my implementation, the corresponding output:
 
 
 <img width="1075" alt="Screen Shot 2022-05-21 at 2 50 07 AM" src="https://user-images.githubusercontent.com/103089880/169646035-f0618fd9-47a0-4add-b045-cc8489b82353.png">

 
 For the implementation reviewed, the corresponding output:







## Snippet 3


```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```


It should produce:

```
[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedu, https://cse.ucsd.edu/]
```

Added Test

<img width="775" alt="Screen Shot 2022-05-21 at 2 59 09 AM" src="https://user-images.githubusercontent.com/103089880/169646401-0d71634d-9772-4f69-bc6b-d12abc65f235.png">


 For my implementation, the corresponding output:
 
 
 <img width="1159" alt="Screen Shot 2022-05-21 at 2 58 22 AM" src="https://user-images.githubusercontent.com/103089880/169646366-8e3f1216-0a71-45d4-8255-38451cee4cd3.png">

 
 
 For the implementation reviewed, the corresponding output:



