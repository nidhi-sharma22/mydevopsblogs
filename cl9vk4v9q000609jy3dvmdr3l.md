---
title: "Linux cheat Sheet"
datePublished: Sun Oct 30 2022 16:19:17 GMT+0000 (Coordinated Universal Time)
cuid: cl9vk4v9q000609jy3dvmdr3l
slug: linux-cheat-sheet
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1667142687607/EAonQhC8N.jpg
tags: linux, linux-for-beginners, linux-basics

---

# **What Is Linux?**

Like macOS, Windows & iOS. Linux is a operating System. 

### Now let's move to Commands used in Linux....

***Commands***

**User information Commands**
- ```
$ who
``` :- who command is used to display users who are logged on the system, including the terminals they are connecting from.

- 
```
$ id
```:- used to print the genuine and effective user ID and group ID.

- 
```whoami
``` :- Show your username


- ```
$ uname -a
``` :- Show system and kernel.
- ```
$ date
``` :- Show system date
- ```
$ uptime
``` :- Show uptime

**Directory Operations**


- ```
$ pwd
``` :- Show current directory
- ```
$ mkdir dir
``` :- Make directory dir
- ```
$ cd dir
``` :- Change directory to dir
- ```
$ cd ..
``` :- Go up a directory


**File Operations**


- ```
$ rm filename
```:-  to remove file name
- ```
$ ls
``` :- 	List files
- ```
$ ls -l
``` :- detailed listing of the files and directories in the current directory.

- 
```$touch filename
``` :- to create a new file.

- 
```$cat filename
``` :- to display the contents of a file.

- 
```$cp source/filename destination/
``` :- To create the copy of a file. It will create the new file in destination with the same name and content as that of the file ‘filename’.


- 
```$mv source/filename destination/
``` :- To move a file from source to destination. It will remove the file filename from the source folder and would be creating a file with the same name and content in the destination folder.


- 
```$mv filename new_filename
``` :- To rename a file. It will rename the filename to new_filename or in other words, it will remove the filename file and would be creating a new file with the new_filename with the same content and name as that of the filename file.


- 
```tail file1
``` :- Show last 10 lines of file1


- 
```head file1
``` :- Show first 10 lines of file1

## File Permis­sions

First digit is owner permis­sion, second is group and third is everyone.

Calculate permission digits by adding numbers below.

- 4 read (r)
- 2 write (w)
- 1 execute (x)

**Commands for File Permissions**

- ```
chmod 775 file
``` :- Change mode of file to 775








 














