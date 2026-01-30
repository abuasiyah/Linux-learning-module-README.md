#### LEVEL 0 to LEVEL 1
**Target:** 
The next level’s password is in the *readme* file in the home directory. Use it to SSH into bandit1 on port 2220, and repeat this process for each level.

**Information:**
Commands we may need to solve this level

ls – Lists files and directories
Example: ls -la

cd – Changes directory
Example: cd /var/log

cat – Displays file contents
Example: cat readme.txt

file – Identifies a file’s type
Example: file script.sh

du – Shows disk usage
Example: du -sh folder/

find – Searches for files/directories
Example: find /home -name "*.txt"


**Execution:**
we first type the command ls to list the files that is in the home directory 
``` bash
ls
```
we found the *readme* file. To display the content of the file we type the command cat followed by the file
``` bash
cat readme
```
<img width="667" height="192" alt="image" src="https://github.com/user-attachments/assets/1142562e-07a8-4276-bdf6-1653306ea3ad" />

With this we get the password 

``` bash
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```
We will now log out and log back in on bandit1 with this password
