# Module-4 : Computer Fundamentals

## Room-1 : Inside a Computer System

***

Basic Components inside a Computer System:  
1) Motherboard : The skeleton and Nerves  
2) RAM : Short-term Memory  
3) PSU : Heart and Lungs  
4) CPU : The Brain  
5) GPU : Visual Cortex  
6) HDD + SSD : Long-term Memory

***

#### Motherboard 
It connects and allows communication between all the components.  

#### CPU (Control Processing Unit)
Executes instructions and perform calculation.  

#### RAM (Random Access Memory)
Stores data temporarily while the computer is running. Its a Volatile Memory, means once the computer shuts down it removes everything that was stored in it.  

#### SSD 
Stores data permanently even when powered off.  

#### Network Adapter
Used to communicate with computers and other networks.  

#### PSU (Power Supply Unit)
To supply electricity power to all the components.  

#### Graphic card(GPU) 
Processing and Outputting visual information to display.  

#### Input-Output Devices
To send data and receive data from the computer.  

***

### What happens when you press the start button
```
______________________      ___________________      ________      _______________________      ____________________
| Press Power Button | ---> | Firmware Starts | ---> | POST | ---> | Select Boot Devices | ---> | Start Bootloader |
|____________________|      |_________________|      |______|      |_____________________|      |__________________|
```
1) Press the Power Button :  
   When you press the power button the PSU gets the signal to start sending power to the components.  
  
2) Firmware Starts :  
   A Computer System contains firmware that allows all its components to start up. The Control System that manages this is called Unified Extensible Firmware Interface (UEFI).  
   BIOS does the same as UEFI.  
   But has mainly been replaced by UEFI.  
  
3) Power-ON Self Test :  
   UEFI runs POST to check that required hardware is present, configured and functioning.  
   Errors trigger beeps or alerts.  
  
4) Select Boot Devices :  
   UEFI follows a priority list to determine which device to boot from.  
   Typically on SSD or HDD wiht the Operating System installed.  
  
5) Start a Bootloader :  
   The Bootloader loads the Operating System into RAM.  
   Then UEFI hands Control to the Operating System, completing the boot sequence.  

***


