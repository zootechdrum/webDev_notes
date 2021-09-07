## What is good code ?

Good code can be defined by most people as easily readable and easy to scale. Readability can be done by writing descriptive functions and variables that gives context as to what the use of that variable or function does. Code that is easy to scale can is determined by the space and time complexity the piece of code executes in. For example, will a certain function scale well if we dramatically increase the input ten fold. If the function has a time complexity of O(n^2) , the scalability of that function will be poor. This is a good time to think if their are faster, more efficiant ways to write that function.1

As a software engineer, you should focus on the following three pillars in order to achieve 'good code' .

1.  Readability
2.  Space complexity
3.  Time complexity

## What is space complexity ?

Time complexity is different than time complexity in the sense that space complexity is concerned with the following

1. variables
2. data structures
3. function calls
4. Allocation

### Examples of space complexity ?

```javascript
function scaryCall(num) {
	for (let i = 0; i < n; i++) {
		console.log('hello');
	}
}
```

The time comoplexity of the for loop above is O(1). The reason being is that the only thing that gets created that is saved in memory is the the variable i.

### Exampole of space complexity #2

```javascript
function scaryCall(num) {
	let arr = [];
	for (let i = 0; i < n; i++) {
		arr[i] = i;
	}
	return arr;
}
```

The space time complexity of the the function above is O(n). The reason it is O(n) is due to the array holding `n` number of items. Those items have to placed in that users computer. Therfore it has to take up some amount of space.

## What is time complexity ?

We use time complexity as a way to measure how an algorithm performs regardless of what kind of machine will execute the algorithm. You can get the time complexity by "counting" the number of operations performed by your code. This time complexity is defined as a function of the input size `n` using Big-O notation. `n` indicates the input size, while O is the worst case scenario growth rate function .

### An example of 0(1) time complexity.

Here is an example of an algorithm that takes up 0(1) time .

```Javascript
    function isEvenOrOdd(n) {
        return n % 2 ? 'Odd' : 'Even';
    }

    console.log(isEvenOrOdd(10));
```

It does not matter if n is `10` or `10,001`. It will execute line 2 one time .

The same is true for the following example.

```Javascript
const dict = {the: 2204092, be:123456;

function getWordFrequency(dict,word) {
    return dic[word];
}

console.log(getWordFrequency(dic,'the'));
```

Again, regardless of how dict grows to the `getWordFrequency` function still performs only one operation.

### An example of 0(n) time complexity.

0(1) time complexity happens when the size of the input does matter. As long as the input keeps growing the time it will take for that function to complete will become much longer.

Take the following as an example

```javascript
function findMax(n) {
	let max;
	let counter = 0;

	for (let i = 0; i < n.length; i++) {
		counter++;
		if (max === unefined || max < [i]) {
			max = n[i];
		}
	}

	return max;
}
```

In the function above the `findMax` function will take an input and it will visit each input once. This happens in the for loop. Another example would be asking every student in a classroom if they have a pen.

## What is a quadratic algorithm ?

A quadratic algorithm has the input size of 2 the algorithm will do 4 operations. As you could imagine this is less efficient than our previous examples. As our dataset grows in length the longer it will take for our function to complete .

```javascript
function hasDuplicates(n) {

    const duplicates = [];
    let counter = 0;

    for(let outter = 0; outter < n.length; outter++) {
        for(let outter = 0; outter < n.length; outter++) {
            counter++;

            if(outter ==== inner) continue;

            if(n[outter] === n[inner]) {
                return true;
            }
        }
    }
    return false;
}
```

## What is a Linearithmic algorithm ?

Linearithmic time complexity it's slightly slower than a linear algorithm. However, it's still better the having an algorithm with a time complexity of 0(n^2);

In a Linearithmic algorithm we split our input into 2. We keep splitting the input until we come out with the result that we are looking for.

## What is the most expensive time complexity.

The most expensive time complexity is O(n!) . It is the most expensive in time complexity because

## What is the difference between O(n^2) vs. O(a\*b);

The difference between these two notations is the size of the input in the function. For example, if a function accepts 2 different inputs bu those 2 inputs are always going to be the same in length then the time complexity of that function is going to be O(n^2); . When a function recieves 2 different inputs but the size of the inputs are different then the time complexity is O(a\*b).

## What is a data structure ?

data structure is a way to organize data. Some of the most popular data structures include arrays, hash tables, and linked lists. A good example of a data structure can be seen when we think of running programs on our computers. When we open up Google Chrome that program is on our hard disk. When we visit a link that we may have visited before we can call on our RAM to load uop that link we have visited before to execute that script faster.

## What if the language that I know does not support a data structure that is present in the Java programming language ?

Just because linked lists may come with Java out of the box does not mean we cannot build our own linked list in javascript. You can always build this into the programming language that you are working with .

## What is a hashing function ?

A hashing function takes an input like the string of `grapes` and gives it an addess inside the hashing function. This address makes accessing that property a lot faster because it gives us direct access to that property in memory.
