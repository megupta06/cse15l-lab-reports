# Lab Report 3


## Copying your whole markdown-parse directory to your ieng6 account




To copy the whole directory to the CSE server, you use the command ```scp -r *.java *.md lib/ cs15lsp22xxx@ieng6.ucsd.edu:markdown-parse```. This command securely copies all the .java, .md, and the lib folder recursively to a new folder on the server called markdown-parse.

*****************************************

## Logging into your ieng6 account and compiling and running the tests for your repository




In this step, we first ssh onto the server with ```ssh cs15lsp22xxx@ieng6.ucsd.edu```, change directory to the folder we just securely copied with ```cd markdown-parse/```, and then compile and run the JUnit tests through``` javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java``` and ```java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest``` respectively.
*******************************************


## Combining scp, ;, and ssh to copy the whole directory and run the tests in one line


In this final step, we're combining the above two steps of copying the files over to the server and running the tests in one command.

The full command is
```
scp -r *.java *.md lib/ cs15lwi22amm@ieng6.ucsd.edu:~/markdown-parse; ssh cs15lwi22amm@ieng6.ucsd.edu "cd markdown-parse; /software/CSE/oracle-java-se-14/jdk-14.0.2/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; /software/CSE/oracle-java-se-14/jdk-14.0.2/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest"
```
