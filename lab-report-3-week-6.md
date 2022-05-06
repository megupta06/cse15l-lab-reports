# Lab Report 3

## Streamlining ssh Configuration

To save too much of typing follow these instructions.
 To get started, try opening ```~/.ssh/config``` (on your computer, creating it if it doesn’t exist), and adding these lines
```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22zzz (use your username)
```
It should look like this in VSCode.

<img width="716" alt="Screen Shot 2022-05-05 at 7 39 27 PM" src="https://user-images.githubusercontent.com/103089880/167057844-75e9154a-7fb4-48da-93b5-eb098aeb1d4d.png">


Now, open file in VSCode and try this command.
```
ssh ieng6
```

<img width="716" alt="Screen Shot 2022-05-05 at 7 32 54 PM" src="https://user-images.githubusercontent.com/103089880/167057322-b04ba966-df21-422e-9ef4-f7c5f443149f.png">

Now try ```scp```  command to copy a file to your account using just the alias.
Command:
```
scp -r . ieng6:markdown-parse
```
Your terminal should look similar to this. 

<img width="716" alt="Screen Shot 2022-05-05 at 7 33 56 PM" src="https://user-images.githubusercontent.com/103089880/167057404-3da68dbc-9cb9-4c5a-a732-f6651df5cc6d.png">


**********************************************************


## Setup Github Access from ieng6





















****************************************************************************


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








