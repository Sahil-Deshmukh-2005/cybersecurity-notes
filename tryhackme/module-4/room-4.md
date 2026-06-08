# Module-4 : Computer Fundamentals

## Room-4 : Virtualization Basics

***

Why Virtualization is important?  
Before Virtualization   
`One Server = One Application`  
Means,  
```
having a website = one server
storing data = another server
.....
```

This lead to high cost, low utilization, slow deployment, hard to scale.  
Virtualization solved these issues.  

***

### Virtualization introduced a new idea,  
What if multiple application sould share same `Physical Server` safely.  

***

### Hypervisor 
A virtualization layer, called `Hypervisor`, was introduced to act as a refree between `Lab Machines (VM)` and allow each virtual computer to behave independently, like a physical computer.  
It is the software that creates and manages `Lab Machines (VM)`.  

#### Hypervisors have two main types of implementation
1) Type-1 :  
   Type-1 Hypervisors run directly on the physical hardware, making them fast, efficient, and ideal for servers and professional environments.  
2) Type-2 :  
   Type-2 Hypervisors run within an existing `OS`, making them easier to install and ideal for learning, testing or small setups.  
  
#### Kali linux uses Type-2 Hypervisor.

***

### Lab Machines (VM) 
It is a virtual computer created by the hypervisor. Even though its virtual, it behaves as a real machine.  

***

### Containers 
It is a light weighted, isolated environment that runs a single application and all necessary components to support it.  
Instead os bringing the whole seperate `OS`, a container borrows the core of the existing system by running on the kernel, which is a part of an `OS`, that communicates with the hardware and manage resources such as memory and running processes.  
  
Easiest way to deploy `Containers` in a `VM` is using `Docker`.  

```
               |_____________________________________________|
               |             Physical Server                 |
               |             ______________                  |
               |             | Hypervisor |                  |
               |             ______________                  |
               |  |_______________________________________|  |
               |  |           Virtual Machine             |  |
               |  |   ________________ ________________   |  |
               |  |   |  Container A  |   Container B  |  |  |
               |  |   ________________ ________________   |  |
               |  |_______________________________________|  |
               |_____________________________________________|

```

***

### Benefits of Virtualization
1) Cost Savings
2) Better Resource Usage
3) Safe Testing for CyberSecurity
4) Faster Deployment
5) Flexibility
6) Portability
7) Scalability
8) Centralized Management

***
