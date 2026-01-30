#### LEVEL 1 to LEVEL 2

**Target:**  
The password for the next level is stored in a hidden file in the *inhere* directory.

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
Once we have entred bandit3, we will first type the command ls to list the files that is in the home directory 
``` bash
ls
```
we found the **-** file. we can't simply display the content of the file using cat as it will think we want to read input from the keyboard, not open a file. so for us to open the file we will type this command 
``` bash
cat ./-
```
We are explicitly telling the shell:

**./ →** look in the current directory

**- →** treat this as a literal filename 

<img width="374" height="152" alt="Screenshot 2026-01-30 200237" src="https://github.com/user-attachments/assets/1dc1f6e6-c456-43bc-b042-0b4f061d6f1e" />

With this we have the password 

``` bash
 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
We will now log out and log back in on bandit2 with this password
