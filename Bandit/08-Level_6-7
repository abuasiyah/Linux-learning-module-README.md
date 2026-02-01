#### LEVEL 5 to LEVEL 6

**Target:**  
The next level’s password is stored somewhere on the server in a 33-byte file owned by user bandit7 and group bandit6.

**Information:**  
*Commands we may need to solve this level*

ls – Lists files and directories
Example: ls -la

cd – Changes directory
Example: cd /var/log
.
cat – Displays file contents
Example: cat readme.txt

file – Identifies a file’s type
Example: file script.sh

du – Shows disk usage
Example: du -sh folder/

find – Searches for files/directories
Example: find /home -name "*.txt"

grep – Searches text for a pattern
Example: grep "password" file.txt

**Execution:**  
Once we have entred bandit6, we will first type the command ls to list the files that is in the home directory.
``` bash
ls
```
ls didn't give us any output, meaning that there is no file. so this is the next steps we took:
1.type pwd to prints the current working directory
2.changed to home directory as home should have more directories to look into
3. ls to list files and directories in the home directory
3.Typed find size 33c and we found out that several 33 bytes size file




man find

/ = to type your looking for 

found -user and -group

We found the *inhere* file. We will now use the cd command to change the directory 
``` bash
cd inhere/
```
Once we are in the *inhere* directory, we will use ls again to list the file that are stored in the directory. We can see that we have 20 files.

<img width="479" height="74" alt="Screenshot 2026-02-01 073739" src="https://github.com/user-attachments/assets/e6fbc787-4bfa-411c-b262-6481b9d1f0a4" />


We can use the cat command and list the files one after the other, but that will be time-consuming. knowing i had to find a specific size a typed man find to look for someting that will help us look for size of a file.
``` bash
man find
```
Then we type / and type your looking for, so we type *size* to see if *find* manual has something that looks for a specific size. We can look for size.

<img width="544" height="264" alt="Screenshot 2026-02-01 065422" src="https://github.com/user-attachments/assets/c0bda36e-942d-453d-92b8-35a128a87bb5" />

``` bash
find -size 1033c
```
<img width="336" height="29" alt="image" src="https://github.com/user-attachments/assets/9016c93f-aba4-41cd-8cb8-a445faa128eb" />

We have now found 1 file with that file size. we will now use cat to display that file

``` bash
cat ./maybehere07/.file2
```
<img width="383" height="32" alt="image" src="https://github.com/user-attachments/assets/a3d10e5e-ab84-4df7-b434-8c2b8f23a7c1" />

With this we have the password 

``` bash
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
We will now log out and log back in on bandit6 with this password
