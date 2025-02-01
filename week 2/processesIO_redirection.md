# processes I/O redirection

the point of file is to keep the data persisit,

os(in the middle) provide abstraction to application(top), bottom is hardware

`stat` to look at metadata of a file, the inode hold the metadata of that file

`ls -l` also look at metadata of a file

the permission of a file divide into 3 categprty ( ownder, group, world/other)

check `whoami` to see which group you are

use `group` and `id` to see group

`chmod` to change the permission of a file, use to go back change permission back, `chmod +x`, change a program to be excutable

`umask` ?

-rw————(r readable, w writable, x excutable)

owner   group   world      octal number(raw octal code change bytes so can change permission of a file)

rwx         rwx.    rwx

110         000   000

111          1

where did i put that .c file?

`find` to find file search file system, 

a progam that search a string of text: `grep` ‘\.c$’

 ‘\.c$’. is a regular expression find classes | `grep` ‘\.c$’.  , `|` is a unix pipeline

`find classes | grep ‘\.c$’` find 

when you create a unix pipline, you have 2 process, 2 file that communicate, pipe help them communicate. conneting 2 files. this is the unix fossary action(take basic program to do basic things, and connect them through pipie). you can mix and match programs that connect, like connect legos together

`find classes | grep ‘\.c$’` 

every program you run is called a process, process is a loaded instance of a program. a program is a set of insructions. this set of instructions live in a file

which `ls` figure out where ls is, ls is also a file

to go from a program to a process, move it from disk to memory(ram). why load it into memory? cpu do the work. a program sittng in a file system, load in into memory, cpu fetch it from memory to execute. process is a instance of a program, get a instance of program and run it on the cpu

every process have 3 file

what program am i running?

`control + z` tell a program to pause

`ps` see all program you shell are running 

`ps ux` show all programs belong to you

a process is another abstraction os provide to user, `ps ux` is giving the metadata about the process. the metadata PID to identity a process

`kill -9 + (PID`) to kill a program, 

how do you save the results of a command?

`find classes > output` redirect a file

`find classes | tee output2` tee print out to terminal and write to file at the same time

`diff` tell if 2 files are the same(if diff don’t say anything, you’re good, linux more of the same)

`sha1sum` ou?

a hash function?

`find /etc` , etc contain configuration files

`find /etc &> combined`  combined permission denied file. redirect standout to combine file, take standout move it to combine. move standir to wherever stand at

`/dev/null` is like the trash bin, redirect to here for trash

how do you spam your friends terminal?

`who` to see who is on the machine

`write (username) + message`, control + D to end input

`cowsay hi`

`cowsay -f tux hi`

`mesg n` block

how do i terminate a process

`kill -9 + (PID`) to kill a program,