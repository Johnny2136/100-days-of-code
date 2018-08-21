# 100 Days Of Code - Log

### Day 28: August 21, Tuesday

**Today 's Progress**: I continue work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: Today focused on the Telephone Number Validator challenge This is all about RegEx to pass This project. The telephoneNumberValidator.js is located here:[FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_JS_Projects/telephoneNumberValidator.js).

After examining the requirements I made the following user story, As a user I want to: pass a number to a function that returns true if the passed string looks like a valid US phone number.

For example: For this challenge you will be presented with a string such as 800-692-7753 or 8oo-six427676;laskdjf. Your job is to validate or reject the US phone number based on any combination of the formats provided above. The area code is required. If the country code is provided, you must confirm that the country code is 1. Return true if the string is a valid US phone number; otherwise return false.
* Sample validation data was provided.
* [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp),
* [regexpal.com](https://www.regexpal.com/index.php),
* [regex101.com](https://regex101.com/r/h2HCMZ/1/)

```javascript
/***********************************************************************
 * JavaScript Algorithms and Data Structures Projects:                 *
 * Telephone Number Validator, JJ 2018                                 *
 * https://repl.it/@JohnJohnson2/FCCProjectTelephoneNumberValidatorjs  *
 ***********************************************************************/
//My solution
function telephoneCheck(str) {
  // Good luck!
  //RegExp was validated here: https://regex101.com/r/h2HCMZ/1/
 var phoNum = /^(1\s?)?(\(\d{3}\)|\d{3})[\s\-]?\d{3}[\s\-]?\d{4}$/;
 console.log(phoNum.test(str));
 return phoNum.test(str);
};
//Tests Here:
telephoneCheck("555-555-5555");// should return a boolean.
telephoneCheck("1 555-555-5555");// should return true.
telephoneCheck("1 (555) 555-5555");// should return true.
telephoneCheck("5555555555");// should return true.
telephoneCheck("555-555-5555");// should return true.
telephoneCheck("(555)555-5555");// should return true.
telephoneCheck("1(555)555-5555");// should return true.
telephoneCheck("555-5555");// should return false.
telephoneCheck("5555555");// should return false.
telephoneCheck("1 555)555-5555");// should return false.
telephoneCheck("1 555 555 5555");// should return true.
telephoneCheck("1 456 789 4444");// should return true.
telephoneCheck("123**&!!asdf#");// should return false.
telephoneCheck("55555555");// should return false.
telephoneCheck("(6054756961)");// should return false
telephoneCheck("2 (757) 622-7382");// should return false.
telephoneCheck("0 (757) 622-7382");// should return false.
telephoneCheck("-1 (757) 622-7382");// should return false
telephoneCheck("2 757 622-7382");// should return false.
telephoneCheck("10 (757) 622-7382");// should return false.
telephoneCheck("27576227382");// should return false.
telephoneCheck("(275)76227382");// should return false.
telephoneCheck("2(757)6227382");// should return false.
telephoneCheck("2(757)622-7382");// should return false.
telephoneCheck("555)-555-5555");// should return false.
telephoneCheck("(555-555-5555");// should return false.
telephoneCheck("(555)5(55?)-5555");// should return false.
```
This also was not too hard but validating the regexp to get the tests to pass took a lot of time I actually started working on it yesterday.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedTelephone Number Validator

All code is in GitHub and repl.it here: [repl.it FCCProjectTelephoneNumberValidator.js](https://repl.it/@JohnJohnson2/FCCProjectTelephoneNumberValidatorjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)

### Day 27: August 20, Monday

**Today 's Progress**: I continue work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: Today focused on trying to define the challenge Caesar Cipher (or ROT13) and meet the requirements to pass This project. CaesarCipher.js is located here:[FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects).

After examining the requirements I made the following user story, As a user I want to: enter a ROT13 encoded string as input to a function which will returns a decoded plain text string. also:
* All letters will be uppercase.
* Do not transform any non-alphabetic character (i.e. spaces, punctuation), but be sure to pass them on in the result. I used the following:
* [String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace),
* [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode),
* [ternary operator](https://www.w3schools.com/js/js_operators.asp)

```javascript
console.log("Caesars Cipher")
//Write a function which takes a ROT13 encoded string as input and returns a decoded string.
/***************************************************************
 * JavaScript Algorithms and Data Structures Projects:         *
 * CaesarsCipher, JJ 2018                                      *
 * https://repl.it/@JohnJohnson2/FCCProjectCaesarsCipher       *
 ***************************************************************/
//My solution
function rot13(str) { // LBH QVQ VG!
  let myStr = "";
  console.log(str + "");//Debugging str contents
  console.log((str + "").replace(/[A-Z]/gi, function (myStr) { return String.fromCharCode(myStr.charCodeAt(0) + (myStr.toLowerCase() < "n" ? 13 : -13));}));//Debugging conversion routine, should decode in ROT 13 or encode if plain text
  return (str + "").replace(/[A-Z]/gi, function (myStr) {
    return String.fromCharCode(myStr.charCodeAt(0) + (myStr.toLowerCase() < "n" ? 13 : -13));
  });
};
// Change the inputs below to test
rot13("SERR PBQR PNZC");
rot13("My Test");
```
This was not too hard but I did have some minor code problems that caused a couple refactoring of the code get the tests to pass. Then I wasn't happy and wanted to use ternary operator `?` and `.replace`.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedCaesars Cipher

All code is in GitHub and repl.it here: [repl.it FCCProjectCaesarsCipher](https://repl.it/@JohnJohnson2/FCCProjectCaesarsCipher) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)


### Day 26: August 19, Sunday

**Today 's Progress**: I Started work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: I focused on trying to define the challenge and fully understand the requirements to pass these projects. This isn't like the other challenges as these are for the certification.  I made a place in the FCC-Projects repo on GitHub here in [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects) to store my projects. I had previously did the first project so moved on to the second today. my goal is to complete one a day but some may take longer.

After examining the requirements I made the following user story, As a user I want to: convert the given number into a roman numeral, and all roman numerals answers should be upper-case. I used the following:
* [Modulus (Division Remainder)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)
* [Array.lengthr](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length),
* [Assignment operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment_Operators)
* [Converting Decimal Number lying between 1 to 3999 to Roman Numerals](https://www.geeksforgeeks.org/converting-decimal-number-lying-between-1-to-3999-to-roman-numerals/),

```javascript
console.log("Roman Numeral Converter")
//Convert the given number into a roman numeral. All roman numerals answers should be provided in upper-case.
 /**************************************************************
 * JavaScript Algorithms and Data Structures Projects:         *
 * Roman Numeral Converter, JJ 2018                            *
 * https://jsfiddle.net/johnny2136/8m6937xd/20/                *
 ***************************************************************/
function convertToRoman(num) {
  //Make 2 arrays.
  const decArr = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1];
  const romArr = ["M", "CM","D","CD","C", "XC", "L", "XL", "X","IX","V","IV","I"];
  //Variable for solution.
  let romNum = "";// Be carfull not to accidentally add whitespace
  //While loop inside a for to convert the Number to Roman number
  //console.log("Number: " + num);//Debugging
  for (let i = 0; i <= decArr.length; i++) {     
    while (num % decArr[i] < num) {
      //console.log(num);//Debugging
      romNum += romArr[i];       
      num -= decArr[i];
      //console.log(romNum);//Debugging
      //console.log(num);//Debugging
    };
  };
  console.log(romNum);
  return romNum;
};
//Unit tests:
convertToRoman(36);//should return "XXXVI"
convertToRoman(2); //should return "II".
convertToRoman(3); //should return "III".
convertToRoman(4); //should return "IV".
convertToRoman(5); //should return "V".
convertToRoman(9); //should return "IX".
convertToRoman(12); //should return "XII".
convertToRoman(16); //should return "XVI".
convertToRoman(29); //should return "XXIX".
convertToRoman(44); //should return "XLIV".
convertToRoman(45); //should return "XLV"
convertToRoman(68); //should return "LXVIII"
convertToRoman(83); //should return "LXXXIII"
convertToRoman(97); //should return "XCVII"
convertToRoman(99); //should return "XCIX"
convertToRoman(400); //should return "CD"
convertToRoman(500); //should return "D"
convertToRoman(501); //should return "DI"
convertToRoman(649); //should return "DCXLIX"
convertToRoman(798); //should return "DCCXCVIII"
convertToRoman(891); //should return "DCCCXCI"
convertToRoman(1000); //should return "M"
convertToRoman(1004); //should return "MIV"
convertToRoman(1006); //should return "MVI"
convertToRoman(1023); //should return "MXXIII"
convertToRoman(2014); //should return "MMXIV"
convertToRoman(3999); //should return "MMMCMXCIX"
```
This was pretty straight forward but I did have some minor code problems that caused hours of debugging to get the tests to pass.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedPalindrome Checker
* PassedRoman Numeral Converter

All code is in GitHub and repl.it here: [repl.it FCC_Projects_RomanNumeralConverter.js](https://repl.it/@JohnJohnson2/FCCProjects-RomanNumeralConverterjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)


## Day 25: August 18, Saturday

**Today 's Progress**: I completed work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: I focused on trying to understand the algorithm process and writing code. The Algorithms today were very complex, I once again had to rely on hints. I used the following resources in developing my solutions.

After searching and studying, I learned something new from the following:
* [Object.prototype.hasOwnProperty()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty)
* [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator),
* [Wikipedia Orbital Period](https://en.wikipedia.org/wiki/Orbital_period)
* [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),

```javascript
console.log("Map the Debris");
//Return a new array that transforms the elements' average altitude into their orbital periods (in seconds). The array will contain objects in the format {name: 'name', avgAlt: avgAlt}. You can read about orbital periods on [Wikipedia](https://en.wikipedia.org/wiki/Orbital_period). The values should be rounded to the nearest whole number. The body being orbited is Earth. The radius of the earth is 6367.4447 kilometers, and the GM value of earth is 398600.4418 km3s-2.
function orbitalPeriod(arr) {
  const GM = 398600.4418;
  const earthRadius = 6367.4447;
  let a = 2 * Math.PI;
  let myArr = [];
  let getOrbPeriod = function(obj) {
    let c = Math.pow(earthRadius + obj.avgAlt, 3);
    let b = Math.sqrt(c / GM);
    let orbPeriod = Math.round(a * b);
    delete obj.avgAlt;
    obj.orbitalPeriod = orbPeriod;
    return obj;
  };
  for (var element in arr) {
    myArr.push(getOrbPeriod(arr[element]));
  }
  console.log(myArr);
  return myArr;
};
// test here
orbitalPeriod([{name : "sputnik", avgAlt : 35873.5553}]);
console.log("<----------------------next exercise------------------------->");
```
Once more I had to rely heavily on the hints when my first attempts failed. also [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) I can't say enough about this reference!

**Link(s) to work**

1. Finished [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedEverything Be True
* PassedArguments Optional
* PassedMake a Person
* PassedMap the Debris

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)

### Day 24: August 17, Friday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: After a very long week I am finally able to relax a bit I took today off so I could focus on resting and writing code. So the Algorithms today were a mixed bag, some easier than others. I used the following resources in developing my solutions.

After searching and studying, I learned something new from the following:
* [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
* [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
* [Array.prototype.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex),
* [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator),
* [JavaScript Operators](https://www.w3schools.com/js/js_operators.asp)
* [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),

```javascript
console.log("Drop it");
//Given the array arr, iterate through and remove each element starting from the first element (the 0 index) until the function func returns true when the iterated element is passed through it. Then return the rest of the array once the condition is satisfied, otherwise, arr should be returned as an empty array.
//Resources to solve this: [Array.prototype.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex), [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator), [JavaScript Operators](https://www.w3schools.com/js/js_operators.asp), [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),
function dropElements(arr, func) {
  console.log(arr.slice(arr.findIndex(func) >= 0
    ? arr.findIndex(func): arr.length, arr.length));//Used for debugging
  return arr.slice(arr.findIndex(func) >= 0
    ? arr.findIndex(func): arr.length, arr.length);
};
// test here
dropElements([1, 2, 3, 4], function(n) {return n >= 3;});
console.log("<----------------------next exercise------------------------->");

console.log("Steamroller");
//Flatten a nested array. You must account for varying levels of nesting.
function steamrollArray(arr) {
  let myArr = [].concat(...arr);
  console.log(myArr);//Debugging
  //console.log(myArr.some(Array.isArray) ? steamrollArray(myArr) : myArr);//Debugging
  return myArr.some(Array.isArray)
    ? steamrollArray(myArr) : myArr;
   //console.log(myArr); //Debugging
};
// test here
steamrollArray([[["a"]], [["b"]]]);// should return ["a", "b"].
steamrollArray([1, [2], [3, [[4]]]]);// should return [1, 2, 3, 4].
steamrollArray([1, [], [3, [[4]]]]);// should return [1, 3, 4].
steamrollArray([1, {}, [3, [[4]]]]);// should return [1, {}, 3, 4].
console.log("<----------------------next exercise------------------------->");
```
I still find myself having to rely heavily on the hints and [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) I can't say enough about this reference!

**Link(s) to work**

1. Continuing [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedDrop it
* PassedSteamroller
* PassedBinary Agents

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 23: August 16, Thursday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Another long day and long commute, barely got through one challenge.

```javascript
console.log("Smallest Common Multiple");
//Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters. The range will be an array of two numbers that will not necessarily be in numerical order. For example, if given 1 and 3, find the smallest common multiple of both 1 and 3 that is also evenly divisible by all numbers between 1 and 3. The answer here would be 6.
function smallestCommons(arr) {
let max = Math.max(arr[0],arr[1]);
let min = Math.min(arr[0],arr[1]);
//console.log(max + " & " + min);//Debugging

  function smallComMulti(a, b){ //find smallest Common Multiple
    for(var i = 1; i <= b; i++){     
      if((i * a) % b === 0){
        //console.log(i * a);//Debugging
        return (i * a);
      }
    }   
  };    
  let myNum = smallComMulti(max, min);
  for(var ii = min + 1; ii < max; ii++) {    
    myNum = smallComMulti(myNum, ii);   
  }
  console.log(myNum);
  return myNum;
};
// test here
smallestCommons([1,5]);
console.log("<----------------------next exercise------------------------->");
```
I had to rely on the hints and [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference).

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSmallest Common Multiple

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 22: August 15, Wednesday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Another long day and longer commute, barely got through two challenges.

```javascript
console.log("Sum All Primes");
//Sum all the prime numbers up to and including the provided number. A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two. The provided number may not be a prime.
function sumPrimes(num) {
  function myPrime(number){
      for (let i = 2; i <= number; i++){
          if(number % i === 0 && number!= i){
             return false;
          }
       }
    return true;
  };
  if (num === 1){
    return 0;
  };
  if(myPrime(num) === false){
    return sumPrimes(num - 1);
  };
  // Check if your number is prime
  if(myPrime(num) === true){
    return num + sumPrimes(num - 1);
  }
};
// test here
console.log(sumPrimes(10));
console.log("<----------------------next exercise------------------------->");
```
I had to rely on the hints to get this.

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSum All Odd Fibonacci Numbers
* PassedSum All Primes
All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 21: August 14, Tuesday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Don't have much time tonight, only worked through two challenges. I started a third but didn't finish it.

```javascript
console.log("Convert HTML Entities");
//Convert the characters &, <, >, " (double quote), and ' (apostrophe), in a string to their corresponding HTML entities. (You got to be kidding me!!!)
 function convertHTML(str) {
      const htmlEnt={
        '&':'&amp;',
        '<':'&lt;',
        '>':'&gt;',
        '\"':'&quot;',
        '\'':"&apos;"
      };
  return str.split('').map(function(ojbect){//Use Split and map function to filter str.
        return htmlEnt[ojbect] || ojbect;
      }).join('');//Use .join prototype
  };  
//test here
console.log(convertHTML("Dolce & Gabbana")); //should return Dolce &​amp; Gabbana.
console.log(convertHTML("Hamburgers < Pizza < Tacos")); //should return Hamburgers &​lt; Pizza &​lt; Tacos.
console.log(convertHTML("Sixty > twelve")); //should return Sixty &​gt; twelve.
console.log(convertHTML('Stuff in "quotation marks"')); //should return Stuff in &​quot;quotation marks&​quot;.
console.log(convertHTML("Schindler's List")); //should return Schindler&​apos;s List.
console.log(convertHTML("<>")); //should return &​lt;&​gt;.
console.log(convertHTML("abc")); //should return abc.
console.log("<----------------------next exercise------------------------->");
```
This one used elements from previous Challenges.

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSorted Union
* PassedConvert HTML Entities
All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)

## Day 20: August 13, Monday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: I need to find out why its so hard to do these Challenges, again today I spent hours trying to get something I thought should work to actually work. I used to think I was pretty good at coming up with logical algorithms for solving problems but I am really struggling nothing seems to work, maybe there are too many options `for` vice `map` and the concept of `callbacks` is hard for me to grasp, I will keep trying, maybe it will get easier with practice.

```javascript
console.log("Pig Latin");
//Translate the provided string to pig latin. Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay". If a word begins with a vowel you just add "way" to the end. Input strings are guaranteed to be English words in all lowercase.
function translatePigLatin(str) {
  var pigLatin = '';
  var RegExp = /[aeiou]/gi;
  if (str[0].match(RegExp)) {
    pigLatin = str + 'way';
    //console.log('Test 1st letter is a aeiou');
  } else if(str.match(RegExp) === null) {//added to get last test to pass.
    pigLatin = str + 'ay';
    //console.log('Test there are only consonants');
  } else {
    var vowelIndex = str.indexOf(str.match(RegExp)[0]);
    //console.log(vowelIndex = str.indexOf(str.match(RegExp)[0]));
    pigLatin = str.substr(vowelIndex) + str.substr(0, vowelIndex) + 'ay';
  }  
  console.log(pigLatin);
  return pigLatin;
}
translatePigLatin("consonant");// should return "onsonantcay
translatePigLatin("california");// should return "aliforniacay".
translatePigLatin("paragraphs");// should return "aragraphspay".
translatePigLatin("glove");// should return "oveglay".
translatePigLatin("algorithm");// should return "algorithmway".
translatePigLatin("eight");// should return "eightway".
translatePigLatin("myclm");// should return "eightway".
translatePigLatin("shmmnd");// should return "eightway".
console.log("<----------------------next exercise------------------------->");
```
This one seemed at first pretty straight forward but I couldn't get the last test to pass. I finally looked at the hints and saw I wasn't checking for consonants, I finally got it to work... [String.prototype.match()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match), [w3schools.com](https://www.w3schools.com/js/js_regexp.asp) and [Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedPig Latin
* PassedSearch and Replace
* PassedDNA Pairing
* PassedMissing letters

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 19: August 12, Sunday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: One word AAAAARRRRRRRRRGGGGHHHH!!!!! These are maddening even the solutions I looked up when I was struggling didn't work:

```javascript
console.log("Spinal Tap Case");
//Convert a string to spinal case. Spinal case is all-lowercase-words-joined-by-dashes.
function spinalCase(str) {
  // Replace low-upper case to low-space-uppercase
  str = str.replace(/([a-z])([A-Z])/g, '$1 $2');
  // Split on whitespace and underscores and join with dash
  console.log(str.toLowerCase().split(/(?:_| )+/) .join('-'));
  return str.toLowerCase().split(/(?:_| )+/) .join('-');
}
// Unit test:
spinalCase("This Is Spinal Tap");// should return "this-is-spinal-tap".
spinalCase("thisIsSpinalTap");// should return "this-is-spinal-tap".
spinalCase("The_Andy_Griffith_Show");// should return "the-andy-griffith-show".
spinalCase("Teletubbies say Eh-oh");// should return "teletubbies-say-eh-oh".
spinalCase("AllThe-small Things");// should return "all-the-small-things".
console.log("<----------------------next exercise------------------------->");
```
This one hours finally I gave up and searched for a solution and even that needed altering to get it to work... [String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedWherefore art thou
* PassedSpinal Tap Case

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 18: August 11, Saturday

**Today 's Progress**: I started work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: These algorithm challenges are just as hard as the other algorithm challenge I took the approach of visualizing the requirements and array sets then walking though the JS steps. For example:

```javascript
console.log("Seek and Destroy");
//You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments. Note: You have to use the arguments object.
function destroyer(arr, a1, a2) {
  // Remove all the values
  console.log("Initial Array -->  " + arguments[0]);//Array argument 0  
  var args = Array.from(arguments).slice(1);
  console.log("Filter argument -->  " + (args = Array.from(arguments).slice(1)));//eval arguments
    return arr.filter(function(val) {
      return !args.includes(val);
    });
  return arr;
}
console.log(destroyer([1, 2, 3, 1, 2, 3], 2, 3)); //should return [1, 1].
console.log(destroyer([1, 2, 3, 5, 1, 2, 3], 2, 3)); //should return [1, 5, 1].
console.log(destroyer([3, 5, 1, 2, 2], 2, 3, 5)); //should return [1].
console.log(destroyer([2, 3, 2, 3], 2, 3)); //should return [].
console.log(destroyer(["tree", "hamburger", 53], "tree", 53)); //should return ["hamburger"].
console.log(destroyer(["possum", "trollo", 12, "safari", "hotdog", 92, 65, "grandma", "bugati", "trojan", "yacht"], "yacht", "possum", "trollo", "safari", "hotdog", "grandma", "bugati", "trojan")); //should return [12,92,65].
console.log("<----------------------next exercise------------------------->");
```
This one took some google searching and trying to figure out how to get `Array.from(arguments).slice` to work in my solution... [Arguments object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSum All Numbers in a Range
* PassedDiff Two Arrays
* PassedSeek and Destroy

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)

### Day 17: August 10, Friday

**Today 's Progress**: I finished work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Some of these Challenges continue to be pretty hard while others very simple, I am dealing with the aggravating ones as well as the easy ones.

For example an easy one:
```javascript
//Introduction to Currying and Partial Application
//Fill in the body of the add function so it uses currying to add parameters x, y, and z.
function add(x) {
  // Add your code below this line
    return function(y) {
      return function(z) {
        return x + y + z;
      }
    }  
  // Add your code above this line
}
console.log(add(10)(20)(30));//should return 60.
console.log(add(1)(2)(3)); //should return 6.
console.log(add(11)(22)(33)); //should return 66.
//Your code should include a final statement that returns x + y + z.
console.log("-------------------Next------------------------");
```
And a Aggravating one:
```JavaScript
//Apply Functional Programming to Convert Strings to URL Slugs
//Fill in the urlSlug function so it converts a string title and returns the hyphenated version for the URL. You can use any of the methods covered in this section, and don't use replace. Here are the requirements:
//The input is a string with spaces and title-cased words
//The output is a string with the spaces between words replaced by a hyphen (-)
//The output should be all lower-cased letters
//The output should not have any spaces
// the global variable
var globalTitle = "Winter Is Coming";
// Add your code below this line
function urlSlug(title) {
console.log("First --> "+ title);//DEbugging
var myTitle = title.split(/\W+/); //from previous excersize
console.log("Second  --> "+ myTitle);//DEbugging
var filterTitle = myTitle.filter(function(obj){// my solution-Mozilla.org
return /\S/.test(obj);// Mozilla.org
});
console.log("Third  --> "+ filterTitle.join("-").toLowerCase());//DEbugging
console.log("Finally Global  --> "+ globalTitle);//DEbugging
return filterTitle.join("-").toLowerCase();// StackOverflow!!!
};// ARRRGGGGGHHH!!!!! This was hard!!!!!
// Add your code above this line
var winterComing = urlSlug(globalTitle); // Should be "winter-is-coming"
//Additional tests....
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");// should return "a-mind-needs-books-like-a-sword-needs-a-whetstone".
urlSlug("Hold The Door");// should return "hold-the-door".(https://stackoverflow.com/questions/6442327/using-split-join-to-replace-a-string-with-a-array)
//this challange sort of sucked!!! Took me a long time :(
//This helped https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test
//and this https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `split, filter, join` work togather... [StackOverflow.com]((https://stackoverflow.com/questions/6442327/using-split-join-to-replace-a-string-with-a-array))

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedReturn a Sorted Array Without Changing the Original Array
* PassedSplit a String into an Array Using the split Method
* PassedCombine an Array into a String Using the join Method
* PassedApply Functional Programming to Convert Strings to URL Slugs
* PassedUse the every Method to Check that Every Element in an Array Meets a Criteria
* PassedUse the some Method to Check that Any Elements in an Array Meet a Criteria
* PassedIntroduction to Currying and Partial Application

All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)


### Day 16: August 09, Thursday

**Today 's Progress**: I continue to work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Some of the FCC_Challenges were pretty hard others very simple, I am hanging in there.

![XKCD.com](https://imgs.xkcd.com/comics/code_quality_3.png)

```javascript
//Combine Two Arrays Using the concat Method
//Use the concat method in the nonMutatingConcat function to concatenate attach to the end of original. The function should return the concatenated array.
function nonMutatingConcat(original, attach) {
  // Add your code below this line
  console.log((original), (attach));
  console.log("  Now CONCAT!!!");
  let myArr= first.concat(attach);
  console.log(myArr);
  return myArr;
  // Add your code above this line
}
var first = [1, 2, 3];
var second = [4, 5];
nonMutatingConcat(first, second);
//[Array.prototype.concat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `concat`... [Array.prototype.concat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedRemove Elements from an Array Using slice Instead of splice
* PassedCombine Two Arrays Using the concat Method
* PassedAdd Elements to the End of an Array Using concat Instead of push
* PassedUse the reduce Method to Analyze Data
* PassedSort an Array Alphabetically using the sort Method


All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)


### Day 15: August 08, Wednesday

**Today 's Progress**: I continue to work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: These FCC_Challenges are pretty tricky, thank goodness for google! :grin:

![XKCD.com](https://imgs.xkcd.com/comics/bad_code.png)

```javascript
//Implement the filter Method on a Prototype
//Write your own Array.prototype.myFilter(), which should behave exactly like Array.prototype.filter(). You may use a for loop or the Array.prototype.forEach() method.
// the global Array
var s = [23, 65, 98, 5];
Array.prototype.myFilter = function(callback){
  var newArray = [];
  // Add your code below this line
   //console.log("this -->" + s);//Debug  
   this.forEach(function(obj) { //My solution
    //console.log("this -->" + obj);//Debug  
     if (callback(obj) == true) { //My solution
       newArray.push(obj); } });//My solution
      //console.log("this -->" + newArray);//Debug  
  // Add your code above this line
  return newArray;
};
var new_s = s.myFilter(function(item){
  return item % 2 === 1;
});
// Resources for this exercise: [Array Map, Filter and Reduce in JS](https://atendesigngroup.com/blog/array-map-filter-and-reduce-js)
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `forEach` in conjunction with `callback`... [Array Map, Filter and Reduce in JS](https://atendesigngroup.com/blog/array-map-filter-and-reduce-js)

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedImplement map on a Prototype
* PassedUse the filter Method to Extract Data from an Array
* PassedImplement the filter Method on a Prototype
* PassedReturn Part of an Array Using the slice Method to Extract Data from an Array


All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)


### Day 14: August 07, Tuesday

**Today 's Progress**: I finished the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section and started [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Oh no these FCC_Challenges are not at all straight forward, and there are no hints or examples it's very challenging and not a lot of fun Thank goodness there is google! You can really tell the folks who did the last round of challenges cared about passing on information rather than this round of challenges designed to trick the student and make things obscure and nerve wracking. Today it was all about dealing with these frustrating misleading challenges yuck!

![XKCD.com](https://imgs.xkcd.com/comics/code_quality.png)

```javascript
//Implement map on a Prototype
//Write your own Array.prototype.myMap(), which should behave exactly like Array.prototype.map(). You may use a for loop or the forEach method.
// the global Array
var s = [23, 65, 98, 5];
Array.prototype.myMap = function(callback){
  var newArray = [];
  // Add your code below this line
   for (let i = 0; i < this.length; i++) {
     newArray.push(callback(this[i]));
  };
  // Add your code above this line
  return newArray;
};
var new_s = s.myMap(function(item){
  return console.log(item * 2);
});
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out callback...

**Link(s) to work**

1. Continued [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedUse a Mixin to Add Common Behavior Between Unrelated Objects
* PassedUse Closure to Protect Properties Within an Object from Being Modified Externally
* PassedUnderstand the Immediately Invoked Function Expression (IIFE)
* PassedUse an IIFE to Create a Module

2. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedLearn About Functional Programming
* PassedUnderstand Functional Programming Terminology
* PassedUnderstand the Hazards of Using Imperative Code
* PassedAvoid Mutations and Side Effects Using Functional Programming
* PassedPass Arguments to Avoid External Dependence in a Function
* PassedRefactor Global Variables Out of Functions
* PassedUse the map Method to Extract Data from an Array


All code is in GitHub and repl.it here: [Repl.it OOP](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming), [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub OOP](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js), [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)

### Day 13: August 06, Monday

**Today 's Progress**: I worked on the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: I like these FCC_Challenges very straight forward I wish all were this way :grin:. Today it was all about Constructors and prototypes pretty cool stuff. Since today was such a good coding day I thought I would share my favorite cartoon series, enjoy! 

![XKCD.com](https://imgs.xkcd.com/comics/disaster_movie.png)

```javascript
//Add Methods After Inheritance
//Add all necessary code so the Dog object inherits from Animal and the Dog's prototype constructor is set to Dog. Then add a bark() method to the Dog object so that beagle can both eat() and bark(). The bark() method should print "Woof!" to the console.
function Animal() { }
Animal.prototype.eat = function() { console.log("nom nom nom"); };
function Dog() { }
// Add your code below this line
Dog.prototype = Object.create(Animal.prototype);// my solution
Dog.prototype.constructor = Dog;// my solution
Dog.prototype.bark = function() {// my solution
  console.log( "Woof!");// my solution
};
// Add your code above this line
let beagle8 = new Dog();
beagle8.eat(); // Should print "nom nom nom"
beagle8.bark(); // Should print "Woof!" 
console.log("--------------------------------------------");
```
and the last one my personal favorite `Mixin` :lol:
```javascript
//Use a Mixin to Add Common Behavior Between Unrelated Objects
//Create a mixin named glideMixin that defines a method named glide. Then use the glideMixin to give both bird and boat the ability to glide.
let bird = {
  name: "Donald",
  numLegs: 2
};
let boat = {
  name: "Warrior",
  type: "race-boat"
};
// Add your code below this line
let glideMixin = function(obj) {
  obj.glide = function() {
    console.log("Gliding, wooosh!");
  }
};
 glideMixin(bird);
 glideMixin(boat);
bird.glide(); // prints "Gliding, wooosh!"
boat.glide();
console.log(bird); // prints "Gliding, wooosh!"
console.log(boat); // prints "Gliding, wooosh!"
console.log("--------------------------------------------");
```
**Link(s) to work**

1. Continued [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedIterate Over All Properties
* PassedUnderstand the Constructor Property
* PassedChange the Prototype to a New Object
* PassedRemember to Set the Constructor Property when Changing the Prototype
* PassedUnderstand Where an Object’s Prototype Comes From
* PassedUnderstand the Prototype Chain
* PassedUse Inheritance So You Don't Repeat Yourself
* PassedInherit Behaviors from a Supertype
* PassedSet the Child's Prototype to an Instance of the Parent
* PassedReset an Inherited Constructor Property
* PassedAdd Methods After Inheritance
* PassedOverride Inherited Methods


All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)

### Day 12: August 05, Sunday

**Today 's Progress**: I worked on the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: These FCC_Challenges were a lot different from the Challenges in the algorithm section that were so tough, there were plenty of good examples and instructions but I manages with the help of Stackoverflow to get them done OOP section seems easy Should get a lot done tomorrow. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) and [Stackoverflow](https://stackoverflow.com)

```javascript
//Use Prototype Properties to Reduce Duplicate Code
//Add a numLegs property to the prototype of Dog
function Dog(name) {
  this.name = name;
}
Dog.prototype.numLegs = 4;
// Add your code above this line
let beagle = new Dog("Snoopy");
console.log(beagle); // prints Snoopy
console.log(Dog); // prints Snoopy
console.log("--------------------------------------------");
```

**Link(s) to work**

1. Started [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedUse Dot Notation to Access the Properties of an Object
* PassedCreate a Method on an Object
* PassedMake Code More Reusable with the this Keyword
* PassedDefine a Constructor Function
* PassedUse a Constructor to Create Objects
* PassedExtend Constructors to Receive Arguments
* PassedVerify an Object's Constructor with instanceof
* PassedUnderstand Own Properties
* PassedUse Prototype Properties to Reduce Duplicate Code


All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)

## Day 11: August 04, Saturday

**Today 's Progress**: I finished the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) and started the [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: Felt good finishing some FCC_Challenges! The Challenges in the algorithm section were tough, there were no examples and vague instructions but I manages with the help of Stackoverflow to get them done OOP section seems easy Should get a lot done tomorrow. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) and [Stackoverflow](https://stackoverflow.com)

```javascript
//Chunky Monkey
//Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.
function chunkArrayInGroups(arr, size) {//My solution reusing slice and push
  var a = 0;      
  var result = [0];
  for(var i = 0; i < arr.length; i += size){
      console.log(a);//Debugging
      result.push(arr.slice(a, size +i));
      a += size;
  }
  console.log(result + " & " + arr); //Debugging
  return result;
}
console.log(chunkArrayInGroups(["a", "b", "c", "d","a", "b", "c", "d"], 2));
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Finished [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

   * PassedChunky Monkey

2. Started [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

   **Introduction to the Object Oriented Programming**

   * PassedCreate a Basic JavaScript Object

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)

### Day 10: August 03, Friday

**Today 's Progress**: I continued working the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is done this has been a trying week with very rough commutes today I left early and still had a 3 hour commute. We did more labs in OpenShift and probes in  CLI as well as configuring the GUI. The weekend is here and I plan on resting and knocking some FCC_Challenges out! Starting tonight. The Challenges, well I got stuck on the second one, and had to read more on `.filter` after that and some false starts I nailed it. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

```javascript
// Falsy Bouncer
//Remove all falsy values from an array.
//Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.
function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  return arr.filter(object => object);
  //or....
  //return arr.filter(Boolean);  
}
console.log(bouncer([7, "ate", "", false, 9]));
console.log(bouncer(["a", "b", "c"])); //should return ["a", "b", "c"].
console.log(bouncer([false, null, 0, NaN, undefined, ""])); //should return [].
console.log(bouncer([1, null, NaN, 2, undefined])); //should return [1, 2].
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedSlice and Splice
* PassedFalsy Bouncer
* PassedWhere do I Belong
* PassedMutations
All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 9: August 02, Thursday

**Today 's Progress**: I continued working the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: Due to dentist appointment no commute today Yay!!!! :smile: I did my homework for the OpenShift class I'm in this week and read over what they went over today. The Challenges continue to be difficult but I'm hanging in there with this 100-day coding challenge. JavaScript is a bit different from plain Java like the `findElement` of an array in Java it's `return Arrays.asList(arr).contains(targetValue);` and in Java script its `var found = array1.find(function(element)` Took me a while to get the one below.

```javascript
//Finders Keepers
//Create a function that looks through an array (first argument) and returns the first element in the array that passes a truth test (second argument). If no element passes the test, return undefined.
function findElement(arr, func) {
  var num;
  console.log(arr);// for Debugging
  //console.log(arr.find((num) => {return func(num)})); //for troubleshooting.
  return arr.find((num) => {return func(num)});
}
console.log(findElement([1, 2, 3, 4], num => num % 2 === 0));//should return 2.
console.log(findElement([1, 3, 5, 8, 9, 10], num => num % 2 === 0)); //should return 8.
console.log(findElement([1, 3, 5, 9], num => num % 2 === 0)); //should return undefined.
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedBooFinders Keepers
* PassedBoo who
* PassedTitle Case a Sentence

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 8: August 01, Wednesday

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

### Day 1: July 25, Wednesday

**Today's Progress**: I've gone through 3 exercises on FreeCodeCamp and did one project.

**Thoughts** II've had many coding classes in college and want to step up my game, I found out that coding is not like riding a bike you don’t just learn it and then know it from now on, I don’t code at work so my skills rusted up quite a bit. I want to revamp them and try and stay current with modern technology I started following students of [CodeClan](https://codeclan.com/) in Scotland and found Free Code Camp so I’m working through the course ware and once done hope to contribute to the project, and it's an awesome feeling when I finally solve an exercise challenge after a lot of failing unit tests that green banner appears and it’s like “YEEEESSSS!!!!!!”.

**Link(s) to work**
1. [Palindrome Checker](https://github.com/Johnny2136/FCC-Projects/blob/master/PalindromeChecker.js)
2. [Introduction to the Debugging Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging)
  * PassedUse the JavaScript Console to Check the Value of a Variable
  * PassedUnderstanding the Differences between the freeCodeCamp and Browser Console
  * PassedUse typeof to Check the Type of a Variable (https://www.freecodecamp.com)
