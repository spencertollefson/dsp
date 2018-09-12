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

> > 1. **pwd [NAME]** - shows the current working directory path

    2. **mkdir [NAME]** - creates a directory

    3. **rm -rf [NAME]** *or* **rmdir [NAME] (only if empty)** - deletes the directory. The -r option is recursive and allows all subfiles and subdirectories to be deleted as well. The -f option is to force this potentially dangerous option through.

    4. **touch [NAME]** - this command creates a new file

    5. **rm [NAME]** - this command deletes a file

    6. **mv [OLDNAME] [NEWNAME}** - this command in effect renames files

    7. **ls -a** - this command shows all files, including hidden ones

    8. **cp [OLDFILE] [NEWFILEPATH] - this command copies a file

    9. **head [NAME]** - this command shows the first 10 lines (can be changed) of a file

    10. **tac [NAME]** - this command reads a file's lines in reverse older. Just for fun!


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

> > `ls` This command lists the contents of the current directory. However it keeps things simple.
    `ls -a` Lists all the contents, including hidden files.
    `ls -l` Long list format. Includes additional info like read/write/executable permissions, owner, group, file size, and more.
    `ls -lh` Long list and human readable format. Human readable shows file sizes in KB, MB, and GB instead of only bytes
    `ls -lah` Long list, all files (hiden too), and human readable file size listing.
    `ls -t` sort by modification time, with the newest being printed first
    `ls -Glp` remove Group permissions from the long listing, and append the indicator backslash / to directories

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > `kill` - this command can be folloewd by PID to kill a process
    `chmod` - this command allows one to change permissions. Useful for allowing script files to be run more simply.
    `man` - I've been using this command this whole assignment to look up the manual for different commands
    `whoami` - reminds me who I am everytime I forget
    `grep` - I want to get much better with this command. Is able to search through file(s) for strings. Can be combined with regex for powerful seraches.

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > Xargs is a bit difficult to wrap your head around as it doesn't read input from other CLI arguments. Rather, it reads in data from STDIN and executes the command one or more times. The one or more times is key, is that is where xargs really shines.

An example is `xargs -n 1 find -name ".jpeg" ".png"`. This '-n' option tells xargs how many arguments you want to pass to the command per line. So in this case, one argument is passed for every find optoin. Thus, xargs allows this find to search every file for either ".jpeg" or ".png" and keeps them separate.

 

