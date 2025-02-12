`tmus`: open window side by side, split up terminal to set up windows

`ps aux` to view all processes on a program,  `top` to see interactiver, `htop`

`tmus`: it does not lose you work even if you close your computer, `tmus attach`

`vim hello.sh`, to print. echo “” hello world”. `chmod + x hello.sh`, make the file exectuable

`sh hello.sh`, is an interpreter, `bash`is also interpreter.  `Bash is more complex than SH`

on the top of the file, shabang: `@#!/bin/sh` tell the OS how to interpreter this file, on the top of the file, shabang control how that program is interpreteed.

you need to export environemnt variable for shell script first, if you remove the variable, shell script return empty string access an variable does not exist. it does not return an error, which is tricky.

Shell:

NAME=$(NAME:-Anonymous)

echo”Hell0,$Name!”

case $Name in

mayleen) GREETING=heelo ;;

victoria)  GREETING=hola ;;

*) GREETING=hi;;

esac

env Name = Victoria ./hello.sh, env changes the instance of this program, but the main name is still not victoria

echo “Today is $()” 

date

with in shell script, you can capture another program output and see it as a string,

`$()` is called command substution, can also use `‘’`

curly braces around variable also works, you don’t have to 

case $Name in

mayleen) GREETING=hello ;;

victoria|tori)  GREETING=hola ;;

*) GREETING=hi;;

esac

`**tori**) GREETING=hola ;;` ????

`case` is like the Switch statement in C

in C programming Main, return 0 is exit status, 0 means successful

check metadata file, use `stat`

`echo $?` check status??? when return 0 success, when return 1 failed

#!/bin.sh

if stat $1  &> /dev/null; then

echo FILE exist!

else

echo FIle does not exist!

fi

reriect error message as well

chmod + x ./exists.sh





relative path 

2 dots to go back to parent directory

1 dot means the current location

`pwd` to see the absolute path

shell scripts run line by line, bail out hits an error

always the first line of every script is a shabang, the line tell OS what program to use to interpreate this file

- echo $PATH, why use `./` ?

export PATH

check the exit code of prirevous command: `echo $?`, if return 0 file exist(success), non 0 means failure

- redirect out put to throw it away  `> / dev/null 2>&1`, redirect stdout to stdin? why it need 2>&1, redirect stdir out first.
- use `stat` and `test` to see if a file exist: `test -e [hello.sh](http://hello.sh)` , test by default don’t print anything, just `echo$?`, you can use`[ ]` to call test comamnd: `if [ -e hello.sh ]; then`

```python
echo argc: $#
echo argv” $0

EXITCODE=0

check_file(){
if [ -e "$1" ]: then
	echo we have $1
else
	echo Missing $1
	EXITCCODE=$(($EXITCODE + 1))
 fi
 }
 
 '' to group argument, differnt betwen single and douvle quotes
 for argument in "$0": do
	 check_file "$argument"
 done

you should double quotes your variable for good practice, you can then group them?
```

```python
<<comment
...
comment

echo old argv: $@

while [ $# -gt 0]: do
	check_file "$argument"
	shift
done

echo new argv: $@

exit $EXITCODE
```

- `sh -x`  to trace the command
- what is $@?
- shift, take the first thing out, put second things at front as the first thing, this is a data structure of queue, whenu shift, you popping from the front of queue, until it’s empty

`cat` reads from stdin and read it back out





`curl` to pull down data, `wc` to count 

use the filter of regular expression to struct a unix pipe line

review shell script:

`tr` is a mapping program, take one set and map onto another\

`echo unix is so cool | tr a-z A-Z`

unix philosophy(why? scaliing and specialize/optimze for a task):

1. write programs: do one thing and do it well
2. write programs: work together
3. write programs: communicagte in plan text

unix pipl line is a digital pipeline of assembly line, you want o scale and take advantage of resrouces, that’s why you use unix pipeline

1. STAGE 1, gather/read data
2. stage 2, filter and select
3. stage 3, aggregate and count

get text from `ls`, extract text from `ls` : `strings`

we have cpu cores on computer, by putting thing in a pipleline, you are introducing concurrency, by creting a strcture you are building concurrecy that you can do things at the same time. (Parallel computing)when you doing unix pipeline, you are doing parrell computing.

how many instances of bash?zsh?sh?

`ps aux` , `ps aux | grep bash`,  `ps aux | grep bash | wc -l`, `ps aux | grep -v grep | grep bash | wc -l`, `ps aux | grep -v grep | grep -Eo '(bash|tmux)' | sort | uniq -c`

who has the most processes?

`ps aux | cut -d ‘ ’ -f 1 | sort | uniq -c | sort -n | head -n 5`