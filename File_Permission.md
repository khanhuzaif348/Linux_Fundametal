# **File Permission** 

.Permiossion devide into  threee categories .


**Read(r)**  - Allows the usr to view the contents of the file.

**Write(w)** - Allow Mdification 

**EXecute(x)** - Allows the user to execute it.

These  Permission apply to three different groups of users:

**Owner:** Who owns the File.

**Group :** A group of users who share common permission for the file .

**Others:** All other users who are not in the group.




Changing File Permission

chmod(change Mode): Change the File Permission. 
                    Two  ways to define permission 
                    1 - Symbolic Mode 2 - Numeric Mode 
Symbolic Mode - Permission using letters(r,w,x) and Operators(+,-,*).
Eg - chmod u+x File.txt - adds Execute permission for the owner.(u stands for user/Owner).
    chmod go-w file.txt - removes write permission from group and others(g for group , o for others)

    
Numeric Mode:  Permission are represented as a three  -digit number

Eg - Chmod 755 file.txt - grants rwx(7) to the owner , rx(5) to the grouup , rx(5) to others.


7 rwx(Read,write,Execute)         4 r--(read)         1 x(execute)

6 rw-(read,write)                 3 wx(write,execute) 0 ---(no permission) 

5 r-x(read,execute)               2 w-(write)                         



  
