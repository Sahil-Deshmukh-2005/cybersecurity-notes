***

As we use IPv4 and IPv6, we broadly use IPv4, but there are limited numbers of available IPv4 addresses.  
Therefore, what we do is we use 2 types of IPs, Private IP and Public IP.  
We use Private IPs in LANs, and we use Internet, services we convert that Private IP into Public IP.  
You might say how is this saving IPv4 addresses, we can use same IP addresses in different LANs.  

```
     |------------------------------------------|               |------------------------------------------|
     |   LAN1                    10.1.1.101     |               |     10.1.1.101               LAN2        |
     |                               💻         |               |         💻                               |
     |                               ⬆️         |               |         ⬆️                               |
     |                               ⬆️         |               |         ⬆️                               |
     |                               ⬆️         |               |         ⬆️                               |
     |                               ⬆️         |               |         ⬆️                               |
     |            A                Switch       |     Router    |       Switch               B             |
     |            💻 ➡️➡️➡️➡️➡️➡️➡️ 🔳 ➡️➡️➡️➡️➡️➡️➡️ ⬛ ⬅️⬅️⬅️⬅️⬅️⬅️⬅️ 🔳 ⬅️⬅️⬅️⬅️⬅️⬅️⬅️ 💻             |
     |         10.1.1.100            ⬇️         |      ⬆️       |         ⬇️             10.1.1.100        |
     |                               ⬇️         |      ⬆️       |         ⬇️                               |
     |                               ⬇️         |      ⬆️       |         ⬇️                               |
     |                               ⬇️         |   |-------|   |         ⬇️                               |
     |                               💻         |   |  NAT  |   |         💻                               |
     |                           10.1.1.102     |   | Table |   |     10.1.1.102                           |
     |------------------------------------------|   |-------|   |------------------------------------------|

```
This preserves IPv4 addresses.   
But Private IPs cannot access internet, Therefore we translate them to Public IP.

***

## NAT (Network Address Translation): 
As we saw we can use same IPv4 Addresses in different LANs but when we try to use the internet we cannot use these IPv4 addresses.  
Therefore we use NAT table which converts these IPv4 addresses i.e. 10.1.1.100, to much more releavent IPv4 addresses i.e. 209.165.205.5, then we can use the internet.  
```
          10.1.1.100 ----> Private IP
          209.165.205.5 ----> Public IP
```

### Static NAT 
Every private IP is mapped with it's own public IP address making it way more costly for companies.  

### Dynamic NAT
A public IP for a private IP is selected from the pool of public IPs.  
Unused ones are again put into the pool.  

***

## PAT (Port Address Translation):  
When responses comes back, which device should receive them.  
All private IPs can use same IP but they have to use different ports/port number.  
```
Original (Private)                     Translation (Public)
192.168.1.5:5000                       49.x.x.x:10001
192.168.1.6:6000                       49.x.x.x:10002

Same Public IPs but Different Port Numbers.
```

***
