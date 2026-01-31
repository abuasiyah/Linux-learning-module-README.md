#### LEVEL 4 to LEVEL 5

**Target:**  
TThe password for the next level is stored in the only human-readable file in the *inhere* directory.

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

**Execution:**  
Once we have entred bandit4, we will first type the command ls to list the files that is in the home directory.
``` bash
ls
```
<img width="230" height="66" alt="image" src="https://github.com/user-attachments/assets/4ce1225a-20a1-44bd-bf4a-199cb03d5de5" />

We found the *inhere* file. We will ow use the cd command to change the directory 
``` bash
cd inhere/
```
Once we are in the *inhere* directory, we will use ls again to list the file that are stored in the directory. We can see that we have 
