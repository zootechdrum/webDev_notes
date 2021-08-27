# What is time complexity ?
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

        for(let i = 0; i< n.length; i++) {
            counter++;
            if(max === unefined || max < [i]) {
                max = n[i];
            }
        }

        return max;
    }
```
In the function above the `findMax` function will take an input and it will visit each input once. This happens in the for loop. Another example would be  asking every student in a classroom if they have a pen. 

## What is a quadratic algorithm ?

A quadratic algorithm has the input size of 2 the algorithm will do 4 operations. As you could imagine this is less efficient than our previous examples.  As our dataset grows in length the longer it will take for our function to complete . 

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
Linearithmic time complexity it's slightly lower than a linear algorithm. Howerver, it's still better the having an algorithm with a time complexity of 0(n^2);

In a Linearithmic algorithm we split our input into 2. We keep splitting the input until we come out with the result that we are looking for. 


