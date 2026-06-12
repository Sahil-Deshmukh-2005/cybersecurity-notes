# Web Fundamentals

Last time we saw what `HTTP Request` and `HTTP Response` looks like,  
Now we gonna see whats inside of those Requests and Responses.  

***

## Headers 
`Header` contains metadata about the Requests/Response.  

### Commond Request Headers
1) User Agents  
Tells server which browser is making the request.

2) Cookie  
It stores session ID, login Information, preferences.

3) Authorization  
Contains API tokens, authentication credentials

4) Content Type  
Tells what kind of data is being sent.

***

## Cookies 
Small data store in browser.  
Used for staying logged in, remembering preferences, tracking sessions.  

***

## Sessions
Server-Side login tracking   
```
Login ----> Server creates session ----> browser stores cookies
```
The Browser sends cookies with future requests.  

***

## URLs 
```
https://example.com/login?id=5
```

Here,  
`https` := protocol  
`example.com` := domain  
`login` := path  
`id=5` := parameter

***

## DNS 
We have seen DNS in depth in `tryhackme/module-3/room-1.md`. 

***

## Caching 
Caching means temporarily storeing data to avoid frequent server requests.

Sometimes,  
- websites shows old content
- login/logout behaves weirdly
- responses appear inconsistent

because browser is using cached data.  

### Common Caching Types
#### Browser Cache
Stored locally by browser.  

#### DNS Cache
Stores recent domain -> IP mapping.  

***
