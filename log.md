# 100 Days Of Code - Log

### Day 1: July 25, Wednesday

**Today's Progress**: I've gone through 3 exercises on FreeCodeCamp and did one project.

**Thoughts** II've had many coding classes in college and want to step up my game, I found out that coding is not like riding a bike you don’t just learn it and then know it from now on, I don’t code at work so my skills rusted up quite a bit. I want to revamp them and try and stay current with modern technology I started following students of [CodeClan](https://codeclan.com/) in Scotland and found Free Code Camp so I’m working through the course ware and once done hope to contribute to the project, and it's an awesome feeling when I finally solve an exercise challenge after a lot of failing unit tests that green banner appears and it’s like “YEEEESSSS!!!!!!”.

**Link(s) to work**
1. [Palindrome Checker](https://github.com/Johnny2136/FCC-Projects/blob/master/PalindromeChecker.js)
2. [Introduction to the Debugging Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging)
  * PassedUse the JavaScript Console to Check the Value of a Variable
  * PassedUnderstanding the Differences between the freeCodeCamp and Browser Console
  * PassedUse typeof to Check the Type of a Variable (https://www.freecodecamp.com)
  
  ### Day 2: July 26, Thursday

**Today's Progress**: I've gone through the remaining exercises on FreeCodeCamp Debugging Project.

**Thoughts** I've had a lot of experiance debugging so was able to get though all the excersizes a couple we pretty tricky.

```javascript
//Debugging: Use Caution When Reinitializing Variables Inside a Loop
// original buggy code...

function zeroArray(m, n) {
  // Creates a 2-D array with m rows and n columns of zeroes
  let newArray = [];
  let row = [];
  for (let i = 0; i < m; i++) {
    // Adds the m-th row into newArray
    /**** //the offending code Loop****
    for (let j = 0; j < n; j++) {
      // Pushes n zeroes into the current row to create the columns
      row.push(0);
    }
    */
    // Pushes the current row, which now has n zeroes in it, to the array
    newArray.push(row);
  }
  for (let j = 0; j < n; j++) { //my solution move outside first loop
      // Pushes n zeroes into the current row to create the columns
      row.push(0);
    }
  return newArray;
}
let matrix = zeroArray(3, 2);
console.log(matrix);
```

**Link(s) to work**
1. [Introduction to the Debugging Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging)
*  PassedCatch Misspelled Variable and Function Names
*  PassedCatch Unclosed Parentheses, Brackets, Braces and Quotes
*  PassedCatch Mixed Usage of Single and Double Quotes
*  PassedCatch Use of Assignment Operator Instead of Equality Operator
*  PassedCatch Missing Open and Closing Parenthesis After a Function Call
*  PassedCatch Arguments Passed in the Wrong Order When Calling a Function
*  PassedCatch Off By One Errors When Using Indexing
*  PassedUse Caution When Reinitializing Variables Inside a Loop
*  PassedPrevent Infinite Loops with a Valid Terminal Condition
[Code Here](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntroductionToTheDebuggingChallenges.js)
and all in repl.it https://repl.it/@JohnJohnson2/DebuggingFCC

### Day 3: July 27, Friday

**Today's Progress**: I've gone through the first few exercises on FreeCodeCamp Basic Data Structures.

**Thoughts** I thought this was going to be easy, but yeah I over thought a couple of the challenges and spent a few hours trying to fix the spaghetti code monster I created pretty tricky there FCC. :smile:

```javascript
//Remove Items from an Array with pop() and shift()
function popShift(arr) {
  let popped = arr.pop(); // change this line (This was tricky I was over thinking it)
  let shifted = arr.shift(); // change this line
  return [shifted, popped];
}
// do not change code below this line
console.log(popShift(['challenge', 'is', 'not', 'complete']));
```

**Link(s) to work**
1. [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)

* PassedUse an Array to Store a Collection of Data
* PassedAccess an Array's Contents Using Bracket Notation
* PassedAdd Items to an Array with push() and unshift()
* PassedRemove Items from an Array with pop() and shift()
* PassedRemove Items Using splice()
HAll in GitHub and rep.it here: [Rep.it](https://repl.it/@JohnJohnson2/FCCBasicDataStructurs2) [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicDataStructure.js)

### Day 4: July 28, Saturday

**Today's Progress**: I've gone through the next few exercises on FreeCodeCamp Basic Data Structures.

**Thoughts** I knew this was going to be tricky, I remembered over thinking a couple of the challenges yesterday but even though I tried to keep it simple, but once again i made at least one spaghetti code monster :monster: I had a hard time with one of the challenges, I usually rely on JS Libraries Writing your own JS can be challenging. :smile:

```javascript
//Copy Array Items Using slice()
function forecast(arr) {
// change code below this line
  return arr.slice(2, 4); //My solution
}
// do not change code below this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```
#### or another way of doing it (was the first way i tried it)
```javascript
function forecastAlt(arr) {
// change code below this line
let myArr = arr.slice(2, 4) ;
console.log("This is the content of myArr = " + myArr); //for debugging
console.log("This is the content of arr = " + arr); //for debugging
return arr = myArr; //my solution 
//(after hours fighting code, once I put the debug statements in it was pretty clear)
}
// do not change code below this line
console.log(forecastAlt(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

**Link(s) to work**
1. [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)

* PassedAdd Items Using splice()
* PassedCopy Array Items Using slice()
* PassedCopy an Array with the Spread Operator
* PassedCombine Arrays with the Spread Operator
* PassedCheck For The Presence of an Element With indexOf()
* PassedIterate Through All an Array's Items Using For Loops
* PassedCreate complex multi-dimensional arrays

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCBasicDataStructurs2) [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicDataStructure.js)
