# Module-9 : Defensive Security

## Room-1 : SOC Fundamentals

***

### SOC ( Security Operations Center ) :
A SOC is a dedicated facility operated by a specialized security team. This team aims to continuously monitor an organization's network and resources and identify suspicious activity to prevent damage.  

Main Focus:  
1. Detection
2. Respond

#### Detection 
- Detect Vulnerabilities : A vulnerability is a weakness that an attacker can exploit to carry out things beyond their permissions level.
- Detect unauthorized activity : Suppose an attacker discovered the username and password of one of the employees and then used them to log into company system.
- Detect policy violations : A security policy is a set of rules and procedures created to help protect a company against security threats and ensure compliance.
- Detect intrusions : Intrusion refers to unauthorized access to systems and networks.

#### Response 
- Support with the incident response : Once an intrusion is detected, certain steps are taken to respond to it. This response includes minimizing its impact and performing the root cause analysis of the incident. The SOC team also helps incident response team carry out these steps.

***

### Three pillars of SOC 
1. People :
Regardless of the evolution of automating the majority of security tasks, the People in a SOC will always be important. People here means SOC team. 
2. Process :
Process is a way of answering alert triage ( 5 W's ).
    - What? : What caused the alert to generate?
    - When? : When was the alert generated?
    - Where? : Where was the alert detected?
    - Who? : Who caused the malware, so that alert was generated?
    - Why? : Why did malware was installed?
  
    After all this the analyst have to generate a Report of the event.  
3. Technology : 
The Technology portion in the SOC pillars refers to the security solutions. These security solutions efficiently minimize the SOC team's manual effort to detect and respond to threats.  
    - `SIEM` ( Security Information and Event Management ) is a popular tool used in almost every SOC environment.
    ```
    ❗Note : the SIEM solution only provides the detection capabilities in a SOC environment.
    ```
    - `EDR` ( Endpoint Detection and Response ) provides the SOC team with detailed real-time and historical visibility of the devices' activities. It has extensive detection capabilities for endpoints, allowing you to investigate them in details and respond with few clicks.
    - `Firewall` functions purely for network security and acts as a barrier between your internal and external networks. It monitors incoming and outgoing traffic and filters any unauthorized traffic. The firewall also has some detection rules deployed, which helps us identify and block suspicious traffic before it reaches the internal network.

***
