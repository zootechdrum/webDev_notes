## What are good reasons as to why you would use getters and setters in object oriented programming ?

One reason as to why you would use a getter and setter is to prevent anyone from accessing or setting those specific values. For example we can set up constraints as to what property type that variable will hold. We can do some type checking before that variable gets set. We can use a getters to get private variables from a class with risking that the variables will be accessed from outside of the class. 

## Replace a magic number with a symbolic constraint . 
A magic number consist of a number that has a special meaning in the code base but is hard to tell by looking at the number.
For example if an employee in a database is identified by having the id of `99999` . we can set up a global variable that will store that number and call it `EMPLOYEE` . This has a clearer meaning . 