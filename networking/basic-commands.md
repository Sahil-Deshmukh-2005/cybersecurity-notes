# Basic Networking Commands 

***

## ip a
`ip a` or `ip address` is used to get the IP address, MAC address of the machine.  
1) lo :  
local address, which means your own machine.  
`127.0.0.1` is the IP address or we can also use `localhost`.  
  
2) wlo1 :  
If we are using wifi adaptor we'll also see this.  
`10.256.168.192` is your local IP address.  
  
***

## hostname -I
It shows your IP and MAC address.  
Output: `<IP address> <MAC address>`

***

## ping 
```bash
ping google.com
```
This is used to check the connectivity between your machine and the server.  
`Ctrl+C` to stop the command.  

Better command:  
```bash
ping -c 4 google.com
```
This only sends 4 packets and then stops itself.  

***

## ss -tulnp
Modern command for viewing network connections and listening ports.  

```
ss = Socket Statistics
-t = TCP
-u = UDP
-l = listening ports
-n = shows numbers directly
-p = shows processes using ports
```

***

## netstat -tulnp
This is the older version of `ss`.  

***

## nmap 
nmap = network mapper

shows :  
  open ports  
  services  
  and also operating systems  

```bash
nmap scanme.nmap.org
```

scans host `scanme.nmap` and returns open ports, services, ......

```bash
nmap localhost
```
This scans your own machine.  

***

## traceroute
Shows the path packets take through routers to reach a destination.  

```bash
traceroute google.com
```

***

