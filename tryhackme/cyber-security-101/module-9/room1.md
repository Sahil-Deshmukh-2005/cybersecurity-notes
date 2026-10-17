# Module-9 : Offensive Security Tooling

## Room-1 : Hydra

***

### Whats Hydra? 
Its a brute force online password cracking program, a quick system login password "hacking" tool.

***

### Commands 
1. For FTP :  
`hydra -l <username> -P <full path to passlist.txt> ftp://<machine-ip>`  
  
2. For SSH :  
`hydra -l <username> -P <full path to pass> MACHINE_IP -t 4 ssh`  
-l : specifies the (SSH) username for login  
-P : Lists of passwords  
-t : sets number of threads to spawn  
  
3. For web :  
`sudo hydra <username> -P <wordlist> MACHINE_IP http-post-form "<path>:<login_credentials>:<invalid_response>"`  
http-post-form : The type of the form is POST  
`<path>` : The login page URL, Ex, login.php  
<login_credentials> : The username and password used to log in, Ex, username=^USER^&password=^PASS^  
<invalid_response> : Part of the response when the login fails  
  
Ex,  
`hydra -l <username> -P <wordlist> MACHINE_IP http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -V`  
/ = the main ip addr  
the specified username will replace ^USER^  
the password from the wordlist will replace ^PASS^  
F=incorrect is a string that appears in server reply when the login fails.  
  
`-s <port>` can be used to specify the port number if the website is not using default port.  

***
