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

