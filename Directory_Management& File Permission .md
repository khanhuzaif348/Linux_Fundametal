# **Directory MAnagement**

**Root Directorry(\)**

  **Topmost directory in Linux File System.
  All other directories and files are nested  benaeth this directory
  The root directory is the starting point of the entire Linux filesystem.**

**Common Directories in Linux** 

 /bin(Binary)              /usr(User system resources)          /lib
 /home 		                 /tmp				                          /sbin
/var(variable)             /dev			                            /etc


**Absolute vs Relative PAths**
 
**Absolute paths** : Specifies the complete path to a file or directory from the root directory.It always begins with **/.**

**Relative path** :  Specifies the path to a file or directory relative to the current directory you are in . It does not begins with /.
 
# **Directory Management - Commands** 


**ls directoryName** - This will display list of files or sub-directory present in directory .

**mkdir directoryNAme**  - To create a new Directory.To create more then one Directory.

**mkdir -p/parentsDir/childdir :** If the parent directory does nor exist.this cmd will help you to create necessary parent and child directory .

**rmdir Dirname** - This will help you to delete dir . To remove a Dir ,make sure it is emty 

**mv oldDir NewDir** - This will help you to move dir to anoher dir 

**cd dirName** - This will change the dir of the current working console.

**cd ..** - This will change the current dir to immediate parent Dir . 









# **File Permission : UNderstanding file permissions** 

Permission are devided into 3 categories .

**Read(r)** : Only view contents

**write(w)** : allows the user modify the contents of the file .

**Execute(x)** : Allows the user to execute the file .


These permission devidde three groups of user :



**Owner** : The user who owns the file or Dir.

**group** : A group of users who share common  permission for the file .

**Others** : All other users who are not the owner or in the group .




									
