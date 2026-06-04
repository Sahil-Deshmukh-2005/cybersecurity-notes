# Basic Commands
Linux basic commands to use in daily file.

***

## 1. pwd = Print Working Directory
It returns current working directory.
```bash
pwd
```

***

## 2. ls 
```bash
ls
```
It returns all the files, directories present in current directory.  
❗This does not show the hidden files, directories.

```bash
ls -a
```
This will return all the files.(including hidden)

```bash
ls -l
```
This returns long listing format of all the files, directories.  
❗This does not show the hidden files, directories.

```bash
ls -la
```
or  

```bash
ls -al
```
This will return long list format of all the files(including hidden).

```bash
ls Documents
```
This returns the files, directories in the Documents directory.

***

## 3. cd = Change Directory
This is used to change the directory you are working in.  
❗The directory you are changing in should be present in current directory.
```bash
cd Documents
```
Changes the working directory to Documents.

```bash
cd ..
```
Goes to previous directory.

```bash
cd
```
Goes back to the home directory.

```bash
cd Documents/Projects
```
Can change multiple directories at once.

***

## 4. history
Shows the history of the commands in the terminal with a sequence number, and the numbers could be used to run the command at that particular number.
```bash
history
```
### Output 
```bash
101 pwd
102 cd Documents
103 ls
104 ls -a
```
We can run the commands by using the index number.
```bash
!101
```

***

## 5. touch
```bash
touch notes.txt
```
It is used to create a file.

```bash
touch notes1.txt notes2.txt
```
We can create multiple files too.

***

## 6. mkdir = Make Directory
Same as its name , it is used to create directory.
```bash
mkdir Projects
```
Creates Projects directory in current working directory. 

```bash
mkdir Folder1 Folder2
```
Creates multiple directories.

❕Important 
```bash
mkdir -p Work/2026/Tasks
```
Creates the parent directories if its not present.  

***

## 7. nano 
```bash
nano file.txt
```
It is used to open/edit a file in the terminal.

***

## 8. vim
```bash
vim file.txt
```
`Vim` is a text editor similar to vs code it has its own different language.

***

## 9. cat, less, head and tail
```bash
cat notes.txt
```
It returns the content of the file in the terminal.  
❗Cannot see long text or content.

```bash
less notes.txt
```
Same as `cat` but also work for long content.

```bash
head notes.txt
```
It returns first 10 rows of the file to the terminal.

```bash
head -20 notes.txt
```
It returns first 20 rows of the file.

```bash
tail notes.txt
```
It returns last 10 rows of the file.

```bash
tail -5 notes.txt
```
It returns the last 5 rows of the file.

***

## 10. echo
```bash
echo "hello nakama"
```
It prints the `hello nakama` to the terminal.

***

## 11. whoami
```bash
whoami
```
Returns the name of the current user.

***

## 12. uname = Unix name
```bash
uname
```
It returns the system name. Ex, Linux

```bash
uname -a
```
It returns the brief information about the system.

***

## 13. uptime
```bash
uptime
````
It returns the total time the machine was awake.

*** 

## 14. cp = Copy
As the name suggest it is used to copy files and directories.  
```bash
cp <File to be copied> <Destination>
```
For Example, 
```bash
cp file1.txt file2.txt
```
This copies the content of file1 to file2.  

```bash
cp notes.txt Documents
```
This copies the notes file to Documents directory.  

```
-r = recursive
-i = asks/ confirms
-v = verbose or we can say that it visually shows whats going to happen.
```
Example, 
```bash
cp -r Projects Backup
```
This recursively copies files from Projects to Backup directory.  

```bash
cp -v file1.txt file2.txt
```

This shows whats going to happen  
```
file1.txt ----> file2.txt
```


```bash
cp -i file1.txt file2.txt
```

This asks first before coping the content, type `Y` if YES and `n` if NO.

***

## 15. mv = move

This is used to move a file/directory.  
It can also be used to rename a file.  

```bash
mv reports.txt Documents
```
This moves reports file to Documents directory.

```bash
mv old_name.txt new_name.txt
```

This renames the file.  

```
-v = verbose
-i = asks/ confirms
```
❗Note that you cannot use -r(recursive) to move files/directories.   

Examples,  
```bash
mv -v draft final
```

This shows:
```
draft ----> final
```

```bash
mv -i final summary
```

This asks before moving.  

***

## 16. rm and rmdir = Remove and Remove Directory
Same as name suggest it is used to remove or delete a file/directory.

```bash
rm notes.txt
```
Removes notes file.  

```bash
rmdir Empty_folder
```

This removes empty folder.  
❗Note that the folder/directory should be empty, it'll not delete if folder has something in it.  

```
-r = recursive
-v = verbose
-i = asks/ confirms
-f = force
```

```bash
rm -f main.txt
```
Force remove main file.

```bash
rm -rf Projects
```
Recursively remove by force from Projects directory.

***

## 17. sudo = Superuser do
I never thought this would be the expansion of abbreviation `sudo`.  

`sudo` is used to remove the permissions from a file/directory. It lets the user use the file/directory or execute it normally.   
This gives administrator rights to the user.  
   
```bash
sudo ls /root
```
But here sudo asks for password of user:
```
[sudo] password for username:
```

***
## 18. chmod and chown = Change Mode and Change Owner

We'll discuss about this in `permissions.md`.  
This is just an overview.  

```bash
chmod +x script.sh
chmod 644 exam.txt
chmod 755 shared_folder
sudo chown username report.txt
sudo chown user:group Project
```
These are few examples of how a file/Directory permissions can be manipulated.  

```bash
ls -l
```
This command lets you see the permissions of each file/directory.  

***

## 19. find
Same as its name, its used to find file/directory.

```bash
find . -name notes.txt
```

Here `.` mean everything, so it mean search everything and find the file notes.txt

```bash
find . -iname README.md
```

`-iname` means case insensitive.  

```bash
find Projects
```

Returns path of Projects directory.  

***

## 20. locate
Similar to find but faster, as locate searches in the database.  

```bash
locate notes.txt
```
Returns path for notes.txt

```bash
locate -i README.md
```
Case insensitive 

❗Note that it might might not locate sometimes as it searches from the database. sometimes the database is not updated, so if you get an error, just run the following command.  
```bash
sudo updatedb
```

This updates the database.  

*** 

## 21. grep
Used to search particular word/line in a file.  
 ```bash
grep "Alex" text.txt
```
This returns the lines with word Alex

```bash
grep -n "Alex" text.txt
```
This returns the output with order number.  

```bash
grep -i "alex" text.txt
```
This is case insensitive form.  

```bash
grep -r "error" Logs
```
This performs resursive search over the entire Directory.  

***

## 22. df -h AND du -sh
Simply means,  
```
df = Disk Free
du = Disk Usage
```

here   
```
-h = human readable, if you dont put h itll show size in kb
-s = summarize
```
Commands:
```bash
df -h
```
  
```bash
du -sh
```
***

## 23. top
This gives us realtime analysis of running processes.  
top - Table of Processes

```bash
top
```
This has a better interface version called, htop, goof for human readability.  
First install htop.  
```bash
sudo apt intall htop
```
```bash
htop
```

Q - Quit

***

## 24. ps aux
This is the snapshot of all the processes running currently.  
ps - process status
a - of all users
u - detailed user oriented format
x - process without terminal too (background)

```bash
ps aux
```
If you want processes of particular user

```bash
ps -u Alex
```

***

## 25. sudo apt
Last time we saw what sudo does, using it now we can manipulate packages.  
apt - Advanced Package Tools

```bash
sudo apt update
sudo apt upgrade
sudo apt install htop
sudo apt remove htop
sudo apt autoremove
```

***

## 26. man AND --help 
man - mannual  
Both does the same job.  
  
```bash
man ls
```
```bash
ls --help
```
This gives the mannual of ls command.  

Q - Quit

*** 

## 27. alias
Rename the commands as you want.  
Temporarily stored for current session once you shutdown the device it resets.  

```bash
alias ll="ls -l"
ll
```

Now you can use `ll` to run `ls -l`.  

```bash
alias
```
Shows all the renamed commands.  

```bash
unalias ll
```
Removes the alias `ll` for the command.  

***

## 28. wget
```bash
wget <URL>
```
Download using URL

```bash
wget https://files.example.com/manual.pdf
```
Downloads manual.pdf  

```bash
wget -O notes.pdf https://files.example.com/manual.pdf
```
Renames while downloading.  

```bash
wget -b https://files.example.com/manual.pdf
```
Used to download in background.  

***

## 29. tar
Consider it as zip.  

```bash
tar -czf backup.tar.gz Projects
tar -xzf backup.tar.gz
tar -tf backup.tar.gz
```

```
c - Create
x - Extract
t - List Contents
z - Use gzip Compression
f - Specify file name
v - Verbose (show files)
J - xz Compression
```
***

## 30. kill AND pkill AND killall
Used to terminate the processes using their PID (Process ID)  
```bash
kill <PID>
```
Terminated the process.  

```bash
kill -9 <PID>
```
Immediate termination.  

```bash
pkill <PName>
```
Kills all the processes with Process name = PName.  
Ex, pkill chrome  
```bash
pkill -9 <PName>
```
Force Kill.  
❗But keep in mind that pkill matches the process name partially that means it can easily kill some other processes too.  

```bash
killall <PName>
```
This is safer than `pkill`, it exactly matches the name and then only kills the process.  

***

### This is the END of basic commands, these are not all of them, but very useful in day-to-day life.  
### There are still some networking commands that well cover in networking.  









