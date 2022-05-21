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




 For my implementation, the corresponding output:
 
 
 For the implementation reviewed, the corresponding output:







## Snippet 3









 For my implementation, the corresponding output:
 
 
 For the implementation reviewed, the corresponding output:



