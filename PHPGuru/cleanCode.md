## What are good reasons as to why you would use getters and setters in object oriented programming ?

One reason as to why you would use a getter and setter is to prevent anyone from accessing or setting those specific values. For example we can set up constraints as to what property type that variable will hold. We can do some type checking before that variable gets set. We can use a getters to get private variables from a class with risking that the variables will be accessed from outside of the class.

## Replace a magic number with a symbolic constraint .

A magic number consist of a number that has a special meaning in the code base but is hard to tell by looking at the number.
For example if an employee in a database is identified by having the id of `99999` . we can set up a global variable that will store that number and call it `EMPLOYEE` . This has a clearer meaning .

## What is a state behavioral design pattern ?

The programs we write can be in any number of fluctuating states. For example, we can be calling and an api and then listen for any user input . There are 2 different states our program can be in. Most programmers have written "state machines" at least once. A state machine is where we write a switch statement and try to implement some sort of logic flow based on the state that the program is in.

```PHP
class Document is
    field state: string
    // ...
    method publish() is
        switch (state)
            "draft":
                state = "moderation"
                break
            "moderation"
                if (currrentUser.role === 'admin')
                    state = "published"
                break
            "published":
                // Do nothing.
                break
```

The above switch method can be hard to maintain because as soon as we start to introduce additional states and states that depend on other states the code can start to become a mess.

How can we fix this ?
We fix it by using the state pattern .

### What is an example of using he state pattern ?

Take a document as an example. A document can be in 3 states.

1. Draft state
2. Moderation State
3. Publish

Each of the 3 options above can be represented by objects. This is better than using a switch statement because with objects you can modify the class individually without affecting the rest of the other objects.

An example

```php
    class Document is
        field state: State:

        constructor status is
            this.state = new DraftState(this);

        UI = new UserInterface();
        UI.newPage.onClick(this.draft);
        UI.edit.onClick(this.Moderation);
        UI.publish.onClick(this.publish);

        method.changeState(state: State) is
            this.state = state;

        //Ui Methods that depending on state delegate the methods
        // of that state.

        method clickDraft() is
            state.draft();

    abstract class state is
        protected field document: Document

        constructor State(document) is
            this.document  = Document

        //Methods all classes that will represent state need to apply
        abstract method draft()
        abstract method moderation()
        abstract method publish()

    class moderation extends state is
        method moderation() is
            document.changeState(new Moderation(draft));
        method publish() is
            document.changeState(new Publish);

```

## When should I throw an error vs when should I use a conditional .
