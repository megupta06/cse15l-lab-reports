# Lab Report 3


## Copy whole directories with ```scp -r```

 To copy the whole directory to the CSE server, you use the command

``` 
scp -r *.java *.md lib/ cs15lsp22@ieng6.ucsd.edu:markdown-parse
```
This command securely copies all the ```.java```, ```.md```, and the ```lib``` folder recursively to a new folder on the server called ```markdown-parse```.


<img width="716" alt="Screen Shot 2022-05-05 at 6 04 05 PM" src="https://user-images.githubusercontent.com/103089880/167050322-769c1165-4333-4a64-bce2-3d2e8e026f69.png">


Now, we first ```ssh``` onto the server with ```ssh cs15lsp22xxx@ieng6.ucsd.edu``` and log into ```ieng6 ```account, change directory to the folder we just securely copied with ```cd markdown-parse/```, and then compile and run the JUnit tests.

Commands for compiling and running the test:

```
javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java 
java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest
```


<img width="716" alt="Screen Shot 2022-05-05 at 5 43 17 PM" src="https://user-images.githubusercontent.com/103089880/167050333-9871e436-db96-44d0-84c4-b75ba97c47cf.png">




 In this final step, we're combining the above two steps of copying the files over to the server and running the tests in one command.
 The  command is:
 ```
 scp -r *.java *.md lib/ cs15lwi22amm@ieng6.ucsd.edu:~/markdown-parse; ssh cs15lsp22akh@ieng6.ucsd.edu "cd markdown-parse; /software/CSE/oracle-java-se-14/jdk-14.0.2/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; /software/CSE/oracle-java-se-14/jdk-14.0.2/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest"
 ```

<img width="716" alt="Screen Shot 2022-05-05 at 5 46 08 PM" src="https://user-images.githubusercontent.com/103089880/167050342-4c602db5-41ea-48c8-b02d-81d391bd3be4.png">








