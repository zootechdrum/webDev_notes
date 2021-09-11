## What is typescript ?

Typescript is a superset of javascript. It adds new bells a whistles to the javascript lanugage.

## Why is typescript nice to have ?

Typescript is nice to have because it can catch errors before you run your script and it allows you to define types.

For example,

```javascript
function sum(a, b) {
	return a + b;
}
console.log('a', '4');
```

The above example is an excelleent example of an error typescipt would prevent. Although the above won't give you a runtime error the logic is probably not what is expected in the sum function. With typscript we can define types in the sum function. By doing so errors would be thrown before we even get to the point where we catch it in the browser or the command line.
