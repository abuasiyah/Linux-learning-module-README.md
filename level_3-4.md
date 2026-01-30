#### LEVEL 3 to LEVEL 4

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
<img width="230" height="66" alt="image" src="https://github.com/user-attachments/assets/4ce1225a-20a1-44bd-bf4a-199cb03d5de5" />

We found the *inhere* file. We will ow use the cd command to change the directory 
``` bash
cd inhere/
```
we then do ls to check a file, but nothing comes up meaning that the file we are looking for maybe hidden

<img width="256" height="43" alt="image" src="https://github.com/user-attachments/assets/4e794470-9bf8-44ed-ac3f-10b2b3274d35" />

So we put -a after the ls command to show ay hidden files. -a means all, including hidden files

``` bash
ls -a
```
<img width="258" height="31" alt="image" src="https://github.com/user-attachments/assets/3cc06bc7-933b-4dbe-a4bc-eda2427913ee" />
we going to use the cat command to display the **...Hiding-From-You** file and put ./ before it

We are explicitly telling the shell:  
**./ →** look in the current directory

**...Hiding-From-You →** treat this as a literal filename 

``` bash
cat ./...Hiding-From-You
```
<img width="382" height="28" alt="image" src="https://github.com/user-attachments/assets/8bc574a8-ddcc-427e-950b-82c742442f82" />


With this we have the password 

``` bash
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
We will now log out and log back in on bandit4 with this password
