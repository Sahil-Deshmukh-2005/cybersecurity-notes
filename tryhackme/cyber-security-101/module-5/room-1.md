# Module-5 : Networking

## Room-1 : Networking Concepts

***

### OSI Model
1) Physical Layer :-  
Physical data transmission media.  
Ex., Electrical, Optical, and Wireless signals

2) Data-Link Layer :-  
Reliable data transfer between adjacent nodes in the same network.  
Ex., Ethernet and WiFi

3) Network Layer :-  
Logical addressing and routing between networks. Sending data between different networks.  
Ex., IP, ICMP, and IPSec

4) Transport Layer :-  
End-to-end communication and data segmentation.  
Ex., UDP and TCP

5) Session Layer :-  
Establishes, maintains, and synchronizing sessions.  
Ex., NFS, RPC

6) Presentation Layer :-  
Data encoding, encryption, and compression.  
Ex., Unicode, MIME, JPEG, PNG, MPEG

7) Application Layer :-  
Providing services and interfaces to applications.  
Ex., HTTP, FTP, DNS, POP3, SMTP, IMAP

***

### Ranges of Private IP Address
- 10.0.0.0 - 10.255.255.255 = (10.0.0.0/8)  
- 172.16.0.0 - 172.31.0.0 = (172.16.0.0/12)  
- 192.168.0.0 - 192.168.255.255 = (192.168.0.0/16)  

***

### Encapsulation 
Every layer in TCP/IP protocol attacks their own header and sometimes trailer to the packet. This process is called `Encapsulation`.  
```
                       |------------------|
Application Layer ---> | Application Data |
                       |------------------|


                     |---------------|------------------|
Transport Layer ---> | TCP/IP Header | Application Data |
                     |---------------|------------------|


                   |-----------|---------------|------------------|
Network Layer ---> | IP Header | TCP/IP Header | Application Data |
                   |-----------|---------------|------------------|


                     |----------------------|-----------|---------------|------------------|----------------------|   }
Data-Link Layer ---> | Ethernet/WiFi Header | IP Header | TCP/IP Header | Application Data | Ethernet/WiFi Header |     } Frame
                     |----------------------|-----------|---------------|------------------|----------------------|   }

UDP Used = UDP Datagram
TCP Used = TCP Segment

```

***







