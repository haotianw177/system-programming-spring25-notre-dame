# notes


## Week 1 – What Is the Shell?
When we speak of the command line, we are really referring to the shell. The shell is a
program that takes keyboard commands and passes them to the operating system to carry
out. Almost all Linux distributions supply a shell program from the GNU Project called
bash. The name “bash” is an acronym for “Bourne Again SHell”, a reference to the fact
bash is an enhanced replacement for sh


- In Linux, the `$` symbol in a prompt usually indicates that you are logged in as a regular user.
- If you're logged in as the root user (superuser), the prompt will typically use a `#` instead.
- The first directory in the file system is called the root directory
- Note that unlike Windows, which has a separate file system tree for each storage device, Unix-like systems such as Linux always have a single file system tree, regardless of how many drives or storage devices are attached to the computer. Storage devices are attached (or more correctly, mounted) at various points on the tree according to the whims of the system administrator, the person (or people) responsible for the maintenance of the system.
- Absolute Pathnames(fix navigation), Relative Pathnames(., ..) In general, if we do not specify a pathname to something, the working directory will be assumed.
- Filenames and commands in Linux, like Unix, are case sensitive. Filenames that begin with a period character are hidden. This only means that `ls` will not list them unless you say `ls -a`.
- Linux has no concept of a “file extension”(.pdf , .txt).
- Though Linux supports long filenames that may contain embedded spaces and
punctuation characters, limit the punctuation characters in the names of files
you create to period, dash, and underscore. Most importantly, do not embed
spaces in filenames. If you want to represent spaces between words in a file-
name, use underscore characters.
-

commands: 

`exit` end a terminal session

`$` Represents the shell prompt or a variable (e.g., `$HOME` is the home directory path).

`date`
`uptime`
`df`  to see the current amount of free space on our disk drives

`free` display the amount of free memory
`alias`  arbitrarily creates shortcuts for commands (e.g., alias ll='ls -la').

**`source $HOME/.bashrc`** Applies changes made to the `.bashrc` file, reloading the shell configuration. **`.bashrc`** file is a configuration file for the **Bash shell**

`touch`  creating new empty files(create multiple ones at the same time is allowed) or updating the timestamp (last access and modification times) of existing files

`mkdir` Creates a new directory(folder)

`mv` move

`ls` Lists files and directories in the current directory

`ls -l` Lists files in long format

`ls -la`  Lists all files (including hidden ones) in long format, showing details like permissions, ownership, size, and modification date

`cd`  Changes the current directory to the new directory

`cd -`  Switches back to the previous directory

`cd ~/`  Changes to the user's home directory

`cd/`  Changes to the root directory

`cd ~`  go to the home directory

`cd ..`  move up one directory level

`cd ~user_name` Changes the working directory to the home directory of
user_name.

`~/.bashrc`  refers to the user's shell configuration file

`less` Displays a file's content one screen at a time

`pwd` Prints the current working directory's full path