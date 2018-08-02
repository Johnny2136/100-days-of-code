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

**Thoughts** I knew this was going to be tricky, I remembered over thinking a couple of the challenges yesterday but even though I tried to keep it simple, but once again I made at least one spaghetti code monster :monster: I had a hard time with one of the challenges, I usually rely on JS Libraries Writing your own JS can be challenging. :smile:

```javascript
//Copy Array Items Using slice()
function forecast(arr) {
// change code below this line
  return arr.slice(2, 4); //My solution
}
// do not change code below this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```
Another way of doing it (This was the first way I tried it)

I had to add debugging statements to find where i was missing the unit test.

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


### Day 5: July 29, Sunday

 **Today 's Progress**: My goal today is to finnish the remaining challanges in [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures).

**Thoughts**: Remembered NO OVER THINKING!!! I have a bad habit of over complicating simple instructions, well it says do "a" I think well should i get to "a" via `ax^2+ab+c=0` :smile:

Today didn’t disappoint I forgot to capitalize the "O" in "Object" and spent almost an hour trying to figure why the unit tests weren’t passing ARGGGGG!!!

```javascript
//Generate an Array of All Object Keys with Object.keys()
//Finish writing the getArrayOfUsers function so that it returns an array containing all the properties in the object it receives as an argument.
let users2 = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};
function getArrayOfUsers(obj) {
  // change code below this line
  return Object.keys(obj);//OH GOD!!! an hour just because I forgot to capitalize O
  // change code above this line
}
console.log(getArrayOfUsers(users2));
```

**Link(s) to work**
1. [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)

* PassedAdd Key-Value Pairs to JavaScript Objects
* PassedModify an Object Nested Within an Object
* PassedAccess Property Names with Bracket Notation
* PassedUse the delete Keyword to Remove Object Properties
* PassedCheck if an Object has a Property
* Passed Iterate Through the Keys of an Object with a for...in Statement
* PassedGenerate an Array of All Object Keys with Object.keys()
* PassedModify an Array Stored in an Object

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCBasicDataStructurs2) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicDataStructure.js)

### Day 6: July 30, Monday

 **Today 's Progress**: I started challanges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1 hour.

**Thoughts**: Today was a tough day I had a 15.5-hour day at work (counting the commute) and was knee deep in Docker CLI. I feel so tired but I managed to get some coding before bed. Tomorrow it’s Kubernetes and another long day. 

```javascript
//The algorithm to convert from Celsius to Fahrenheit is the temperature in Celsius times 9/5, plus 32.
function convertToF(celsius) {
  let fahrenheit = celsius * 9/5 + 32 ;// my solution
  return fahrenheit;
}
convertToF(30);
```

**Link(s) to work**
1.  Started [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

Introduction to Basic Algorithm Scripting

* PassedConvert Celsius to Fahrenheit
* PassedReverse a String
* PassedFactorialize a Number

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 7: July 31, Tuesday

**Today 's Progress**: I continued the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is a tough week I had another long day at work (counting the hellish commute) and was knee deep in Docker CLI and RedHat's OpenShift. I feel like I could sleep for a week. Tomorrow it’s another long commute day. These challenges seem hard, to me coming up with code from scratch is difficult I should try what I did in college and make a UML model of the user story before starting to write the code.

```javascript
//Find the Longest Word in a String
//Return the length of the longest word in the provided sentence.
function findLongestWordLength(str) {
    var obj = str.split(' ');// Split the words up
    var letterCount = 0; //variable for number of letters
    for (var i = 0; i < obj.length; i++) { //loop through the split string
        if (letterCount < obj[i].length) { // this looks ugly I'm sure there is a better way
            letterCount = obj[i].length;
        }
    }
    console.log(letterCount);
    return letterCount;    
} 
findLongestWordLength("The quick brown fox jumped over the lazy dog");
```

**Link(s) to work**
1.  Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

Introduction to Basic Algorithm Scripting

* PassedFind the Longest Word in a String
* PassedReturn Largest Numbers in Arrays

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)


### Day 8: August, Wednesday

**Today 's Progress**: I continued working the challanges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is not getting any easier I had another long day at work (counting the hellish commute 2.5 hours to go 65 miles) we did more docker files in OpenShift and Dockerfiles CLI also RedHat's OpenShift GUI console. Tomorrow I have a dentist appointment and homework for the OpenShift class I'm in this week. The Challenges continue to be difficult but I'm hanging in there with this 100-day coding challenge.

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  var sln = target.length;
  console.log(sln);//Debugging statment
  if(str.substr(-sln) === target){
    console.log(str.substr(-sln) + " = " + target);//Debugging statment
    return true;
  } else {
    return false;
  }
}
confirmEnding("Bastian", "n");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedConfirm the Ending
* PassedRepeat a String Repeat a String
* PassedTruncate a String

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

