# **Welcome to CSE15L !**
## 1. **Installing VS Code**
Go to the Visual Studio Code website [VSCode](https://code.visualstudio.com).




<img width="1440" alt="Screen Shot 2022-04-09 at 9 34 00 PM" src="https://user-images.githubusercontent.com/103089880/162601665-8ba63c63-026e-4747-b70b-c2f30865eb83.png">



Click download option and install the software. There are versions for all the major operating systems, like OSX (for Macs) and Windows (for PCs). When it is installed, you should be able to open a window that looks like this.



<img width="1440" alt="Screen Shot 2022-04-09 at 9 37 17 PM" src="https://user-images.githubusercontent.com/103089880/162601720-de48e308-c41e-4eca-879c-dc8d7319f586.png">


*Welcome to VS Code!*

*****************************************

## 2. **Remotely Connecting**

If you are on Mac, go to your terminal and enter the command with zz replaced by the letters in your course-specific account.

```
$ ssh cs15lsp22zz@ieng6.ucsd.edu
```

Since this is the first time you're connecting to the server, you should see the following.

```
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.

RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.

Are you sure you want to continue connecting (yes/no/[fingerprint])?

```

Type **yes** and press enter. You should see messages similar to these on your screen.



<img width="565" alt="Screen Shot 2022-04-01 at 6 18 28 PM" src="https://user-images.githubusercontent.com/103089880/162605793-f2a46866-1461-4552-8141-ba7c1f1f92dc.png">



Now your terminal is connected to a computer in the CSE basement, and any commands you run will run on that computer! 

*********************************

3. ## **Trying Some Commands**


Here are some specific useful commands to try:

* cd ~
* cd
* ls -lat
* ls -a
* ls <directory> where <directory> is /home/linux/ieng6/cs15lsp22/cs15lsp22abc, where the abc is one of the other group members’ username
* cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
* cat /home/linux/ieng6/cs15lsp22/public/hello.txt
  

  
Here is the example of me trying few commands.
  


<img width="565" alt="Screen Shot 2022-04-01 at 6 22 08 PM" src="https://user-images.githubusercontent.com/103089880/162606197-34be5493-169b-4ce4-8f4c-09a6624000b8.png">

 
 4. ## **Moving Files with scp**
 
  
  Create a file on your computer called WhereAmI.java and put the following contents into it:
  
  ```
  
  class WhereAmI {
  
  public static void main(String[] args) {
  
    System.out.println(System.getProperty("os.name"));
  
    System.out.println(System.getProperty("user.name"));
  
    System.out.println(System.getProperty("user.home"));
  
    System.out.println(System.getProperty("user.dir"));
  
  }
  
}

```
  
In the terminal from the directory where you made this file, run this command. Don't forget to replace zz with your account name!
  
``` 
scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/
```
  
You will be prompted for password just like ssh. Enter the password and log into ieng6 with ssh again.
  
This how my screen looked after entering password.
  
  
  <img width="651" alt="Screen Shot 2022-04-01 at 6 17 08 PM" src="https://user-images.githubusercontent.com/103089880/162606771-884b0437-de36-4bce-9a7f-4e0ec24b9a95.png">



Now, enter ```ls``` command in the terminal.
  
When run on the client computer, the output look something like this.

