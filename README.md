# bash-assignment
Assignment 2: bash scripting exercise

### Question 1
How many processes are currently running on your system? Use ps and wc, the first line of output of ps is not a process!
ps -e | wc -l

### Question 2
Write a script that upon invocation shows the time and date, lists all logged-in users, and gives the system uptime. 
The script then saves this information to a logfile.

code
```
datetime= 'date'
users= 'who'
system='uptime'
  echo date and time: $datetime
  echo logged in users: $users
  echo system uptime: $system
```
   
### Question 3
Which command would you use in order to create an empty file in the current directory, let's say empty.txt?
touch empty.txt

### Question 4
You are in /home/icipe/  suppose this directory is empty. How do you create in only one command the whole path /home/icipe/Work/mini-project/RNA-Seq/?
mkdir -p mkdir -p home/icipe/Work/mini-project/RNA-Seq/

### Question 5
Suppose your current working directory contains a file named seqs.txt. How do you rename this file into sequences.fasta? 
Does this have any effect on the content of the file, and if yes, what does it do?

mv seq.txt sequence.fasta



