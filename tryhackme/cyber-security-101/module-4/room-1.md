# Module-4 : Command Line

## Room-1 : Windows Command Line

***

```bash
set
```
This is used to get the current path.

***

```bash
ver
```
This gives the version of your OS.

***

```bash
systeminfo
```
This is used to get the information about the current system.  

***

```bash
ipconfig
```
This is used to get the IP address of your system.  

```bash
ipconfig /all
```
This gives more detailed information about your IP.  

***

```bash
ping example.com
```
This is used to check the connection between your machine and the server.  

***

```bash
tracert example.com
```
This gives the route of packet. (Packet means data which is segmented into multiple parts)  

***

```bash
nslookup example.com
```
It looks up for the Host's or Domain's IP address.

***

```bash
netstat
```
This gives the current network connection and listening ports.  

```
-a : displays all established connections and listening ports.
-b : shows the program associated with each listening ports and established connections.
-o : reveals the process ID (PID) associated with the connections.
-n : uses a numerical form for addresses and port numbers.
```
```bash
netstat -abon
```

***

```bash
cd
```
This gives current working directory.  

***

```bash
dir
```
This gives child directories.  

***

```bash
tree
```
This gives the tree like structure for current directory and subdirectories.  

***

```bash
cd Users
```
Change directory to Users directory.

```bash
cd ..
```
Get back to previous directory/Parent directory.

***

```bash
mkdir Projects
```
Creates Projects directory.

***

```bash
rmdir Projects
```
Removes Projects directory.  

***

```bash
copy test1.txt test2.txt
```
Copies content of `test1.txt` to `test2.txt`.

***

```bash
move test2.txt Projects
```
Moves test2.txt to the Projects directory.

***

```bash
del test1.txt
```
```bash
erase test2.txt
```
Deletes the files.  

***

```bash
tasklist
```
Displays current running processes.

***
