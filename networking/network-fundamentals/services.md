# Services 

***

## ARP and RARP 
ARP = Address Resolution Protocol  
RARP = Reverse Address Resolution Protocol  
  
When a device A wants to communicate with device B in same LAN, it needs its MAC address.  
So it broadcasts the IP address of that device and the device returns it with its MAC address, this is known as `ARP`.  

`RARP` is reverse of `ARP`, its when a device has other devices MAC address and need their respective IP address.  

***

## DHCP 
DHCP = Dynamic Host Configuration Protocol  
  
This is a server/client protocol that automatically provides an IP address along with a subnet mask and default gateway.  
These things are allocated for limited period of time called `lease`.  
  
- Steps used by DHCP servers :
1) Discover : A broadcast discover message is sent out by the DHCP client to find DHCP server.
2) Offer : DHCP server replies back with offer message with an IP address.
3) Request : DHCP client accepts the IP address given by the DHCP server and sends back request message.
4) Acknowledge : DHCP server then sends DHCP client the IP address and subnet mask assigned to the DHCP client.

***

## DNS 
DNS = Domain Name System  
  
Instead of using IP address for website to remember we use human readable format i.e. domains, ex, `www.google.com`.  
The DNS helps to convert this human readable domain into numeric IP address, i.e. `142.251.156.119`.  
  
Command : 
```bash
nslookup www.google.com
```

This will show the IP address.  

***

## HTTP/ FTP/ SMTP/ Telnet and SSH/ RDP 
  
HTTP = Hypertext Transfer Protocol  
FTP = File Transfer Protocol  
SMTP = Simple Mail Transfer Protocol  
SSH = Secure Shell  
RDP = Remote Desktop Protocol  
  
All these protocols are for to transfer data across the internet.  

### HTTP 
We have learnt it already.  

### FTP 
Same as its name its used to transfer files.  
There 2 channels between client and server.  
1) Control Channel : Used for sending commands, responses, and other control information via TCP port 21.
2) Data Channel : Actual data is transferred via this channel.

### SMTP 
Used for mail transfer.  
  
Uses TCP port 25.  
But this is not secure, thats why we use,  
  
SMTPS = SMTP Secure, It uses TCP port 465 with SSL/TLS encryption.  

### Telnet and SSH 
Both are used for Remote Access Control (RAC),  
where one can use others device without physically being there. (Uses terminal securely)  
But Telnet is not so secure as it does not use encryption for login credentials. Therefore, we use SSH it is secure and uses encryption.  

### RDP
Same as Telnet and SSH.  
It gives access and control over other devices GUI.  
It uses TCP port 3389, But it can be changes for security purpose.  
RDP supports encryption.  

***
