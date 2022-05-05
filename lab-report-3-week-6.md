# Lab Report 3


## Copying directory to your ieng6 account




To copy the whole directory to the CSE server, you use the command ```scp -r *.java *.md lib/ cs15lsp22akh@ieng6.ucsd.edu:MarkdownParse```. This command securely copies all the .java, .md, and the lib folder recursively to a new folder on the server called markdown-parse.

*****************************************

## Logging into ieng6 account and running the tests for the repository




In this step, we first ssh onto the server with ```ssh cs15lsp22xxx@ieng6.ucsd.edu```, change directory to the folder we just securely copied with ```cd markdown-parse/```, and then compile and run the JUnit tests through``` javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java``` and ```java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest``` respectively.
*******************************************


## Combining scp 



