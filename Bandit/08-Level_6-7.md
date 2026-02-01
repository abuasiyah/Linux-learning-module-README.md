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

we found to argumets that was benefital :  -user and -group

<img width="559" height="38" alt="Screenshot 2026-02-01 083700" src="https://github.com/user-attachments/assets/1b351076-0e22-434a-b2b7-ffff145f8508" />

<img width="559" height="38" alt="Screenshot 2026-02-01 083741" src="https://github.com/user-attachments/assets/3d4d8c4a-e505-4418-949f-37e1bee0e705" />

With this arguments, we will look for our targeted file 

``` bash
find  / -user bandit7 -group bandit6 -size 33c
```
This gives us a list of files with  "permission denied" 

<img width="752" height="568" alt="image" src="https://github.com/user-attachments/assets/2e5c4c29-7153-49de-ba35-5081fceb87cb" />

To only give us back files with permissions we type 2> /dev/null = hides any permission errors or access denials.

``` bash
find / -user bandit7 -group bandit6 -size 33c 2> /dev/null
```
<img width="627" height="32" alt="Screenshot 2026-02-01 132255" src="https://github.com/user-attachments/assets/9c60515c-1ef1-4f7f-b6d3-180f1c107596" />


``` bash
find -size 1033c
```
With this we have the password 

``` bash
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
We will now log out and log back in on bandit6 with this password
