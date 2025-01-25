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

Reading week 1

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

`less` Displays a file's content one screen at a time, allows us to scroll forward and backward through a text file.

`pwd` Prints the current working directory's full path

ssh hwang@jumpbox.nd.edu

ssh student10.cse.nd.edu

terminal use ssh to talk to student machine

bash interpretuer reads command and tranlaste into actions

on git, fork create a new origin of OG file, to make a copy, run git clone(now 3 copies, the og, the online the one locally on your machine). when you clone to local machine, it’s gonna create a checkout that will checks out a working directory. then you use git add to tell git, to keep tracking of the changes(it’s added to staging area now, kinda like gmail draft mode), once you happy with draft, you make commit to save it to git log(local). git log have bunch of transactions. you then push the changes(local to cloud). you do a pull to see the changes being made on your cloud file

see the changes other made, `pull`

ready to add things/save things ,`add/commit`

all done, do a `push`

**`stdin`** stands for **standard input**. It is one of the three standard streams used in Unix-like and other operating systems for input/output operations. It acts as the default source from which a program reads its input.

`git switch` main branch, `git pull —rebase`, to pull the changes. then create a new branch `git checkout -b reading01` ( waht does rebase do??)

`git log` to read entries

`git branch` check out which branch you’re on

`git checkout -b reading01` create a new branch

`git checkout` do multiple thingm `git switch` only switch to a branch

git add and git commit diff???

`git restore` go back to the previours version, throw away all changes you made

traversal is the process of systematic visiting each elment in data scturecture(BFS, DFS)

for BFS, we use Queue(First in first out), for DFS, we use Stack(last in first out)

Iterative deepening search(IDS). call DFS for different depths, starting from an initial value. in every call, DFS is restricted to that depth(search entire level with DFS). we use Stack for IDS. due to using stacj, we retian

pruning involves removing branches of the tree that do not need to be expolosred, thus reduce the search space and improving effciency

shell is a interpreturor, what is Shell?

shell is application use libraries to talk to os and then os talk to hardware,

operating system talk to hardware on shell’s behave

memory is just address with label

comp arc, programming paradigms

fc/ds/pp(application)

sp.os(libraries, os)

every program exist in a file system

`lsblk`

`whoami`

`id -a`

`su pbui`

`suedo` change account?

`.` file start with . is a hidden file

`ls -l`

`stat`

what is bashrc

`tree`

`cat`

`file` determine a file's type

`cp` – Copy files and directories
`mv` – Move/rename files and directories
`mkdir` – Create directories
`rm` – Remove files and directories
`ln` – Create hard and symbolic links

how do i create a short cut to a file.directory

ln abc or stat abc*

create a soft link?

softlink contains tha path to the original file?, it’s content is the name of the file

softlink when u open it, you follow the link to the original destination

softlink is less effcient, take more space, the benifit of softlink can access other file system, otherwise use hardlink

![Screenshot 2025-01-18 at 7.13.28 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/e9aa5cb4-3732-470f-8eea-daed9eaaa042/Screenshot_2025-01-18_at_7.13.28_PM.png)

![Screenshot 2025-01-18 at 7.13.49 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/b8640935-d6b9-4170-b040-2dd203b367cd/Screenshot_2025-01-18_at_7.13.49_PM.png)

![Screenshot 2025-01-18 at 7.14.04 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/56e0bffe-c901-4f8d-bf89-a371d4600dba/Screenshot_2025-01-18_at_7.14.04_PM.png)

![Screenshot 2025-01-18 at 8.21.05 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/e6464631-1bc7-49b8-ba42-4b2aa9c44849/Screenshot_2025-01-18_at_8.21.05_PM.png)

![Screenshot 2025-01-18 at 8.21.16 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/7be248c1-8c4b-4d20-bc6d-602a6e9d881e/Screenshot_2025-01-18_at_8.21.16_PM.png)

wildcard:

Since the shell uses filenames so much, it provides special
characters to help us rapidly specify groups of filenames. These special characters are called wildcards. Using wildcards (which is also known as globbing) allows us to select filenames based on patterns of characters. Table 4-1 lists the wildcards and what they select.

![Screenshot 2025-01-20 at 3.32.36 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/2887dfcc-e489-4280-b595-226153d424e5/Screenshot_2025-01-20_at_3.32.36_PM.png)

![Screenshot 2025-01-20 at 3.32.49 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/c923c6c8-fbe2-487b-9c33-1845be61530d/Screenshot_2025-01-20_at_3.32.49_PM.png)

ln – Create Links
The ln command is used to create either hard or symbolic links. It is used in one of two ways. The following creates a hard link: `ln file link` The following creates a symbolic link: `ln -s item link`

Hard Links
Hard links are the original Unix way of creating links, compared to symbolic links, which are more modern. By default, every file has a single hard link that gives the file its name. When we create a hard link, we create an additional directory entry for a file. Hard links have two important limitations:

1. A hard link cannot reference a file outside its own file system. This means a link
cannot reference a file that is not on the same disk partition as the link itself.
2. A hard link may not reference a directory.

A hard link is indistinguishable from the file itself. Unlike a symbolic link, when we list a directory containing a hard link we will see no special indication of the link. When a hard link is deleted, the link is removed but the contents of the file itself continue to exist (that is, its space is not deallocated) until all links to the file are deleted. It is important to be aware of hard links because you might encounter them from time to time, but modern practice prefers symbolic links, which we will cover next.

When thinking about hard links, it is helpful to imagine that files are made up of two parts.

1. The data part containing the file's contents.
2. The name part that holds the file's name.

When we create hard links, we are actually creating additional name parts that all refer to the same data part. The system assigns a chain of disk blocks to what is called an inode, which is then associated with the name part. Each hard link therefore refers to a specific inode containing the file's contents.

Symbolic Links
Symbolic links were created to overcome the limitations of hard links. Symbolic links work by creating a special type of file that contains a text pointer to the referenced file or directory. In this regard, they operate in much the same way as a Windows shortcut, though of course they predate the Windows feature by many years.
A file pointed to by a symbolic link, and the symbolic link itself are largely indistinguishable from one another. For example, if we write something to the symbolic link, the referenced file is written to. However when we delete a symbolic link, only the link is deleted, not the file itself. If the file is deleted before the symbolic link, the link will continue to exist but will point to nothing. In this case, the link is said to be broken. In many implementations, the ls command will display broken links in a distinguishing color, such as
red, to reveal their presence

where is ls located?

/ root, use for system applications

-bin(binary) is applications

-dev is devices

-etc is configuration

-tmp is scratch base(public space anyone can use)

-var is use for application data

-usr is user folder, use for user application

inode store metadata about files and directories

every file have 3 groyps, what can user do, what can group do, what can world do

**softlink**: Programs don’t know or care about version numbers—they just look for the name **"Python."** The **soft link** (sign) makes it simple to manage updates without having to go around and fix every single program that uses **"Python."**

## Command

`type` – Indicate how a command name is interpreted
`which` – Display which executable program will be executed
`help` – Get help for shell builtins
`man` – Display a command's manual page
`apropos` – Display a list of appropriate commands
`info` – Display a command's info entry
`whatis` – Display one-line manual page descriptions
`alias` – Create an alias for a command

![Screenshot 2025-01-20 at 4.54.27 PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/85d9e183-3509-446c-8f99-e6f2c163695d/2d1e97e7-db3a-4086-97b7-97b0a5066b17/Screenshot_2025-01-20_at_4.54.27_PM.png)