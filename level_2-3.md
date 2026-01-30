#### LEVEL 1 to LEVEL 2

**Target:**  
The password for the next level is stored in a file called **--spaces in this filename--** located in the home directory

**Information:**  
*Commands we may need to solve this level*

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
Once we have entred bandit2, we will first type the command ls to list the files that is in the home directory 
``` bash
ls
```
we found the **-** file. we can't simply display the content of the file using cat and there are two separate reasons for this:

1️. Spaces split arguments:
Bash thinks we trying to open four different files, not one due to the spaces.
2.**--** has special meaning

-- tells a command:

“Stop processing options after this point”

In bash, spaces separate arguments
cat ./-
```



With this we have the password 

``` bash
 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
We will now log out and log back in on bandit2 with this password
