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

## What does the `td` command do in the terminal .

The `tr` command accepts standard input and makes some sort of modification as then gives us some standard output. For example 
```
cat [file] | tr a-z A-Z
```
This will replace any lowercase letters and transfer them to uppercase letters. 
* This will not overwrite the file that is being saved as standard input. 

How do you overwrite something in a file by using the terminal. 

```
echo "Another Minute! Date is: $(date): > ~/time.log
```
to append to a file instead of re-writing the file you can use
```
echo "Another Minute! Date is: $(date) >> !/time.log
```