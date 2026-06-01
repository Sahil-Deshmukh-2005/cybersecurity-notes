# Module-2 : Networking Fundamentals

## Room-1 : What is networking 
Networks are simply things connected.  
Specifically in computing when 2 or more devices are connected it is called `network`.  

***
.
## Internet
Internet is made up of many small such networks. These small networks are called `private networks`, where they are being connected,`internet`, is called `private networks`.  
Evolution:  
1960 - ARPANET project  
1989 - World Wide Web, by Tim Berner-Lee

***

## Identifying Devices on a Network
### IP (Internet Protocol):  
It is used as a way of identifying a host on a network, for a period of time, where that IP can be associated with another device.  
`IPv4 : 192.168.1.1` each section is called octet, range of each section is 0-255.  
IP addresses follow set of standards/rule known as `protocols`.  
There are 2 types of IP addresses:
1) Public Address  
2) Private Address  
  
A `Public Address` is used to identify the device on the internet, whereas the `Private Address` is used to identify a device amongst other devices.  
Public IP addresses are given to a device by your `Internet Service Provider(ISP)`

### MAC (Media Access Control):  
Every device has a unique identifier called `MAC`, which is given to a device at the time of manufacturing.  
`MAC` is a 12 characters hexadecimal number, each seperated by colon(`:`).  
First 6 characters represent the company that made network interface and Last 6 characters are unique numbers to identify a device.  
Ex, a4:c3:f0:85:ac:2d  
However these `MAC` addresses can be faked or `spoofed` in the process known as `spoofing`. A device pretending to be other device using it's `MAC` address.  
Ex,  
```
A and B are on same network,  
and B has paid WiFi,  
So A can change its MAC address to B's MAC address and access the WiFi
```

***

## ping 
A tool to check the connectivity between source and target device.  
We can use the Domain name or IP address

```bash
ping google.com
```


```bash
ping 142.250.195.78
```

