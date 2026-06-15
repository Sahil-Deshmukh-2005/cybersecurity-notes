# Module-3 : How the web works

# Room-1 : DNS in Details

***

## DNS 
Whats is a DNS?  
`DNS` or `Domain Name System` is used to convert the user readable domain name to `IP(Internet Protocol)` address.  
We as human wont be able to remember IP for every single website, that it is linked to.  
So, the `DNS` works as a converter.  

```
https://tryhackme.com ----> 104.26.10.229
```
***

## Domain Hierarchy 
### Top-level Doamin(TLD) :
The Domains are the suffixes in the URL.  
Ex,  
.com , .gov , .edu , .us , .ca , etc..

#### Generic TLD(gTLD) :
The generic domains used by commercials, government, etc.  
Ex,  
.com , .edu , .gov , etc..

#### Country Code TLD(ccTLD) : 
The domains that are specific to a country.  
Ex,  
.us , .ca , .in , etc..


### Second-level Domain(SLD) :
The domain name that is used by the server.  
Ex,  
tryhackme, google, etc..

#### Subdomain : 
The domain before the `SLD` is called `subdomain`.  
Ex,  
admin , etc.. 

```
admin.tryhackme.com
```
admin = Subdomain  
tryhackme = SLD  
.com = gTLD  

❗There are restrictions/rules to be followed for creating an URL : 
1) Every domain i.e. TLD, SLD, Subdomain must be less than 63 characters.
2) Total length of the URL should be less than 253 characters.
3) Every domain only should consist `a-z0-9` and `-` and No 2 `-` should be together.

***

## DNS record types
1) A records = resolves IPv4  
2) AAAA recoeds = resolves IPv6  
3) CNAME records = resolves another domain name  
4) MX records = resolves email  
5) TXT records = resolves text based content

***

## Commands 
### nslookup 
Used to query DNS to map domain names to IP or vice-versa.  
  
```bash
nslookup <URL>
```

```bash
nslookup website.thm
```
This returns the IP of the website.  

```bash
nslookup -type=TXT website.thm
```
This returns the text record from the website.  

```bash
nslookup -type= MX website.thm
```
This returns the mail exchange.  

```bash
nslookup -type= A website.thm
```
This returns IPv4 address.  

```bash
nslookup -type=CNAME shop.website.thm
```
This returns Canonical name = shop.myshopify.com   

