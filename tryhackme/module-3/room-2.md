# Module-3 : How the Web Works

## Room-2 : HTTP in Details

***
.
### HTTP = HyperText Transfer Protocol
Its is used whenever you view a website.  
Developed by Tim Berner-Lee and his team between years 1989-1991.  
It is set of rules used for communicating with web servers for the transmitting of the webpage data, whether it is HTML, Image, Video, etc..  

***

### HTTPS = HTTP Secure
It is the secure version of `HTTP`.  
Data is encrypted while transmitting.  

***

### URL = Uniform Resource Locator
An URL is predominantly an instruction on how to access a resource on the internet.  
```
http://user:password@tryhackme.com:80/viewroom?id=1#tasks
```
1) Scheme = http
This instucts on what protocol to use.
Ex, http, https, ftp

2) User = user:password
Some services require login authentication, which it then showed on the URL.

3) Host = tryhackme.com
The domain name or IP address you wish to access.

4) Port = 80
The port you are going to connect to.

5) Path = viewroom
The file name/ location you wanna access.

6) Query String = id=1
Extra bits of information that can be sent to the requested path.

7) Fragment = #tasks
This is a reference to location on that actual page requested.

***

### Making a request
Short request = GET / HTTP/1.1  
  
But for much rich experience, youll need to send other data as well. This other data is sent in what is called `Header`.  

***

### HTTP Method
They are the way for the client to show their intended action when making HTTP request.
```
GET = Retrive Data
POST = Submit Data
PUT = Update Existing Data
DELETE = Delete the Data
```

***

### HTTP Status Code
```
200 = OK
201 = Created
301 = Moved Permanently
302 = Found
400 = Bad Request
401 = Not Authorized
403 = Forbidden
404 = Page Not Found
405 = Method not Allowed
500 = Internal Service Error
503 = Service Unavailable
```

***

### Headers
#### Request Headers
```
- Host = Website name
- User-Agent = Browser name
- Content-Length = Request length
- Accept-Encoding = Type of compression method
- Cookie = Data sent to server to help it remember your information
```

#### Response Headers
```
- Set-Cookie = Information to store which gets sent back to the server on each request
- Cache-Control = How long to store the content of the response in the browser's cache before it requests it again
- Content-Type = Type of data being returned. Ex, HTML, CSS, JS, Image, etc..
- Content-Encoding = Type of compression method
```

***

### Cookies
It is used so that the server remembers the user in next request.  
As HTTP is `Stateless` (Does not remember the previous state), it forgets who you are so is `Cookie : name = adam`, this cookie will be sent every time a request is sent so that the server knows who you are.  

