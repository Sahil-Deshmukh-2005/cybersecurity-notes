# Module-1 : Start Your Cybersecurity Journey

## Room-1 : Offensive Security Intro

Offensive Security is about thinking like an attacker to find weakness before real hackers do.

### Commands :
```bash
dirb <URL>
```
Some websites leave hidden directories or endpoints accessible, `dirb` is used to discover those hidden directories or endpoints.  
  
Ex,  
We can see a website `http://fakebank.com/dashboard` but there may be hidden directory or endpoint like `http://fakebank.com/account` that is not visible on the main website, it can be discovered using `dirb` command.  
```bash
dirb http://fakebank.com
```
❗Use only on authorized targets such as labs, tryhackme rooms, or your own system.
