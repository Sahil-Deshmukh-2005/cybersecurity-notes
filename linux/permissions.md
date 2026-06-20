# Permissions Settings

***

r - Read - 4  
w - Write - 2  
x - Execute - 1  

***

## There are three types of users   
1) Owner  
2) Groups  
3) Others  

```
-rwxrw-r--
rwx = Owner
rw- = Groups
r-- = Others
```
Group of 3.  

***

## Numeric Permissions and chmod 
```
drwxr-xr-x 2 john staff.......
-rw-r--r-- 1 sudo staff.......
```
d = directory   
\- = file

r = 4, w = 2, x = 1  
  
We add these to give permissions to different types of users.  
```
chmod 755 notes.txt ----> -rwxr-xr-x
chmod 777 notes.txt ----> -rwxrwxrwx
```

***

## Ownership and Groups
### chgrp
```
chgrp <group> <file/directory>
```
Ex,  
```bash
chgrp sales report.txt
chgrp sales Soap
```
### chown
  
```
chown <user> <file/directory>
```

Ex,  
```bash
chown alice script.py
chown alice:devs script.py
```

***

## ACLs (Access Control Lists)
Special permissions.  
```bash
sudo apt install acl
```
#### Commands 
```
setfacl -m u:alex:rw reports.txt ----> -rw-r--r--+...
getfacl report.txt
```

***

## How Linux Evaluates Permissions?
```
Accessing File/Directory?
      ↪️ Is Owner? ---> Owner Permissions
      ↪️ Has ACL user entry? ---> ACL user Permissions
      ↪️ Is in Group? ---> Group Permissions
      ↪️ Maths ACL group? ---> ACL group Permissions
      ↪️ Others? ---> Others Permissions
```

***

