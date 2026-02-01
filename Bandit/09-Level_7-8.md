#### LEVEL 7 to LEVEL 8

**Target:**  
The password for the next level is stored in the file data.txt next to the word millionth

**Information:**  
*Commands we may need to solve this level*

man – Displays the manual page for a command
Example: man ls

grep – Searches text for matching patterns
Example: grep "error" file.txt

sort – Sorts lines of text
Example: sort names.txt

uniq – Filters or reports repeated lines
Example: uniq file.txt

strings – Extracts readable text from binary files
Example: strings binaryfile

base64 – Encodes or decodes Base64 data
Example: base64 -d file.txt

tr – Translates or deletes characters
Example: tr 'a-z' 'A-Z'

tar – Archives multiple files into one
Example: tar -cvf archive.tar folder/

gzip – Compresses files using gzip
Example: gzip file.txt

bzip2 – Compresses files using bzip2
Example: bzip2 file.txt

xxd – Creates a hex dump of a file
Example: xxd file.bin

**Execution:**  
Once we have entred bandit6, we will first type the command ls to list the files that is in the home directory.
``` bash
ls
```
We found the *data.txt* file. As we know that the password is next to the millionth word, we will use the grep command to searches the text millionth in the *data.txt" file

``` bash
grep  "millionth" data.txt
```
<img width="391" height="29" alt="image" src="https://github.com/user-attachments/assets/0f6dbf6c-1c9d-409e-b0c9-4d5bcb6f17ad" />

With this we have the password 

``` bash
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
We will now log out and log back in on bandit8 with this password

