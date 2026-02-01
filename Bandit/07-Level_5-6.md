#### LEVEL 5 to LEVEL 6

**Target:**  
The password for the next level is located in a human-readable file inside the inhere directory. The file is exactly 1033 bytes in size and not executable.

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
Once we have entred bandit5, we will first type the command ls to list the files that is in the home directory.
``` bash
ls
```
<img width="230" height="66" alt="image" src="https://github.com/user-attachments/assets/4ce1225a-20a1-44bd-bf4a-199cb03d5de5" />

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

We find 3 types of files and from the information we need we find that:
1. data -> It does not show plain text  
2. OpenPGP Public Key -> Not human-readable text
3. ASCII text -> Plain human-readable text
Due to *-file07* is the only human-readable file, we will the cat command to display that file and start with ./ meaining that *-file07* is file in the current directory.

