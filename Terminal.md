# Practice in the Terminal

## The Command Line 
1. `sudo`

sudo (SuperUser DO) Linux command allows you to run programs or other commands with administrative privileges, just like “Run as administrator” in Windows. This is useful when, for example, you need to modify files in a directory that your user wouldn’t normally have access to.

2. `apt-get`

is the one of the most important Ubuntu commands every beginner must know. It is used to install, update, upgrade and remove any package. apt-get basically works on a database of available packages
 * sudo apt-get update
 * sudo apt-get upgrade
 * sudo apt-get install
 * sudo apt-get remove
 * sudo apt-get purge
 * sudo apt-get autoremove

 3. `ls`

ls (list) command lists all files and folders in your current working directory. You can also specify paths to other directories if you want to view their contents.

4. `cd`

cd (change director”) Linux command also known as chdir used to change the current working directory. It’s one of the most used basic Ubuntu commands. Using this command is easy, just type cd followed by the the folder name. You can use full paths to folders or simply the name of a folder within the directory you are currently working. Some common uses are:

* cd /  – Takes you to the root directory.
* cd .. – Takes you up one directory level.
* cd –  – Takes you to the previous directory.

5. `pwd`

pwd (print working directory) Ubuntu command displays the full pathname of the current working directory.

6. `cp`

cp (copy) Linux command allows you to copy a file. You should specify both the file you want to be copied and the location you want it copied to – for example, cp xyz /home/myfiles would copy the file “xyz” to the directory “/home/myfiles”.

7. `mv`

mv (move) command allows you to move files. You can also rename files by moving them to the directory they are currently in, but under a new name. The usage is the same as cp – for example mv xyz /home/myfiles would move the file “xyz” to the directory “/home/myfiles”.

8. `rm`

rm (remove) command removes the specified file.

* rmdir (“remove directory”) – Removes an empty directory.
* rm -r (“remove recursively”) – Removes a directory along with its content.

9. `mkdir`

mkdir (make directory) command allows you to create a new directory. You can specify where you want the directory created – if you do not do so, it will be created in your current working directory.

10. `history`

history command displays all of your previous commands up to the history limit.

11. `df`

df (display filesystem) command displays information about the disk space usage of all mounted filesystems.

12. `du`

du (directory usage) command displays the size of a directory and all of its subdirectories.

13. `free`

free – Displays the amount of free space available on the system.

14. `uname -a`

uname -a – Provides a wide range of basic information about the system.

15. `top`

top – Displays the processes using the most system resources at any given time. “q” can be used to exit.

16. `man`

man command displays a “manual page”. Manual pages are usually very detailed, and it’s recommended that you read the man pages for any command you are unfamiliar with. Some uses are :

* man man – Provides information about the manual itself.
* man intro – Displays a brief introduction to Linux commands.


17. `info`

Similar to man, but often provides more detailed or precise information.

18. `<command name> -h` or `<command name> –help`

This command is a third alternative to get help. While not as detailed as the info or man pages, this will provide a quick overview of the command and its uses.

For example: 
```
man -h or man -help
```

19. `passwd`

passwd Ubuntu basic command is used to change user password using Terminal. What you have to do is run the below command, where is the username whose password has to change:
```
passwd <user>

```

20. `whatis`

whatis command shows a brief description of what is the functionality of specific built-in Linux command.

`whatis <command>`

Some examples are:
```
whatis cd
whatis man
whatis help
```

## Terminal Shortcuts:
|Terminal Shortcuts | Function |
| :---:    | :---    |
| Ctrl + Shift + T |	Open new tab on current terminal |
|Ctrl + Shift + W  | Close the current tab |
|Ctrl + A |	Move cursor to beginning of line|
|Ctrl + E	|Move cursor to end of line|
|Ctrl + U	|Clears the entire current line|
|Ctrl + K	|Clears the command from the cursor right|
|Ctrl + W	|Delete the word before the cursor|
|Ctrl + R	|Allows you to search your history for commands matching what you have typed|   
|Ctrl + C	|Kill the current process|
|Ctrl + Z	|Suspend the current process by sending the signal SIGSTOP|
|Ctrl + L	|Clears the terminal output|
|Alt + F	|Move forward one word|
|Alt + B	|Move backward one word|
|Ctrl + Shift + C	|Copy the highlighted command to the clipboard|
|Ctrl + Shift + V or Shift + Insert	|Paste the contents of the clipboard|
|Up/Down Arrow keys	|To scroll through your command history, allowing you to quickly execute the same command multiple times|
|TAB	|Used to complete the command you are typing. If more than one command is possible, you can press it multiple times to scroll through the possible completions. If a very wide number of commands are possible, it can output a list of all possible completions.|



















