# Burp Suite

Burp suite is a web security testing tool.  

#### Visualise it like this:  

```bash
Browser ➡️ Burp Suite ➡️ Internet
```
Instead of directly connecting to the website/internet, `burpsuite` acts as a middle man when activated, it lets you:  
```
👉 see requests
👉 modify them  
👉 replay them  
👉 test web application
```
Thats why its called `Intercepting proxy`.  

***

Burp shows HTTP commands:
```
⭐ GET
⭐ POST
⭐ PUT
⭐ DELETE
```

*** 

## Intercept 
When the Intercept is ON ✔️ and you try to open a website, it freezes, and you get to see the `GET` command in the `burp`.  
When the Intercept is OFF ✖️, the `burp` will still log the traffic, but it wont freeze the website.

***

## Result / Requests
```
GET / HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
Accept: text/html
```
Here,  
GET = HTTP Method, meaning to fetch the data  
/ = homepage

***

## Headers
Metadata about the requests.  
Ex,  
```
Browser info,
cookies,
accepted content,
language.
```
***

## Status Code
Status code are numerical values that states the condition of request.
```
100 - 199 ➡️ Informational
200 - 299 ➡️ Successful
300 - 399 ➡️ Redirection
400 - 499 ➡️ Client error
500 - 599 ➡️ Server error
```
***

## Repeater
A repeaters job is to send the same HTTP request again and again manually.  
While modifying parts of it to observe how the server responds.  
So we dont have to use the browser UI again and again.  
Ex,  
GET /profile?id=5 HTTP/1.1
Host: example.com  
  
change id=5 ----> id=6  
and observe the response.  
### What things you can test:
1) parameters  
   ?id=5  
2) Headers  
   User-Agent  
   Cookie  
   Authorisation  
3) Request Method  
   GET ----> POST  
4) Body Data  
   JSON/forms/etc..  

***

## Request and Response Structure
We did this in tryhackme Module-3, room-2 : HTTP in Details  

***

