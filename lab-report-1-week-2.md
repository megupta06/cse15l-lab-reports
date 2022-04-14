# **Welcome to CSE15L !**
## 1. **Installing VS Code**
Go to the Visual Studio Code website [VSCode](https://code.visualstudio.com).




<img width="1440" alt="Screen Shot 2022-04-09 at 9 34 00 PM" src="https://user-images.githubusercontent.com/103089880/162601665-8ba63c63-026e-4747-b70b-c2f30865eb83.png">



Click download option and install the software. There are versions for all the major operating systems, like OSX (for Macs) and Windows (for PCs). When it is installed, you should be able to open a window that looks like this.



<img width="1440" alt="Screen Shot 2022-04-09 at 9 37 17 PM" src="https://user-images.githubusercontent.com/103089880/162601720-de48e308-c41e-4eca-879c-dc8d7319f586.png">


*Welcome to VS Code!*

*****************************************

## 2. **Remotely Connecting**

If you are on Mac, go to your terminal and enter the command with ``zz`` replaced by the letters in your course-specific account.

```
$ ssh cs15lsp22zz@ieng6.ucsd.edu
```

Since this is the first time you're connecting to the server, you should see the following.

```
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.

RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.

Are you sure you want to continue connecting (yes/no/[fingerprint])?

```

Type ```yes``` and press enter. You should see messages similar to these on your screen.



<img width="565" alt="Screen Shot 2022-04-01 at 6 18 28 PM" src="https://user-images.githubusercontent.com/103089880/162605793-f2a46866-1461-4552-8141-ba7c1f1f92dc.png">



Now your terminal is connected to a computer in the CSE basement, and any commands you run will run on that computer! 

*********************************

## 3. **Trying Some Commands**


Here are some specific useful commands to try:

* ```cd ~```
* ```cd```
* ```ls -lat```
* ```ls -a```
* ```ls <directory>``` where ```<directory>``` is ```/home/linux/ieng6/cs15lsp22/cs15lsp22abc```, where the ```abc``` is one of the other group members’ username
* ```cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/```
* ```cat /home/linux/ieng6/cs15lsp22/public/hello.txt```
  

  
Here is the example of me trying few commands.
  


<img width="565" alt="Screen Shot 2022-04-01 at 6 22 08 PM" src="https://user-images.githubusercontent.com/103089880/162606197-34be5493-169b-4ce4-8f4c-09a6624000b8.png">

  *********************************************************
 
## 4. **Moving Files with scp**
 
  
  
  To learn how to  send files from your computer to server, create a file on your computer called ```WhereAmI.java``` and put the following contents into it:
  
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
  
In the terminal from the directory where you made this file, run this command. Don't forget to replace ```zz``` with your account name!
  
``` 
scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/
```
  
You will be prompted for password just like ssh. Enter the password and log into ```ieng6``` with ```ssh``` again.
  
This is how my screen looked after entering password.
  
  
 <img width="595" alt="Screen Shot 2022-04-01 at 6 17 08 PM" src="https://user-images.githubusercontent.com/103089880/162607590-8955b8c6-0f7d-4a96-8854-5006b420a887.png">


  
When run on the client computer, the output look something like this.
  
  
  
  <img width="552" alt="Screen Shot 2022-04-01 at 6 42 46 PM" src="https://user-images.githubusercontent.com/103089880/162607532-2045518e-c96a-42f0-b3ac-cb9030b40e12.png">

  
  
Login to your server and type ```ls``` in the terminal. Then run the java file in the server and you will see different set of results.
  
  
  <img width="559" alt="Screen Shot 2022-04-01 at 6 34 09 PM" src="https://user-images.githubusercontent.com/103089880/162607363-1e5e22a9-3b3f-46e0-8399-79fe967a4595.png">
  
  ***********************************************************
  
  
## 5. **Setting an SSH Key**
  
  
I know you must be tired by now by entering password multiple times to log in or run ```scp``` but not anymore. There is a solution to it- ```ssh``` keys!
 
Here’s what you should run to set this up:
  
On your client, enter the command
  ```
  $ ssh-keygen
  ```
  
  Your screen should look something like this.
  
  <img width="570" alt="Screen Shot 2022-04-10 at 12 44 01 AM" src="https://user-images.githubusercontent.com/103089880/162608039-eef482df-5705-4c35-9e5f-7b91da2a93be.png">

  
  You have now generated a public and private key. The public key will have to be sent to the server. Now you need to copy the public key to the ```.ssh``` directory of your user account on the server. For that enter the following command on your server.

  ```
  $ mkdir .ssh
  $ <logout>
```
  
  Now, go back on clinet and enter the command using your username and the path you saw in the command above.

  
  ```
  $ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys
  ```
  Now, you should be able to ```ssh``` or ```scp``` from this client to the server without entering your password!

************************************************************
  
## 6. Optimizing Remote Running
  
  You will agree that it was a lot of complex work to do with a lot of steps! But this task of local editing file , then copying it to the remote server and running it can be made easier!

  * You can use upper arrow key to run the last command!
  
  * You can use semicolons to run multiple commands on the same line in most terminals.
  
  * Moreover, you can write a command in quotes at the end of an ```ssh``` command to directly run it on the remote server.
  
    Here is an example to try
  
  ```
  $ ssh cs15lsp22zz@ieng6.ucsd.edu "ls"
  ```
  
  <img width="570" alt="Screen Shot 2022-04-10 at 1 09 03 AM" src="https://user-images.githubusercontent.com/103089880/162608950-27b76216-4da7-4828-98e0-8edd019ef496.png">

  Isn't it fun! you did two steps in one using this command.
  
  
  **************************************
 
  **_Hope you had a good time learning it!_**
  
 
  
  
  
  

