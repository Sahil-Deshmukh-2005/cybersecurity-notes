# Module-5 : Operating System Basics

## Room-1 : OS Introduction

***

An `OS` is a core software that co-ordinates everything happening on a computer.  

```
            User
             ⬇️
         Application
             ⬇️
             OS
             ⬇️
          Hardware
```
Without an `OS`, each application would need direct control over the CPU, memory, files, devices and security.  
The `OS` handles this by acting as a Central Organizer.  

***

### System Privilege Layers
#### Kernel Space :- 
The privileged, locked down core of the `OS`.  
This is where the `kernel`, the part of the `OS` that direclty manages hardware and software resources.  
It has unrestricted access to the CPU, memory, storage and all the hardware components.  

#### User Space :-
Where all standard applications runs.  
Applications in `User Space` deliberately prevented from accessing hardware directly.  
Whenever they need to openor save a file, play a sound, or connect to WiFi, they must make a `system call` and request that the `kernel` act on their behalf.

***

### OS Duties/Responsibilities
1) Process Management :-  
Creates, schedules, prioraties and terminates running processes. Decides CPU time for each process.
  
2) Memory Management :-  
Allocates RAM to processes.  
It prevents one process from interupting/crashing other processes.
  
3) File System Management :-
Organize files into directories, handles naming, paths, permissions.
  
4) User Management :-
Handles multiple user accounts, authentication and permissions to determine who can access what.
  
5) Device Management :-
Loads drivers and provides a universal interface (hardware abstraction layer).
Ex, plug in new mouse, printer, pendrive.

***

### At base level your OS handles
- Authentication = Verifies who you are through login passwords and biometrics.
- Permissions = Controls exactly what each user and app is allowed to read, write and execute.
- Isolation = Keeps every process in its own protected box, (kernel / user space seperation).
- System Protection = Safeguards critical system files and settings from unauthorized changes.

***

### OS Interfaces
1) GUI = Graphical User Interface, Interaction through clicking and tapping.  
2) CLI = Command Line Interface, Text based interface, communication through commands.

***
