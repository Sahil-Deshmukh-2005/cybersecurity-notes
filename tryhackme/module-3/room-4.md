# Module-3 : How the Web Works

## Room-4 : Putting it all together

***

### Load Balancers
When a websites traffic starts getting quite large or is running an application that needs to have high availability, one web server might no longer do the job.  
Load Balancer provides two main features, ensuring high traffic website can handle the load and providing a failover if a server becomes unresponsive.  
When you request a website with load balancer, the load balancer will receive your request first and then forward it to one of the multiple servers behind it.  
The Load Balancer uses different algorithms to help it decide which server is best to deal with the request.  
Algorithms like:  
1) Round-Robin : Cycle through the servers one after another.
2) Weighted : Server that is least busy.

Load Balancers also perform periodic checks with each server to ensure they are running properly; This is called a `health check`.   
If a server does not respond appropriately or doesnt respond, the Load balancer will stop sending traffic to it untill it reponds appropriately again.  
```
                        🗃️ Server1
                      ↗️  
        💻    ➡️  ⚖️   ➡️  🗃️ Server2
     Computer     LB  ↘️  
                        🗃️ Server3
```

***

### CDN (Content Delivery Network) 
Think of it like a temporary storage.  
It allows you to host static files from your website, such as JS, CSS, Image, Videos, and host them across thousands of servers all over the world.  
When an user wants to access that file, the CDN will search the nearest server instead to search other side of world.  

***

### Database
A proper storage unit for the website to store its user information.  

***

### WAF (Web Application Firewall) 
```
  💻 ------------> 🧱 ------------> 🗃️
Compter         Firewall          Server
```
Its main purpose is to protect the web server from potential attacks.  
Itll only allow certain amount of requests from an IP per second; This is called `rate limiting`.

***

### Whats a web server?
A web server is a software that listens for incomming connections and then utilizes the HTTP Protocol to deliver web content to its client.  

***

### Virtual Hosts
Web server can host multiple websites with different domain names, using `Virtual Hosts`.

***

### Static and Dynamic Content 
1) Static = The web page that never changes. Ex, wiki
2) Dynamic = Web pages changes to the need. Ex, blogs

***

### How a request to website works
```
                    1)Request tryhackme.com in your browser.
                                      ⬇️
                    2)Check local cache for IP addresses.
                                      ⬇️
                    3)Check your Recursive DNS server for address.
                                      ⬇️
                    4)Query root server to find authoritative DNS server.
                                      ⬇️
                    5)Authoritative DNS server advises the IP address for the website.
                                      ⬇️
                    6)Request passes through Web Application Firewall.
                                      ⬇️
                    7)Request passes through the Load Balancer.
                                      ⬇️
                    8)Connect to web server on port 80 or 443.
                                      ⬇️
                    9)Web server receives the GET requests.
                                      ⬇️
                    10)Web Application talks to database.
                                      ⬇️
                    11)Your browser renders the HTML into a viewable website.
```

