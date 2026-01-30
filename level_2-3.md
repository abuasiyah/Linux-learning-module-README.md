#### LEVEL 2 to LEVEL 3

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

How to make it work

We will put double quotation on this filename. This will preserve the spaces and most special characters.

``` bash
cat "./--spaces in this filename--"
```
<img width="450" height="123" alt="image" src="https://github.com/user-attachments/assets/46199021-f86c-4a23-8499-ec4c8a8e4e78" />

With this we have the password 

``` bash
 MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```
We will now log out and log back in on bandit3 with this password
