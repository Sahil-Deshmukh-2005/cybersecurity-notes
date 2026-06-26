# OSI Model 

***

This is a theoretical model.  
How data travels from one computer to another.  
layer 7 ----> layer 1 = sending   
layer 1 ----> layer 7 = receiving  

## Layer 7 : Application Layer
Provides internet services directly to user application.  
This layer interacts with you.  
Ex., Browsers, Whatsapp  

## Layer 6 : Presentation Layer
Translates, encrypts and format data.  
Acts like a translator.  
Ex., HTTPS encryption  

## Layer 5 : Session Layer
Creates and manages communication sessions.  
Keeps conversations between devices active.  
Ex., Video call session

## Layer 4 : Transport Layer
Ensures reliable data delivery between devices.  
Responsible for:  
- Breaking data into pieces
- Reliability
- Flow Control
Ex., File download uses - TCP, gaming/video calls uses - UDP

## Layer 3 : Network Layer
Handles IP addressing and routing.  
Finds the path data should take.  
Ex., IP address

## Layer 2 : Data Link Layer
Transfers data between devices on the same local network.  
Uses MAC address.  
Ex., WiFi-Frame

## Layer 1 : Physical Layer
Transmits raw bits through physical hardware.  
Actual physical connecntion.  
Ex., Cables, Signals

```
You open a website "www.google.com"
Layer 7 : Browser requests website.
Layer 6 : Data encrypted (HTTPS).
Layer 5 : Session maintained.
Layer 4 : TCP breaks data into packets.
Layer 3 : IP routing devide path.
Layer 2 : MAC addressing used locally.
Layer 1 : Electrical/WiFi signals transmitted.
```

***
