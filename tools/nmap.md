# Nmap = Network Mapper

Nmap is a network scanning tool.  
- active services
- open/close/filtered ports

***

## TCP vs UDP
Why this is important because `nmap` uses `TCP` scans or `UDP` scans.  
### TCP = 

***

## Ports
A computer can run many network services.  
Each service uses a port.   
```
HTTP ----> 80
HTTPS ----> 443
SSH ----> 22
FTP ----> 21
```

A port is like a door.  
If a door is open ----> A service is listening   

***

## Command
```bash
nmap <target>
```
Target can be an IP, Domain name, ..

```bash
nmap 127.0.0.1
```
or 
```bash
nmap localhost
```

This scans your own machine.  

```bash
nmap scanme.nmap.org
```
This is a basic TCP scan.  
This target is intentionally provided for practice, and is Nmap's test target.  

***

## Result
The result somewhat looks like this:
```
22/tcp open ssh
80/tcp open http
```

Here, 
```
22 = port
tcp = protocol
open = state
ssh = service
```

***

## Service Version Detection
```bash
nmap -sV scanme.nmap.org
```

This is used to identify the versions of the services.  
Its usefull because versions may contain vulnerabilities.  

***

## Fast Host Discovery 
```bash
nmap -sn <Subnet Addr>
```
This finds all the live devices on the particular subnet.  
You can check your IP address/Subnet by,
```bash
ip a
```
This will return,  
```
inet 192.168.1.5/24
```
So,  
Your IP = `192.168.1.5`  
and your Subnet is `192.168.1.0/24`  
Put your Subnet in `Subnet Addr`.  

Ex,  
```bash
nmap -sn 192.168.1.0/24
```

Youll see:
- routers
- VM
- laptop
- phones (maybe)

***

## Timeing Templates
Faster scan timing
```bash
nmap -T4 scanme.nmap.org
```

Templates:  
T0 ----> Very slow  
T1 ----> Sneaky  
T3 ----> Normal  
T4 ----> Faster  
T5 ----> Very aggressive  
  
T3 or T4 are fine.  
  
You might ask why these templates are even useful as we can always use `T4` for faster scans.  
#### Faster Scans 
- Finishes quickly
- Generates more traffic
- are easier to detect

#### Slower Scans
- Quieter
- Stealthier
- takes more time

This becomes important later with:  
- IDS
- IPS
- Firewalls
- Detection System

***

## Scan Ports
### Scan Specific Ports
```bash
nmap -p 80,443 scanme.nmap.org
```
This will only scan ports 80 and 443.  

### Scan Range of Ports
```bash
nmap -p 1-100 scanme.nmap.org
```
Scans ports from 1 to 100

### Scan all Ports
```bash
nmap -p- scanme.nmap.org
```
Scans All the ports.  

```
❕Important 
There are 0-65535 i.e. 65536 ports available in total.
```





