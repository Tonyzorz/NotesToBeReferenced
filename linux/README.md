
# UsefulThingsForCoding
Things that might come in handy later on in the future!

## Linux command notes 

Studying terminal commands from [linuxcommand](http://linuxcommand.org/index.php), all credits goes to this site. 

## Index

 - A. [What is the Shell?](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#What-is-the-Shell)  
 - B. [Navigation](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#Navigation)  
 - C. [Looking around](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#looking-around)  
 - D. [A guided tour](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#a-guided-tour)  
 - E. [Manipulating files](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#manipulating-files)  
 - F. [Working with commands](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#working-with-commands)  
 - G. [I/O redirection](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#i/o-redirection)  
 - H. [Expansion](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#expansion)
 - I. [Permissions](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#permissions) 
 - J. [Job control](https://github.com/Tonyzorz/UsefulThingsForCoding/blob/master/linux/README.md#job-control)  

## What is the Shell?
	
 **Shell** - a program that takes comands from keyboard and gives them to the operating system to perform.   
 
Nowadays, we have graphical user interfaces, _gui_, in addition to command line interfaces. On most linux system, a bash acts as the shell program. 

 Terminal is a program that lets user interact with shell. 

## Navigation  

* **pwd** - prints current directory
* **cd** - changes directory
* **ls** - list files and directories

## Looking around

* **ls** - list files and directories
	* ls -l = list the files in the working directory in long format
	* ls -la = list all files including the hidden ones
* **less** - view text files
* **file** - could see what type of file selected file is

Most commands operate in this pattern :
	
> command -options arguments

ls -la ../ = means list files and directories in long format of current location's previous directory

Use double quotes if file or directory contains space in between. When creating a file or directory, underscore bar is widely used instead of space bar. 

## Manipulation files
* **cp** - copy files and directories
* **mv** - move or rename files and directories
*  **rm** - remove files and directories 
*  **mkdir** - create directories
* **touch** - creates file

## Working with commands
* **type** - display information about command type
*  ** which** - locate a command
*  **help** - display reference page from shell bulltin (like help50 from cs50)
*  **man** - display an online command reference

command types :
1. executable programs
2. shell bulltin - a command built into shell itself
3. shell function - 
4. alias - commands that you can build youself
	>ls is aliased to `ls -F --color=auto --show-control-chars'

## I/O redirection

most command line programs that display their results do so by sending their results to a facility called standards output.
	
	">" character is used to send the output to a designated file

	">>" character is also used to send the output to a designated file but > overwrites while >> appends

$((arithmetic expression))

	ex. Echo $(($((5 ** 2))* 3)) or 
	$(((5 ** 2) * 3))

Brace Expression

	$ echo a{A{1,2},B{3,4}}b
	aA1b aA2b aB3b aB4b

	mkdir {2007..2009}-0{1..9} {2007..2009}-{10..12}

## Permissions

Computing systems can have not only multitasking but also multi-user. Before computers were personal, a typical university computer system consisted of a large mainframe computer and terminals were located throughout the campus. 

* **chmod** - modify file access rights

	 when ls -l is typed, -rwxrwxrwx type format may appear. The first case is displayed as - or d, - for file d for directory. there are three sections divided by three letters, each part in sequential order representing owner, group owner, and other users. 
	chmod ### file/directory will modify the access rights. 
	the numbers are represented as binary. for rwx, it will be 111 = 7. So if you want to grant all access to all users, which is not recommended, you have to type 777.

* **su** - temporarily becomes superuser
	
	you can become superuser by typing the comand su. Typing exit will end your superuser session.
	on mac though, su is disabled by default( I have enabled the su command using the taewon default password for my personal computer).

* **sudo** - temporarily become the superuser
* **chwon** - change file ownership
* **chgrp** - change a file's group ownership

## Job control
>cannot perform this on mac os, will get back to it once i install linux os later on and edit

a single processor computer can only execute one process at a time but linux kernel manages to give each process its turn so it makes it look like it is running simultaneously.

* **ps** - list the process running on the system
*  **kill** - send a signal to one or more processes (usually to kill a process)
*  **bg** - put a process in the background
* **fg** - put a process in the foreground

