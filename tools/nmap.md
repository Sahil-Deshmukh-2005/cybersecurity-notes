# Nmap = Network Mapper

Nmap is a network scanning tool.  
- active services
- open/close/filtered ports

***

## TCP vs UDP
Why this is important because `nmap` uses `TCP` scans or `UDP` scans.  
We will cover about this in depth in `networking`.  
  
### TCP = Tranmission Control Protocol
This protocol is used when you want relaiable connection.  
`TCP` first makes the connection with the reciever before sending data, this is called 3-way handshake.  
Due to this its slow, as it first has to make connection, but it ensures the data reaches the reciever.  
  
### UDP = User Datagram Protocol
This protocol is used when you want lower `Latency`.  
`UDP` directly starts throwing packet at the reciever no matter if the reciever catches it, packet may get lost while transferring and client wouldnt even know that.  
Faster than `TCP` as it does not care abot connection.  

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
`-sn` means Ping Scan.  
This finds all the live devices on the particular subnet.  
This does not perform port scanning.  
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

***

## States
```
open -----> Listening
close -----> Reachable but unused
filtered -----> Firewalls/ security filtering
```

***

## UDP Scan
As we saw normal `nmap` without flags is a basic `TCP` scan.  
Now lets see for `UDP` scan,  
```bash
sudo nmap -sU scanme.nmap.org
```
Why `sudo`, because `-sU` flag requires root privileges.  
⚠️ Its too slow, you can run the command go make some food, eat it, wash the dishes, then come back and itd still be running.  

***

## Scan Multiple Targets
```bash
nmap <ip_addr_1> <ip_addr_2> .....
```
You can put as many as you want.  
Ex,  
```bash
nmap 192.168.1.1 192.168.1.5
```

***

## Scan ranges of IP
```bash
nmap 192.168.1.1-20
```
This scans IP from `.1` to `.20`.  

***

## Multiple Flags
You can use multiple flags(-sn, -v, -T3, -p, etc...) at once.  
```bash
nmap -T4 -p 22,80,443 scanme.nmap.org
```
Scans specific ports faster.  

***

## Latency
```
`Latency means Response time ⏲️.
```
Output 
```
Host is up (0.0031s latency).
```
This means Response took 3.2ms.  

***





