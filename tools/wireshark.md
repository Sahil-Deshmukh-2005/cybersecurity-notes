# WireShark

Wireshark captures and analyzes the network packets.  

***

## What are packets? 
The data to be transfered is broken down into pieces, those pieces are called `packets`.  

***

## Steps to start WireShark
```bash
wireshark
```
Then,  
Select one interface, graphes will be visible beside the active interfaces.    
Then,  
Either open a website through browser or `ping` a website.  
  
This will start generating traffic, every packet will be visible on the wireshark.  

***

## Columns
```
No. ----> Packet Number
Time ----> Time Stamp
Source ----> Sender
Destination ----> Receiver
Protocol ----> Protocol Type
Length ----> Packet Size
Info ----> Summary
```

***

## Important Protocols
### ICMP 
Used by `ping`.
  
### DNS
Used for domain lookup.  
  
### TCP/UDP
Main communication protocols. 
  
### HTTP/HTTPS
Protocol to transfer data across internet.  

***

## Inside a Packet
Click on a packet.  
You'll see 3 sections at the bottom.  
  
### Section-1
This shows the summary of the packet.  
  
### Section-2
This tells the packet details.  
  
### Section-3 
This shows the raw packet bytes.  

***
