# Module-3 : How the Web Works

## Room-3 : How websites Work

***
### How we see any website on our browser 
```
    -------Request from Browser----->      -------Request from Browser----->
  💻                                    🌐                                     🗃️
Browser                              Internet                                Server
    <-------Response from Server-----      <-------Response from Server------
```

This is the best diagram I could draw 🤪 to explain you how a website works.  

***

### Two Major Components
1) Frontend (Client Side) :  
   The way your browser renders the website on your machine.
2) Backend (Server Side) :  
   A server that processes your request and returns a response.

***

### Sensitive Data Exposure
When the website doesnt properly protect (or remove) sensitive clear text information to the end-user;  
Usually found in a sites frontend source code, is a `Sensitive Data Exposure`.

***

### HTML Injection
It is a vulnerability that occurs when an unfiltered user input is displayed on the page.  
If the website fails to sanitize the user input (filter any 'malicious' text that a user inputs into a website), and that input is used on the page.  
An Attacker can inject HTML code into a vulnerability website.  
  
You dont get it ? Dont worry let me explain with an example  
Consider a website which accepts user input and a button to submit it.  
If the website does not filter the user input then we can add anything to the input box.  
Let say we put:
```
<a href="http://malicioussite.com">Malicious</a>
```
Then when we submit the button the input will activate, linking the website to 'malicious' website `http://malicioussite.com`, opening the malicious site on that website.


