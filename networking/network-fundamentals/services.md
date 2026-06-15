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
