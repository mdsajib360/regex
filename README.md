# regex 
- #### Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. 
- we can create regex in  one of two ways: 
-  regex literal /regex/
-  Or calling the constructor function of the RegExp object, as follows:
```
const re = new RegExp("ab+c");
```
### Regex notes 
- using the **test** methods:
   
```
  const string = `The dog chased cat`
const regex = /the/i;

console.log(regex.test(string))

```
- Match Literal Strings :
  - regex are case sensitive
- Match different possibilities:
  - Using regexes like /coding/, you can look for the pattern coding in another string.
```
let petString = "James has a pet cat.";
let petRegex = /dog|cat|bird|fisht/; // Change this line
let result = petRegex.test(petString);
console.log(result)
```
- ignore case in a regex: 
```
let myString = "freeCodeCamp";
let fccRegex = /freeCodeCamp/i; // Change this line
let result = fccRegex.test(myString);
```

- Extract Matches using str.match method

```
'Abdul Awal Sajib'.match(/awal/i)
```
- match multiple characters :
  - use g falg 
- Match Anything with Wildcard Period
 -  wildcard character (.)
 - this regex will matches the strings run, sun, fun, pun, nun, and bun. 
 -  
```
  let exampleStr = "Let's have fun with regular expressions!";
  let unRegex = /.un/; // Change this line
  let result = unRegex.test(exampleStr);
  ```

- match all the vowels from a string . using [] bracket: 
  
```
   let quoteSample = "Beware of bugs in the above code; I have only proved it correct, not tried it.";
   let vowelRegex = /[aeiou]/ig; // Change this line
   let result = quoteSample.match(vowelRegex); // Change this line

   console.log(result.length);


  ```