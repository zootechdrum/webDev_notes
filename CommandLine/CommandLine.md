## Permissions and what they mean. 

In a file system users can have certain access rites that can help protect certain files or directories. 

By typing the command 
`ls -l` in the terminal you can see the available rights users and groups have. it will typically looke like
```
-rw-rw-r--
```
the order is owner group world
             rw-   rw-    r--

In the example above the owner would have read and write permission but not executable permission. The group would have the same read and write permission . and the rest of the world wold only have read permission . 

