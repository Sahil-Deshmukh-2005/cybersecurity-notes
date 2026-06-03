# Nmap = Network Map

Nmap is a network scanning tool.  
- active services
- open/close ports

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

This is intentionally provided for practice.  
This is Nmap's test target.  

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
nmap -sn <IP Addr>
```
This finds all the live devices on the local network(IP Addr).  
You can check your IP address by,
```bash
ip a
```
Put your IP in `IP Addr`.  

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
T5 ----> Very aggressive  
  
T3 or T4 are fine.

***

## Specific Ports
```bash
nmap -p 80,443 scanme.nmap.org
```
This will only scan ports 80 and 443.  




