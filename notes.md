# notes


## Week 1 – Learning the Shell
What is Shell? When we speak of the command line, we are really referring to the shell. The shell is a program that takes keyboard commands and passes them to the operating system to carry
out. Almost all Linux distributions supply a shell program from the GNU Project called
bash. The name “bash” is an acronym for “Bourne Again SHell”, a reference to the fact
bash is an enhanced replacement for sh

- Commands are often followed by one or more options that modify their behavior, and further, by one or more arguments, the items upon which the command acts. So most commands look kind
of like this: `command -options argument`. Most commands use options which consist of a single character preceded by a dash, for example, “`-l`”. Many commands, however, including those from the GNU Project, also support long options, consisting of a word preceded by two dashes. Also, many commands allow multiple short options to be strung together. In the following example, the
`ls` command is given two options, which are the `l` option to produce long format output,
and the `t` option to sort the result by the file's modification time. `[me@linuxbox ~]$ ls -lt`

- In Linux, the `$` symbol in a prompt usually indicates that you are logged in as a regular user.

- If you're logged in as the root user (superuser), the prompt will typically use a `#` instead.

- The first directory in the file system is called the root directory

- Note that unlike Windows, which has a separate file system tree for each storage device, Unix-like systems such as Linux always have a single file system tree, regardless of how many drives or storage devices are attached to the computer. Storage devices are attached (or more correctly, mounted) at various points on the tree according to the whims of the system administrator, the person (or people) responsible for the maintenance of the system.

- Absolute Pathnames(fix navigation), Relative Pathnames(., ..) In general, if we do not specify a pathname to something, the working directory will be assumed.

- Filenames and commands in Linux, like Unix, are case sensitive. Filenames that begin with a period character are hidden. This only means that `ls` will not list them unless you say `ls -a`.

- Linux has no concept of a “file extension”(.pdf , .txt).

- Though Linux supports long filenames that may contain embedded spaces and punctuation characters, limit the punctuation characters in the names of files you create to period, dash, and underscore. Most importantly, do not embed spaces in filenames. If you want to represent spaces between words in a file-name, use underscore characters.

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

Option Long Option Description
-a --all List all files, even those with names that begin
with a period, which are normally not listed
(that is, hidden).

`-a`, `--all` List all files, even those with names that begin
with a period, which are normally not listed
(that is, hidden).

`-A`, `--almost-all` Like the -a option above except it does not
list . (current directory) and .. (parent
directory).

`-d`, `--directory` Ordinarily, if a directory is specified, ls will
list the contents of the directory, not the
directory itself. Use this option in conjunction
with the -l option to see details about the
directory rather than its contents.

