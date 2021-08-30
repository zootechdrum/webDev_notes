## What are the differences between Apache and Nginx ?

The main difference between Apache and Nginx is the Apache uses a process driven approach. This means that for each new request a new thread is created . Nginx uses an even driven architecture to handle multiple requests within one thread. (Nginx is faster in that respect.)

### What is a thread ?

A thread is a the smallest sequence of programmed instructions that can be managed independently by a scheduler. In most cases, a thread is a component of a process. 

## Which server is better ?

Nginx is faster because it does not create new threads every time a request is made. The way Apache handles the request is it created a new thread on each request which can be resource intensive especially if we a a million users trying to access the site. 

## What are the common issues when moving from Nginx to Apache ?

Nginx was created as a proxy sever and as a web server. Nginx does not provide a mechanism for specifying config. For file system directory , instead passes their URI itself. This is why when trying to implement some sort of MVC architecture like Laravel or custom . The server looks for a file path instead of a deconstructing the URI and treating them as parameters. Additional configuration needs to made on server in order to treat these requests a particular way. 

## What is a proxy server ?

A proxy sever is a server that acts as a middleman between the client and the final destination the request is being made to. Th reason why you would have a proxy server is to 
1. restrict access to certain sites. 
2. Provide some sort of protection before the request is sent to the actual server.
3. The proxy server can change details of the request before the payload gets reaches the address. 




