#### LEVEL 3 to LEVEL 4

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
Once we have entred bandit3, we will first type the command ls to list the files that is in the home directory.
``` bash
ls
```
