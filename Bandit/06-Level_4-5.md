#### LEVEL 4 to LEVEL 5

**Target:**  
The password for the next level is stored in the only human-readable file in the *inhere* directory.

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
<img width="161" height="38" alt="Screenshot 2026-02-01 193407" src="https://github.com/user-attachments/assets/28ca070b-3413-4315-b316-41382bcf5c93" />


We found the *inhere* file. We will now use the cd command to change the directory 
``` bash
cd inhere/
```
Once we are in the *inhere* directory, we will use ls again to list the file that are stored in the directory. We can see that we have 10 files.

<img width="339" height="43" alt="image" src="https://github.com/user-attachments/assets/ae80905a-a1e0-4e6f-9eee-949184c2acde" />

We can use the cat command and list the files one after the other, but that will be time-consuming. So we we will use the file command to identify the file types. We will use the ./* which means run all the files and directories in the current directory.

``` bash
file ./*
```

<img width="286" height="166" alt="image" src="https://github.com/user-attachments/assets/80136afb-2e12-43bf-86f5-d6432b110e5f" />

We find 3 types of files and from the information we need we find that:
1. data -> It does not show plain text  
2. OpenPGP Public Key -> Not human-readable text
3. ASCII text -> Plain human-readable text
Due to *-file07* is the only human-readable file, we will the cat command to display that file and start with ./ meaining that *-file07* is file in the current directory.

``` bash
cat ./-file07
```
<img width="322" height="29" alt="image" src="https://github.com/user-attachments/assets/d5baffac-32e1-49e8-831e-c08eef7d15a7" />

With this we have the password 

``` bash
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
We will now log out and log back in on bandit5 with this password
