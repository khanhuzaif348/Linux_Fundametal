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


File Permission Representation 

The first charcter indicate the file type:

. for a regular file
d for a directory 
| for a symbolic link 


The next nine characters represent the permission for the owner , group , and Others.
Owner Permission : First 3 character like rwx : - Owner has read , write , and execute permission .

Group permission : (Next three chracter) : like : r-x means the group has read , not write , execute 

Other permission : - like r-- maens others can read file but not another permission for other 



 # **changing File Permission** 

chmod(Change Mode) 

CHange the user permission  . These 2 type 

Symbolic Mode : - Specifies permissions using letters (r,w,x) and Operator (+,-,=).

Example : **chmod u+x file.txt** - adds execute permission for the owner (u stands for user/owner).
Example : chmod go-w file.txt - removes write permisssion from group and others (g for group , o for Others)

**Numeric Mode** : Permission  are represented as a three digit number .

**Example :** chmod 755 file.txt -  grant  rwx(7) to the owner,rx(5) to the group , and rx(5) to others.

7  rwx      4    r--        1 x 

6  rw-       3  wx           0 ---

5 r-x        2  w-




# **Pipe  & Filter** 


A pipe is a special operator (|) in Linux thst allows you to connaect the output of one command to the input of another .

It enables the o/p from one program to be used as the input bfor another 
   ,creating pipeline of commands . 
   
pipes are useful for chaining multiple commands together in a single line , making it easier to perform complex tasks .

**Filter :** 

A filter is a command that process input data and produces Output  Filters takes data from  standerd input(stdin),
Perform operation on it  .
and send the result to standerd o/t (stdout) .
FIlters are commonly used in combinationb with pipes to process and transform data . 

**Few common filter as below** 


**grep**  -   searches for patterns in text .

**uniq**  -   Removes duplicate lines from sorted data .

**awk**   -   A powerfull text processing tool .

**sort**  -   Sorts Data .

**sed**   -  A stream editor used for text transformations.

**cut**   -  Extracts specific columns from input 

**tr**     - Translate or deletes characters .


# **pipes   : Chaining of cmd** 

pipes allows you to combine multiple cmd together ,
For Example yuo can filter the result of one cmd using another command without needing to store intermediate data in  files .

Eg 1 : Using grep with a pipe  :            **ps aux | grep firefox**

Eg 2 :  Using ls and sort with a pipe :     **ls -l |sort -k 5 -n**

Eg 3 : COmbining cat ,grep ,and sort :      **cat file.txt |grep'error' | sort**

Eg 4 : Using ps ,grep ,and awk with pipes : **ps aux | grep 'python' |awk'{print $1,$3,$11}'**

Eg 5 : Redirecting output to a file :       **ps aux |grep 'python'>python_process.txt**

Eg 6 : Appending output to a file :         **ps aux |grep 'python'>>python_process.txt**


# **Process**

**In Linux , System processes are managed using various commands that help you view , monitor,and control the running processes on your system . Here are some useful commands  for manageing system processes .**

**ps(Process status) :** Display running in current procerss . 

    ps - shows processes running in the current shell. 
    ps aux - Lists all  processes running on the system (regardless of the user).
    ps -ef   - Displays all proceses with detailed information .
    ps aux | grep <process_name> -Searches for a specific process by name 

    
top :  Displays a dynamic ,real time view of system process.
htop : showing system processes in a graphical interfacce .
pgrep : finds the process IDs (PIDs) of processes matching a given name or other criteria .
kill : Terminates a process by sending to it .
killall : kills proceses by name instead of byb PID .
nice : Statrs a process with a specific priority.
renice : Changes the priority of and already running process .

Isof : Displays a list of all open files and the processes that opened them .
strace : Traces system calls and signals of a process . 
uptime : Shows how long the system has been running , along with the load averages(system load)
free : Displays memory usage information , useful for monitoring processes that may be consuming lage amounts of memory .

























									
