- [1. Introduction](#1-introduction)
  - [1.1. Scope](#11-scope)
  - [1.2. Background](#12-background)
  - [1.3. Purpose](#13-purpose)
  - [1.4. Next steps](#14-next-steps)
- [2. Basics](#2-basics)
  - [2.1. Common commands](#21-common-commands)
  - [2.2. Shortcuts](#22-shortcuts)
    - [2.2.1. Navigation](#221-navigation)
    - [2.2.2. Editing](#222-editing)
    - [2.2.3. Recall from history](#223-recall-from-history)
- [3. Streams, Pipes and Redirects](#3-streams-pipes-and-redirects)
  - [3.1. Streams](#31-streams)
  - [3.2. Redirections](#32-redirections)
    - [3.2.1. Types](#321-types)
    - [3.2.2. Additional Examples](#322-additional-examples)
      - [3.2.2.1. Send standard output to sout.txt and standard error to serr.txt](#3221-send-standard-output-to-souttxt-and-standard-error-to-serrtxt)
      - [3.2.2.2. Send standard output and standard error streams to the same file sone.txt](#3222-send-standard-output-and-standard-error-streams-to-the-same-file-sonetxt)
      - [3.2.2.3. Ignore both standard input and output](#3223-ignore-both-standard-input-and-output)
  - [3.3. Pipe](#33-pipe)
  - [3.4. xargs](#34-xargs)
  - [3.5. tee](#35-tee)
- [4. Filename expansion](#4-filename-expansion)
- [5. Job control](#5-job-control)
- [6. Process handling](#6-process-handling)
  - [6.1. difference between ```ps``` and ```jobs```](#61-difference-between-ps-and-jobs)
- [7. Quoting](#7-quoting)
- [8. Basic file management](#8-basic-file-management)
  - [8.1. list directory ```ls```](#81-list-directory-ls)
  - [8.2. show file contents](#82-show-file-contents)
  - [8.3. file handling](#83-file-handling)
    - [8.3.1. copy](#831-copy)
    - [8.3.2. move or rename](#832-move-or-rename)
    - [8.3.3. delete](#833-delete)
    - [8.3.4. file linking](#834-file-linking)
    - [8.3.5. change directory](#835-change-directory)
    - [8.3.6. display disk usage](#836-display-disk-usage)
    - [8.3.7. file ownership and permissions](#837-file-ownership-and-permissions)
- [9. Special shell variables](#9-special-shell-variables)
- [10. Exit codes](#10-exit-codes)
- [11. ```grep```](#11-grep)
  - [11.1. Useful ```grep``` options](#111-useful-grep-options)
    - [11.1.1. Examples](#1111-examples)
  - [11.2. Regular expression in grep](#112-regular-expression-in-grep)
  - [11.3. Examples](#113-examples)
- [12. ```find```](#12-find)
  - [12.1. Examples](#121-examples)
- [13. ```sed``` filter and transform text](#13-sed-filter-and-transform-text)
  - [13.1. Overview](#131-overview)
  - [13.2. Examples](#132-examples)
  - [13.3. Grouping](#133-grouping)
    - [13.3.1. Grouping Examples:](#1331-grouping-examples)
  - [13.4. Hold Buffer](#134-hold-buffer)
    - [13.4.1. Example](#1341-example)
- [14. ```awk```](#14-awk)
  - [14.1. Actions](#141-actions)
  - [14.2. Special variables](#142-special-variables)
  - [14.3. Examples](#143-examples)
- [15. Command substitution](#15-command-substitution)
  - [15.1. Examples](#151-examples)
- [16. Process substitution](#16-process-substitution)
  - [16.1. Examples:](#161-examples)
- [17. Subshell](#17-subshell)
- [18. Command grouping](#18-command-grouping)
  - [18.1. using parentheses](#181-using-parentheses)
  - [18.2. using curly braces](#182-using-curly-braces)
- [19. Text editing with ```cut```, ```paste``` and ```join```](#19-text-editing-with-cut-paste-and-join)
  - [19.1. ```cut```](#191-cut)
    - [19.1.1. Examples](#1911-examples)
  - [19.2. ```paste```](#192-paste)
    - [19.2.1. Examples](#1921-examples)
  - [19.3. ```join```](#193-join)
    - [19.3.1. Examples](#1931-examples)
- [20. Aliases](#20-aliases)
  - [20.1. useful aliases](#201-useful-aliases)
- [21. Functions](#21-functions)
  - [21.1. useful functions](#211-useful-functions)
- [22. sort](#22-sort)
- [23. uniq](#23-uniq)
- [24. Conditions](#24-conditions)
  - [24.1. If else](#241-if-else)
  - [24.2. Short circuiting](#242-short-circuiting)
    - [24.2.1. example](#2421-example)
- [25. Loops](#25-loops)
  - [25.1. while loops](#251-while-loops)
    - [25.1.1. example](#2511-example)
  - [25.2. for loops](#252-for-loops)
    - [25.2.1. example](#2521-example)
- [26. ssh](#26-ssh)
- [27. curl](#27-curl)
  - [27.1. Examples](#271-examples)
  - [27.2. handling REST calls](#272-handling-rest-calls)
    - [27.2.1. GET](#2721-get)
    - [27.2.2. POST](#2722-post)
    - [27.2.3. PUT](#2723-put)
    - [27.2.4. DELETE](#2724-delete)
- [28. wget](#28-wget)
  - [28.1. Examples](#281-examples)
- [29. One liners](#29-one-liners)
- [30. Further reading](#30-further-reading)
- [31. Change History](#31-change-history)


# 1. Introduction
## 1.1. Scope
- This document will mainly focus on things that are usually done in the command line
- The focus is on tools and techniques for one shot adhoc tasks. 
- Most of the things in the document can be applied to shell scripting. However, shell scripting is not the focus of this document
- This document is for Linux/Unix 

## 1.2. Background
- I am documenting things I learnt and am still learning
- I had multiple files with random snippets.
- I decided to organize the mess into a single piece, so that I can efficiently look up things
- I cannot claim to be an expert in command line. 

## 1.3. Purpose
- The document will not help anyone become an expert. 
- However, it may help people become effective.
- I have kept the document concise. I skipped over details that I never used much and can be looked up later in the internet.
- I have focused on concrete examples of common or interesting use cases.

## 1.4. Next steps
- rephrase unclear material
- correct incorrect material
- add missing material
- add further reading material
- Contributions are welcome

# 2. Basics
## 2.1. Common commands

command     | description
--          | --
```man```   | get help on commands. e.g.<br>```man date```
```date```  | gives the date and time
```cal```   | shows the calender
```ls```    | tells which files are present in the current working         directory<br>when a *-l* option is used, the command returns owner, size, date of file, persissions, etc.
```cat```   | shows contents of a file
```cp```    | copy a file
```mv```    | move a file
```diff```  | lists differences between 2 files
```rm```    | removes file 
```grep```  | find occurences of strings in one or more files
```pwd```   | print the present working directory's name
```cd```    | changes the current directory 

## 2.2. Shortcuts

### 2.2.1. Navigation
keyboard shortcut | description
---               |---
Ctrl+A            | move the cursor to the start of the line
Ctrl+E            | move the cursor to the end of the line
Alt+F             | move the cursor forward by one word
Ctrl+F            | move the cursor forward by one character
Alt+B             | move the cursor backward by one word
Ctrl+B            | move the cursor backward by one charater
Ctrl+XX           | toggle the cursor's position between the current position and the previous position
 
### 2.2.2. Editing
keyboard shortcut | description
---               |---
Ctrl+U            | cut all the characters to the left of the cursor
Ctrl+K            | cut all the characters to the right of the cursor
Ctrl+W            | cut one word to the left of the cursor
Ctrl+H            | cut one character to the left of the cursor
Alt+D             | cut one word to the right of the cursor
Ctrl+D            | cut one character to the right of the cursor
Ctrl+Y            | paste the cut characters
Ctrl+_            | undo the last deletion
Tab               | complete arguments or list all available commands

### 2.2.3. Recall from history
keyboard shortcut | description
---               |---
Crtl+R            | search the command history
Ctrl+G            | abort
Ctrl+P/UP         | the previous command in the history
Ctrl+N/DOWN       | the next command in the history

# 3. Streams, Pipes and Redirects
## 3.1. Streams
A linux shell's inputs and outputs are sequence of characters called streams. There are three standard I/O streams:

name  | description                    |file descriptor
---   |---                             |---
stdout| displays output from commands  | 1
stderr| displays error from commands   | 2
stdin | provides inputs to commands    | 0
 
## 3.2. Redirections

### 3.2.1. Types
Input and output redirections are done using angular brackets (<>)

Bracket type   | description
---            | ---
\>             | send stream to a file. E.g. <br> ```ls a > o.txt```
\>>            | append stream to a file. E.g. <br> ```ls b >> o.txt```
\>&            | write into stream. E.g. <br> ```ls c > o2.txt 2>&1```
<              | receive stream from a file. E.g. <br> ```wc < o.txt```
<<             | embed the text that will be fed to a command within the script<br> Example<br> ```cat << EOF > output.txt``` <br> ```line 1```  <br> ```line 2``` <br> ```line 3``` <br> ```EOF``` <br> ```echo done```

### 3.2.2. Additional Examples
#### 3.2.2.1. Send standard output to sout.txt and standard error to serr.txt
```command1 > sout.txt 2> serr.txt```
#### 3.2.2.2. Send standard output and standard error streams to the same file sone.txt
```command1 > sone.txt 2>&1```

OR

```command1 &> sone.txt```

#### 3.2.2.3. Ignore both standard input and output
```command1 &> /dev/null```

***/dev/null** is a null device file. This will discard anything written to it, and will return EOF on reading.*

## 3.3. Pipe
Piping can redirect the standard output of one command to the input of another command.

```command1 | command2 paramater1 | command3 parameter1 parameter2 | command4```

Examples:

- Print file contents only once. remove duplicate records:<br> ```sort file1 | uniq```

- print 5 most frequently used commands <br>
```history | awk '{a[$2]++}END{for(i in a){print a[i] " " i}}' | sort -rn  | head -5```

- print the file types and their frequencies <br> ```ls | rev | cut -f1 -d'.' | rev | sort | uniq -c | sort -n```
  
## 3.4. xargs
- short for extended arguments
- some commands can take arguments from both standard input and as command-line arguments.
-  however, there are some commands that cannot take input from standard input. They accept inputs only from arguments. For these commands we need to use args.
-  xargs converts input from standard input into arguments to a command.
-  divides the arguments to a permitted number and runs the command repeatedly over each greoup of arguments.
-  using -n option, the number of arguments per command can be specified. 
   ```find . | xargs -n1 basename```
-  in order to assign the std input to a placeholder , use ```-I{}```. the placeholder is usually used when we want to place the std input in the middle of a command<br>
   ```ls | xargs -I{} echo {} file is found```

Examples:
- print the number lines/words/characters in the files in a directory<br>
  ```ls | wc```
- print the file types and their frequencies <br>
  ```find . -type f | xargs basename -a | grep "\." | rev | cut -f1 -d'.' | rev | sort | uniq -c | sort -n```
- rename all files in a directory<br>
  ```ls | xargs -I{} mv {} {}.bkp```

## 3.5. tee
- the command reads from standard input and writes it to a standard output and to one or more files
- this is useful when we want to see the output of a command both on the screen and also want to save the output in a file for later analysis.

Examples:
- ```ls | tee fileList.txt```

# 4. Filename expansion
- a wildcard character is a character that is used to represent one or more characters in a filename or foldername.
- file globbing is the operation that recognizes these wildcard characters and does the expansion. 

wildcard | description                                                        | example      | matches                           | does not match
---      | ---                                                                | ---          | ---                               | ---
\*       | matches 0 or more characters                                       | ls to*       | to, tom, ton, tow, tommy, tommie  | tata, tea
?        | matches 1 character                                                | ls to?       | tom, tow, ton                     | to, tommy, tommie, tata, tea
[abc]    | matches any one of the characters in the brackets                  | ls [bc]at    | bat, cat                          | Bat, Cat, rat
[a-z]    | matches any one of the characters within the range in the brackets | ls day[1-9]  | day1, day2 upto day9              | day11, day
[!abc]   | matches any one character that is not in the brackets              | ls [!r]at    | bat, cat, Bat, Cat, Rat           | rat
[!a-z]   | matches any one character that is not in the range in the brackets | ls day[!1-9] | day0, days                        | day1 upto day9


# 5. Job control
- command line provides the ability to stop/suspend the execution of a process and resume a suspended process at a later point in time
- each running program is called job
- unique id is assigned to every job 

command        | description
---            | ---
```jobs```     | list all the jobs that the current shell is running or has suspended
```fg```       | bring job to foreground
```bg```       | send job to background
```kill```     | terminate job
```stop```     | suspend job
Ctrl+c         | terminate job
Ctrl+z         | suspend job

- to start a job in the background, we need to add an ampersand(&) at the end of the command

Examples:
- start a job in the background<br>```sleep 1000 &```
- bring the job to the foreground<br>```fg %2 # where 2 is the job number```
- suspend a job<br>```stop %2 # where 2 is the job number```
- resume a job in the background<br>```bg %2 # where 2 is the job number```
- terminate a job<br>```kill %2 # where 2 is the job number```

# 6. Process handling

- Get a snapshot of processes running with ```ps``` command
- Get the process id of a command by ```ps -ef | grep command```
- wait for a process to finish by using ```bash wait <process id>```
- kill a process by using ``` kill <process id>```
- wait for completion of all child processes<br>```wait```
- wait for completion of specific process<br>```wait 1234 # where 1234 is the process id```


## 6.1. difference between ```ps``` and ```jobs```
- ```jobs``` tells the list of jobs the current shell is managing
- ```ps``` tells the list of all the processes running in the system


# 7. Quoting
- Quoting is used to remove special meanings from characters or words
- single quotes - when the single quotes are used, every character within the quotes is preserved and is not evaluated
- double quotes - when the double qoutes are used, the dollar sign, back quotes and blackslashes are evaluated and interpreted.
- escape character - \ is used to preserve the literal value of the following character.
 

Examples: 
examples          | command            | result
---               | ---                | ---
no quote          | ```echo $HOME```   | /home/user1/
escape character  | ```echo \$HOME```  | $HOME
single quote      | ```echo '$HOME'``` | $HOME
double quote      | ```echo "$HOME"``` | /home/user1/

# 8. Basic file management

## 8.1. list directory ```ls```
command                     | description
---                         | ---
```ls```                    | list the contents of current directory
```ls *```                  | list contents of the directory along with the subdirectory
```ls -l```                 | list the contents of a directory along with the owner, permission, date, size
```ls -a```                 | list hidden file
```ls -t```                 | list files in descending order of last modified date
```ls -rt```                | list files in ascending order of last modified date
```ls -R```                 | list files of the current directory and the subdirectory recursively to the last subdirectory
```ls /path/to/dirextory``` | list files in the directory mentioned


## 8.2. show file contents
command                           | description
---                               | ---
```cat demo.txt```                | show the contents of file. use for relatively small files
```head demo.txt```               | show the first part of the file
```tail demo.txt```               | show the last part of the file
```tail -f demo.txt```            | show the text appended to the file as the file grows
```less demo.txt```               | show contents of file one screen at a time
```less -p "regular" demo.txt```  | show contents of the file from the first line with which the pattern matches
```strings -a binaryfile```       | print the sequence of all the printable characters in the file
```diff file1 file2```            | shows difference between 2 files
```comm file1 file2```            | compare 2 sorted file

## 8.3. file handling

### 8.3.1. copy
command                           | description
---                               | ---
```cp file1 file2```              | copy file1 to file2
```cp file1 file2 directory1```   | copy file1 and file2 to directory1
```cp -R directory1 directory2``` | copy contents of directory1 to directory2
```cp *.txt directory1```         | copy all files ending with .txt to directory1

### 8.3.2. move or rename
command                           | description
---                               | ---
```mv file1 file2```              | rename file1 to file2
```mv file1 directory1/```        | move file1 to directory1
```mv *.jpg directory1/```        | move all files ending with .jpg to directory1

### 8.3.3. delete
command                           | description
---                               | ---
```rm file1```                    | remove file1
```rm file1 file2```              | remove file1 and file2
```rm *.png```                    | remove all files ending with .png
```rm -d emptyDirectory```        | remove an empty directory
```rm -r directory1```            | recursively remove all files, subdirectories and directory of directory1

### 8.3.4. file linking
- a symbolic link is a file that points to another file or directory
- there are 2 types of links
  - **Hard link** -> it is an additional name for the existing file. Each file is associated with an unique number. This unique number is called inode. Hardlink associate 2 or more filenames to the same inode and in turn the same file. If the original file is removed, the contents are still available via the hardlink
  - **Soft link** -> it is an indirect pointer to a file or directory. It has only the path of the original file and not its contents

command                           | description
---                               | ---
```ln file1 link1```              | create a hardlink link1 to file file1
```ln -s file1 link1```           | create a softlink link1 to file file1

### 8.3.5. change directory

command                           | description
---                               | ---
```cd```                          | Change to home directory
```cd ~```                        | Change to home directory
```cd -```                        | Change to the previous directory
```cd ..```                       | Change to the parent directory
```cd /```                        | Change to the root directory
```cd ~/dir1/dir2```              | Change to directory relative to home directory

### 8.3.6. display disk usage

command                           | description
---                               | ---
```du```                          | estimates and displays the disk space used by the files
```du -h *```                     | prints size in human readable'

### 8.3.7. file ownership and permissions

command                           | description
---                               | ---
```chmod```                       | change permissions
```chown```                       | change ownership

# 9. Special shell variables

- there are special variables that are set internally
- these variables are available to the user

variable  | description
---       | ---
$0        | name of the shell
\$$        | the process id of the current shell
$?        | the exit status of the last executed command
$!        | the process id of the last background process
$_        | the last argument of the previous command


# 10. Exit codes
- also known as return code
- it is the code that is returned by command or process after it finishes
- following are few exit codes and their meaning

exit code | description
---       | ---
0         | Success
1         | general error
126       | command invoked does not have execute permissions
127       | command not found
130       | command terminated using Ctrl+C



# 11. ```grep```
- searches for pattern in files and prints each line that matches the input pattern
```grep -<options> <pattern> <filenames>```
- grep can be used to search in a single file or in multiple files

## 11.1. Useful ```grep``` options

option  | description
---     | ---
-i      | ignore case
-n      | display line numbers along with lines
-v      | display lines that do not match the pattern
-c      | count the number of matching lines
-l      | diplay the filename of the file which has the matching pattern
-o      | print only the matched string. The whole line with the matched string is not printed
-A\<n>  | include n lines after match 
-B\<n>  | include n lines before match
-C\<n>  | include n lines before and after the match

### 11.1.1. Examples
- lets say a demo file(demo.txt) has following content

> THIS IS UPPER CASE LINE<br>
> this is lower case line<br>
> This is regular line<br>
> This line is also regular<br>
> Line number four<br>
> Line #5<br>
> last line

- Search for a string in a file<br>
  ```grep "this" demo.txt```

- Search for a string in a file, without matching case<br>
  ```grep -i "this" demo.txt```

- Search for a string in a file and get both the line number and output<br>
  ```grep -n "this" demo.txt```

- Get the number of lines matching the searched string<br>
  ```grep -c "this" demo.txt```

- Get the filename in which the searched string is found<br>
  ```grep -l "this" demo.txt```

- Get 2 lines after the matching line<br>
  ```grep -A2 "This" demo.txt```

- Get 2 line before the matching line<br>
  ```grep -B2 "This" demo.txt```

- Get 2 lines before and after the matching line<br>
  ```grep -C2 "This" demo.txt```
 
## 11.2. Regular expression in grep
- a regular expression is a sequence of characters that specifies the search pattern in text.
- different characters have special meaning in regular expressions

character | description
---       | ---
[abc]     | matches any one of the characters in the square brackets
[a-d]     | matches any one of the characters in the range specified in the square brackets
^start    | matches the pattern only if the pattern is at the start of the line 
end$      | matches the pattern only if the pattern is at the end of the line
[^abc]    | matches any one character that is NOT present in the square brackets
[^a-d]    | matches any one character that is NOT present in the range
.         | matches any one character
\*        | mathces 0 or more occurences of the preceding character
.*        | matches zero or more of any character

## 11.3. Examples

- Match any one character<br>
  ```grep "[Tt]his" demo.txt```

- Search for line starting with the search pattern<br>
  ```grep "^last" demo.txt```

- Search for line ending with the search patter<br>
  ```grep "regular$" demo.txt```

- Search for line with a character in specified range<br>
  ```grep "[0-9]" demo.txt```

- Search for line without a character in specified range<br>
  ```grep "[^0-9]" demo.txt```

- Search for a line where the middle characters are not known<br>
  ```grep "line.*regular" demo.txt```

**Note:** grep can have regular expressions in the search pattern part, and can have wildcards in the files to search section.

# 12. ```find```
- the ```find``` command is used to search and locate the list of files and directories
- the list returned will satisfy the conditions used in find command.
- syntax is ``` find [starting point] [expression] ```
- ```-exec [command]``` can be used to run command on the files located by ```find```

## 12.1. Examples
- find files with specific name<br> ```find . -name demo.txt```
- find files with a specific pattern<br> ``` find ./Codes -name *.cpp```
- find directories with specific name<br> ```find . -name Codes -type d```
- find files with permission as 777 and change permissions to 644<br> ```find . -type f -perm 0777 -print -exec chmod 644 {} \;```
- find and remove files<br>```find . -type f -name "*.bkp" -exec rm -f {};```

# 13. ```sed``` filter and transform text
## 13.1. Overview
- looks for pattern and edits them
- works on both files and stdin
- original files is not updated
- results are put into standard output
- syntax is ``` sed 'instructions' file```
- instruction is of format ``` '[address]command/regex/replace/modifier' ``` 
  - example - '5,15s/abc/ABC/g' -> this will substitute abc with ABC in lines 5 to 15. 
    - modifier g specifies that all occurences of abc in line will be replaced with ABC
- when address is used, the lines belonging to the address are examined/modified. -> ```sed '1,100 s/A/a/' file.txt```. this restricts substition to first 100 lines.
- By default all the lines are printed. When '-n' flag is used, this behavior is suppressed. Nothing will be printed unless an explicit request to print is found.
- A pattern can be used as a address -> ```sed -n '/start/,/stop/ p' file.txt```
- When '!' is used, the command is run outside of the address -> ```sed -n '/match/ !p' file.txt```

command | description
---     | ---
d       | delete
p       | print
s       | substitute
q       | quit
a       | insert a line after pattern
i       | insert a line before pattern
c       | change a line
y       | transform

## 13.2. Examples
- remove blank lines<br>``` sed '/^$/d' file.txt```
- remove all lines with search string<br>```sed '/Search/d' file.txt```
- remove all instances of search string<br>```sed 's/Search//g' file.txt```
- print lines with the search string<br>```sed '/Search/ p' file.txt```
- substitue a string with another<br>```sed 's/oldString/newString/g' file.txt```
- remove trailing spaces<br>```sed 's/ *$//' file.txt```
- remove leading spaces<br>```sed `s/^ *//' file.txt```
- add spaces to start of everyline<br>```sed 's/^/    /' file.txt```
- print the first 10 line<br>```sed '10 q' file.txt```<br>```sed -n '1,10 p' file.txt```
- append line after a pattern<br>```sed '/pattern/ a add line here' file.txt```
- insert line before a pattern<br>```sed '/pattern/ i add line here' file.txt```
- change a line with a pattern<br>```sed '/pattern/ c line changed here' file.txt```
- change a->p, b->q, c->r<br>```sed 'y/abc/pqr/' file.txt```
  
## 13.3. Grouping
- sed allows capturing specific parts of text into groups.
- these groups can be manipulated
- group is enclosed within parentheses expression "\(" and "\)" in the search string
- each group is assigned a number. The first group is assigned \1 and so on.
- \1 can be both in pattern string and replacement string

### 13.3.1. Grouping Examples:
- switch first and second columns<br>```sed 's/\([a-z]*\) \([a-z]*\)/\2 \1/' file.txt```
- print lines which have consecutive duplicate words<br>```sed -n '/\([a-z][a-z]*\) \1/p' file.txt```
- remove consecutive duplicate words in a line<br>```sed 's/\([a-z][a-z]*\) \1/\1/' file.txt```

## 13.4. Hold Buffer
- When sed read text, each line is placed into a temporary space.
- When a new line is read, the old text is replaced by the new line in the temporary space.
- This temporary space is called pattern space.
- Hold buffer is like a long term storage. text can be copied to and from pattern space.

command | description
---     | ---
x       | exchange hold space and pattern space
h       | copy pattern buffer into hold space
H       | append pattern buffer into hold space
g       | copy hold space to pattern space
G       | append hold buffer into pattern buffer

### 13.4.1. Example
- print one line after and before the pattern match<br>```sed -n '/999/ !{x;d};/999/ {x;p;x;p;n;p}' file.txt```
- add space after every line<br>```sed 'G' file.txt```
- insert blank line above every line which matches pattern<br>```sed '/start/ {x;p;x}' file.txt```
- Insert blank line after every line which matches pattern<br>```sed '/start/ {G}' file.txt```
- Insert blank line before and after every line which matches pattern<br>```sed '/start/ {x;p;x;G}' file.txt```

# 14. ```awk```
- command line utility to find, process and transform text files
- the basic syntax is ```pattern { action }```
  - the pattern is compared with every input line. pattern can be any regular expression
  - when the pattern matches, the action is performed
  - when no pattern is provided, the action is applied to every line
  - example -> ```/^HTTP/ {print}```
    - every line starting with HTTP is printed
  - there are 2 other important patterns
    - BEGIN - specifies actions to be performed, before any line is read
    - END   - specifies actions to be performed, after all lines are read
    - Example -> ```awk 'BEGIN{print "start"} {print} END{print "end"}' file.txt```
      - first *start* is printed, then all lines of file.txt are printed and then *end* is printed
- awk interprets each line as a record of fields
- one or more consecutive spaces or tabs are considered as a single delimiter between fields
- $1, $2, etc. represents the first field, second field, and so on.
- $0 represents the entire input line
- awk has 2 data types - strings and integers
- awk internally converts variable according to context
- awk supports associative arrays. example ```var[key] = value```
- on integers, basic arithmatic operations (+-*/%) are supported. autoincrement(++) and decrement(--) is also supported.

## 14.1. Actions
- following are few actions that can be performed

action                                                                      | description
---                                                                         | ---
{ print $0; }                                                               | print records
{ exit; }                                                                   | ends program
{ next; }                                                                   | skips current line
{a=$1; b="X"}                                                               | variable assignment
{ c[$1] = $2 }                                                              | array varaible assignment
{if (condition) { action } else if (condition) { action } else { action }}  | if else conditions
{ for (i=1; i < x; i++) { action } }                                        | for loop
{ for (item in c) { action } }                                              | for loop iterating over a list

## 14.2. Special variables

variable    | desc
---         | ---
FS          | Input field separator. can be modified
RS          | Input record separator. default value is newline. can be modified by user
OFS         | Output field separator. can be modified
ORS         | Output record separator. default value is newline. can be modified by user
NF          | Number of fields in the current line (record). cannot be updated by user
NR          | Number of lines processed so far. cannot be updated by user

*Note: -F option can be used to update the input field separator -> ```awk -F":"'{ print $1 }' file.txt```*

## 14.3. Examples
- split up “,” (comma) separated fields and print the third field ($3)<br>```awk -F"," '{print $2}' file.txt```
- print the 3rd field of a csv if the second field ($2) exists and is not empty<br>```awk -F"," '{if ($2)print $3}' file.txt```
- print the last field in each line<br>```awk -F"," '{ print $NF }' file.txt```
- print the line after the line matching search pattern<br>```awk '/pattern/ { i=1; next; } {if(i) {i--; print;}}' file.txt```
- print the line and the 2 lines after the line matching search pattern<br>```awk '/regexp/ {i=3;} { if(i) {i--; print;}}' file.txt```
- print the lines from a file starting at the line matching *start* until the line matching *stop*<br>```awk '/start/,/stop/' file.txt```
- count lines (wc -l)<br>```awk 'END{print NR}' file.txt```
- print matching lines (grep)<br>```awk '/pattern/'```
- print non matching lines (grep -v)<br>```awk '!/pattern/'```
- remove duplicate consecutive lines (uniq)<br>```awk 'a !~ $0 {print}; {a=$0}' file.txt```
- print first 10 lines of file (head)<br>```awk 'NR < 11' file.txt```
- print last 10 lines of file (tail)<br>```awk '{vect[NR]=$0;} END{for(i=NR-9;i<=NR;i++) {print vect[i];}}' file.txt```
- print the total number of bytes used by files<br>```ls -l | awk '{ x += $5 } END { print "Total bytes: " x }'```

# 15. Command substitution
- In command substitution, the output of a command replaces the command
- the output of a command can be used an argument to another command
- syntax is ``` `command` ``` and ```$(command)```
- using backticks (`) is discouraged and has been deprecated
- ```$(commmand)``` supports nesting i.e. ```$(command1 $(command2))```

## 15.1. Examples
- assign the output of a command to a variable<br> ``` thedate=`date` ```
- use the output of command as a parameter of another command<br> ``` vi $(grep -l 123 *) ```

# 16. Process substitution
- the input or output of a command can appear as a file. This is known as process substitution
- this technique is useful when we want to use the output of multiple commands as the input to a command
- process substitution can also be used to capture output and redirect it to the input of a process
- template - ```<(command)``` and ```>(command)```

## 16.1. Examples:
- sort and compare two files<br>
  ```diff <(sort file1) <(sort file2)```

- compare 2 folders<br>
  ```diff <(ls $first_directory) <(ls $second_directory)```

# 17. Subshell
- a subshell is a child process launched by a shell
- whenever a shell script is run, a subshell is created and the script is run in the subshell
- variables defined in parent shell can be accessed if ```export``` is used while defining the variable
- subshells can also be created using parentheses<br>
  ```(command1; command2; command3)```
- subshells are a convenient way to group commands. 
- can be used to temporarily move to a different directory
```bash
#do something in current directory
(cd some/other/directory; other-command)
#back in the original directory
```
- to run a command or script in the current shell, without creating a subshell, use '.' as in ```. script.sh```

# 18. Command grouping
- sometimes we need to run multiple commands and redirect all the output to a single file. Command grouping helps in this.
- without command grouping we need to redirect each command output individually to a file

## 18.1. using parentheses
- Grouping list of commands can be done using parentheses *()*
- a subshell is created
- example - ```(date; uptime) > file.txt```

## 18.2. using curly braces
- Grouping commands can be done using curly braces *{}*
- causes the list to be executed in the current shell context 
- no subshell is created
- example - ```{date; uptime;} > file.txt```

# 19. Text editing with ```cut```, ```paste``` and ```join```

## 19.1. ```cut```
- ```cut``` command cuts out sections from each line and writes result to standard output
- syntax is ```cut OPTION [FILE]```

option  | description
---     | ---
-c      | character range which will be selected
-d      | delimiter which will separate each fields in line in file
-f      | fields which will be printed

when -c option is used, ranges can be specified. Each range can be one of:
range type  | description
---         | ---
N           | Nth character
N-          | fron Nth character to end of line
N-M         | from Nth character to Mth character
-M          | from first to Mth character

### 19.1.1. Examples
- print the first and third columns of a csv file<br>```cut -f1,3 -d"," file.txt```
- print the first 3 characters of each line<br>```cut -c -3 file.txt```

## 19.2. ```paste```
- merges lines of files
- by default, the lines from each files are delimited by tab
- when '-' is used instead of filename, the command reads from standard input
- syntax ```paste [OPTION] [FILE] [FILE]```
  
option  | description
---     | ---
-d      | used to specify the delimiter
-s      | paste one file at a time

### 19.2.1. Examples
lets take 2 files - number.txt and name.txt
> cat number.txt
> 1<br>
> 2<br>
> 3<br>
> 4<br>

> cat name.txt
> Alice<br>
> Bob<br>
> Charlie<br>
> David<br>

- merge 2 files, first file will give the first column and second file will give the second column<br>```paste number.txt name.txt```
- merge 2 files, delimited by ','<br>```paste -d"," number.txt name.txt```
- merge 2 files, sequentially, i.e first only first file is printed and then only the second file<br>```paste -s number.txt name.txt```

## 19.3. ```join```
- join lines of two files on a common field
- syntax ```join [OPTIONS] FILE1 FILE2```

### 19.3.1. Examples
lets take 2 files - number.txt and name.txt
> cat number.txt
> 1 100<br>
> 2 101<br>
> 3 102<br>
> 4 103<br>
> 5 104<br>

> cat name.txt
> 1 Alice<br>
> 2 Bob<br>
> 3 Charlie<br>
> 4 David<br>

- join 2 files based on the first column<br>```join number.txt name.txt```

# 20. Aliases
- aliases are short names for long commands
- when we need to execute long commands multiple times, it is advisable to create aliases
- syntax - ```alias [-p] [name[=value]]```
- we can create permanent alias by storing them in configuration files
- to temporarily bypass an alias, use \ -> ```\ll```

- creating a alias<br>```alias name='values'```
- removing alias<br>```unalias name```
- print all defined alias<br>```alias -p```

## 20.1. useful aliases
```bash
alias gh='history|grep'
alias c=clear
alias cx='chmod +x'
alias ..='cd ..'
alias sl=ls
alias left='ls -t -1'
alias count='find . -type f | wc -l'
alias f='find . |grep '
```

# 21. Functions
- set of commands that accomplish a specific task
- can be used numerous times
- helps avoid writing the same code repeatedly
- can use loops and conditions within them
- arguments can be passed to functions
- by using ```export -f functionname```, we can make the functions available to shell scripts
  - export can be added to configuration files like *.bashrc*
  - To keep things modular, create a new file called ~/.bash_functions and then have your .bashrc load it
- syntax<br> 
```bash
function_name () {
  commands
}
```

```bash
function_name () { commands; }
```

## 21.1. useful functions
```bash
mcd() { mkdir -p "$1"; cd "$1";}
cdl() { cd "$1"; ls;}
```

# 22. sort
- sort lines text files

option  | description
---     | ---
-r      | sort in reverse order
-n      | sort in numberical order
-k <n>  | sort based on nth column
-u      | sort and remove duplicates

# 23. uniq
- report or omit repeated lines
- the input file must be sorted

option  | description
---     | ---
-c      | show how many times a line is repeated
-d      | prints only the repeated lines only once
-u      | prints only the unique lines
-i      | case insensitive comparison


# 24. Conditions
## 24.1. If else
- if-then-else is supported in command line
- Syntax
```bash
if [ condition1 ]; then command1;
elif [ condition2 ]; then command2;
else command3; fi
```

```bash
if [ condition1 ]; then command1; elif [ condition2 ]; then command2; else command3; fi
```
- there are different types of conditions
  1. file based condiitons

conditions  | description
---         | ---
-e          | check if file exists
-r          | check if file exists and is readable
-w          | check if file exists and is writable
-d          | check if file exists and is a directory

  2. string based conditions

conditions  | description
---         | ---
==          | check if both the strings are equal
!=          | check if both the strings are not equal
\>          | check if the first string is lexicographically greater than the second
<           | check if the first string is lexicographically smaller than the second
-n          | check if the string has a length more than 0
-z          | check if the string is an empty string

  3. number based conditions

conditions  | description
---         | ---
-eq         | check if the numbers are equal
-ne         | check if the numbers are not equal
-gt         | check if the first number is greater than the second
-ge         | check if the first number is greater than or equal to the second
-lt         | check if the first number is less than the second
-le         | check if the first number is less than or equal to the second


- 0 is considered true and numbers greater than 0 are considered false. 
  - this is because in Unix/Linix, when a process ends successfuly, it returns 0

## 24.2. Short circuiting
- an alternative way of using conditions is by using logical AND (&&) and logical OR(||)
- evaluation of a logical expression is stopped, as soon as the outcome has been determined. This is known as short-circuiting.
- in case of Logical AND, as soon as sub-expression becomes false, the whole expression evaluates to false
  - in case of *expr1 && expr2*, if expr1 evaluates to false, then the whole expression will evaluate to false. So, expr2 is not evaluated at all.
  - && can be used to ensure that command2 is run only if command1 ends successfully. example ->```command1 && command2``` 
- in case of Logical OR, as soon as sub-expression becomes true, the whole expression evaluates to true
  - in case of *expr1 || expr2*, if expr1 evaluates to true, then the whole expression will evaluate to true. So, expr2 is not evaluated at all.
  - || can be used to ensure that command2 is run only if command1 fails. example -> ```command1 || command2```

### 24.2.1. example
- create folder if it does not exist  
```bash
  [ -d ./some/path/folder ] || mkdir /some/path/folder
```

- create create file only if folder exists
```bash
  cd /some/path/folder && touch file.txt
```

# 25. Loops
## 25.1. while loops
- the loop runs as long as the given condition is true
- syntax 
  ```bash 
  while [ condition ]; do commands; done
  ```
### 25.1.1. example
- print all the folders with .c files<br>
```bash
find . -name *.c | {while read -r filename; do dirname $filename; done;} | sort | uniq # dirname returns the directory name
```


## 25.2. for loops
- the loop iterates over a list of values or preset number of times
- syntax 
  ```bash
  for <variable name> in <a list of items>;do <some command> $<variable name>;done;
  ```
### 25.2.1. example
- copy files from one folder to another
```bash
for file in ./code/*.txt; do cp $file /home/code/backup; done
```

# 26. ssh
- ssh (SSH client) is a program for logging into a remote machine and for executing commands on a remote machine
- syntax ```ssh user@host```
- running a single command on remote server<br>```ssh user@host command_to_run```
- logging into server with different port<br>```ssh -p portnum user@host```
- ssh connection using host in the middle```ssh -t reachable_host ssh unreachable_host```

# 27. curl
- used to transfer data from one server to another
- syntax - ```curl [options] [URL]```

options | description
---     | ---
-o      | save the output in a file with name as specified after the option
-O      | save the output in a file with the same name as in the url
-C -    | resume a download
-I      | fetch headers of a url
-L      | follow redirects


## 27.1. Examples
- retrieve a webpage<br>```curl example.com```
- save a webpage<br>```curl example.com -o example.html```
- resume a download<br>```curl -C - -O https://releases.ubuntu.com/21.10/ubuntu-21.10-desktop-amd64.iso```
- fetch headers only<br>```curl -I example.com```
- fetch weather<br>```curl wttr.in/london```

## 27.2. handling REST calls
### 27.2.1. GET
- GET is used to fetch resource
- the GET method is the default method
- example ```curl https://reqres.in/api/users/2```

### 27.2.2. POST
- POST is used to create resource in a server
- To send a curl POST request we use the option -X POST
- example ```curl -X POST -H "Content-Type: application/json" -d '{"email": "eve.holt@reqres.in","password": "pistol"}' https://reqres.in/api/register```

### 27.2.3. PUT
- PUT is used to update resource
- To send a curl PUT request we use the option -X PUT
- example ```curl -X PUT -H "Content-Type: application/json" -d '{"name": "morpheus","job": "zion resident"}' https://reqres.in/api/users/2```

### 27.2.4. DELETE
- DELETE is used to remove resource
- To send a curl DELETE request we use the option -X DELETE
- example ```curl -X DELETE https://reqres.in/api/users/2```

# 28. wget
- command line utility to download file

options | description
---     | ---
-O      | download file under different name
-c      | resume a download

## 28.1. Examples
- download a file<br>```wget https://releases.ubuntu.com/21.10/ubuntu-21.10-desktop-amd64.iso```
- resume a download<br>```wget -c https://releases.ubuntu.com/21.10/ubuntu-21.10-desktop-amd64.iso```


# 29. One liners

- print the files and directories in tree structure<br>```find . | sed -e "s/[^-][^\/]*\// |/g" -e "s/|\([^ ]\)/|-\1/"```
- print the directories in tree structure<br>```find . -type d   | sed -e "s/[^-][^\/]*\// |/g" -e "s/|\([^ ]\)/| - \1/"```
- quick access to ascii table<br>```man ascii```
- find common lines in 2 files<br>```cat file1 file2 | uniq -d```
- find lines in file1 that is not present in file2<br>```cat file1 file2 file2 | uniq -u```
- find most frequently used commands<br>```history | cut -c8- | sort | uniq -c | sort -rn | head```
- recursively remove only directories with no files<br>```find . -depth -type d -exec rmdir {} \;```

# 30. Further reading
- 

# 31. Change History
- presented in reversed chronological order i.e. the latest change is at the top

Name                  | Date          | Change Description
----                  | ----          | ---
Utsav Barman          | 26 Jan 2022   | added command grouping
Utsav Barman          | 25 Jan 2022   | added chown, chmod and du
Utsav Barman          | 25 Jan 2022   | added & to start a background job; added curl and wget
Utsav Barman          | 25 Jan 2022   | read should be used with option -r ; used appropriate variable names in for loop example;
Utsav Barman          | 25 Jan 2022   | Updated variable DATE to thedate. Uppercase variables are conventionally used for environment variables. Added $() for command substitution. backticks are discouraged; replaced -a with -e
Utsav Barman          | 25 Jan 2022   | fixed typo for cd to root directory; added section for special shell variables and exit codes;
Utsav Barman          | 25 Jan 2022   | Added wait, globbing, grep -o; fixed typos
Utsav Barman          | 24 Jan 2022   | Initial draft




