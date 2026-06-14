# Transport Layer

## Protocols

***

TCP = Transmission Control Protocol  
UDP = User Datagram Protocol  

***

### TCP 
Connection Oriented.  
It first has to make connections to start conversation.  
It first asks server for connection, server acknowledges the request sends back to client, then client sends back the acknowlegement back to server.  
Its called 3-way handshake.  
```
    Client                       Server  }
      | SYN                        |      }
      |--------------------------->|       }
      |                   SYN + ACK|        } After this the communication starts.
      |<---------------------------|       }
      |ACK                         |      }
      |--------------------------->|     }
```

Its slow because it has to make connections before starting communication, but its reliable where you need to make sure data reaches the server.  

***

### UDP 
It does not care about connection.  
It just sends the packet or data at the server with no care if itll catch it or not.  
```
          |--- ✉️ ------->
    💻  ------ ✉️ ------->    🗃️
  client  |--- ✉️ ------->  server
```

***

#### We use TCP if we want accuracy and dont care about the speed.  
#### We use UDP if we only care about the speed and dont care if packet id lost.  
#### A system can have both TCP and UDP sessions.  

***

### TCP/IP Applications and ports
1) FTP (File Transfer Protocol) = 21
2) SSH (Secure Shell) = 22
3) Telnet = 23
4) HTTP = 80
5) HTTPS = 443
6) DNS = 53
7) TFTP = 69
8) SNMP = 161

***

### Flooding 
A flooding is a process in which a Switch A boradcasts the frames to its neighbouring switches i.e. B,C.  
Then those switches broadcasts the frames to their neighbour except where it came from.  

***

