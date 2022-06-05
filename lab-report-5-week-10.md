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


