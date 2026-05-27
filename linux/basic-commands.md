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

## 11. whoami
```bash
whoami
```
Returns the name of the current user.

***




