# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

>> `pwd` shows current working directory  
`mkdir <directory>` creates a directory  
`rm -r <directory>` deletes a directory  
`touch <file>` creates a new empty file  
`rm <file>` deletes a file  
`mv <oldname> <newname>` renames a file  
`ls -a` lists hidden files  
`cp <olddir/file> <newdir/>` copies a file from one directory to another  
`mv <olddir/file> <newdir/>` moves a file from one directory to another  
`echo <text>` outputs text to the terminal (standard output)  
`cat <file>` outputs contents of file to the terminal  
`>` redirects standard output to file (overwrites)  
`>>` redirects standard output to file (appends)  
`<` redirects standard input to a command  
`2>` redirect error messages  
`|` redirects standard output of command on left as standard input to command on right  
`sort` takes standard input and orders it alphabetically for standard output  
`uniq` filters out adjacent, duplicate lines  
`grep` searches for lines that match a pattern  
`sed` searches for and modifies a pattern based on an expression

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

>> `ls` lists all contents of working directory  
`ls -a` lists all contents of a directory, including hidden files and directories  
`ls -l` lists all contents in long format  
`ls -lh` lists all contents in long format with human readable sizes (unit suffixes)  
`ls -lah` lists all contents including hidden files/directories in long format with human readable sizes (unit suffixes)  
`ls -t` orders files and directories by the time they were last modified  
`ls -Glp` long format colorized by file type with a slash ('/') after directory names

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

>> `ls -lhtr` list contents by modified timestamp in reverse order with unit suffixes  
`ls -ld */` only list directories in working directory  
`ls -lhR` list contents of working directory and all child directories (recursively) with unit suffixes  
`ls -lA` list all contents including hidden files except '.' (current directory) and '..' (parent directory)  
`ls -lS` list contents by file size


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

>> `xargs` is used to convert standard input into arguments that are passed to another command. For a simple example, xargs can rename multiple files with .TXT extension to .txt by providing it a list of filenames that have all-caps suffixes (identified with the `basename` command):  
`basename -s .TXT -a *.TXT | xargs -n1 -I % mv %.TXT %.txt`
