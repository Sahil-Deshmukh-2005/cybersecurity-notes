***

# Switches 
Switches are like connectors, which connects multiple devices with each other and where they are connected i.e. ports.  

```
    frame
      🖼️->      1 switch 3
 💻 ➡️➡️➡️➡️➡️➡️➡️ 🔳 ⬅️⬅️⬅️⬅️⬅️⬅️⬅️ 💻        Switch ports table :
  A                 ⬆️ 2               C                port 1 : MAC address of A
                    ⬆️                                  port 2 : empty
                    ⬆️                                  port 3 : empty
                    💻 B



                             frame
                1 switch 3    🖼️-> 
 💻 ➡️➡️➡️➡️➡️➡️➡️ 🔳 ⬅️⬅️⬅️⬅️⬅️⬅️⬅️ 💻        Switch ports table :
  A                 ⬆️ 2  frame        C                port 1 : MAC address of A
                    ⬆️    🖼️ ⏬                         port 2 : empty
                    ⬆️                                  port 3 : empty
                    💻 B



                              frame
                1 switch 3    <-🖼️ 
 💻 ➡️➡️➡️➡️➡️➡️➡️ 🔳 ⬅️⬅️⬅️⬅️⬅️⬅️⬅️ 💻        Switch ports table :
  A                 ⬆️ 2               C                port 1 : MAC address of A
                    ⬆️                                  port 2 : empty
                    ⬆️                                  port 3 : MAC address of C
                    💻 B
```

***

# Routers
Role of a router is to make communication between two different subnet devices.  
```
A                Switch             Router            Switch               B
💻 ➡️➡️➡️➡️➡️➡️➡️ 🔳 ➡️➡️➡️➡️➡️➡️➡️ ⬛ ⬅️⬅️⬅️⬅️⬅️⬅️⬅️ 🔳 ⬅️⬅️⬅️⬅️⬅️⬅️⬅️ 💻        Routing Table:
             192.168.1.0/24                       192.168.2.0/24                          192.168.1.0/24 = Fa0/0
                                                                                          192.168.2.0/24 = Fa0/1
```

***
