# regex 
- #### Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. 
- we can create regex in  one of two ways: 
-  regex literal /regex/
-  Or calling the constructor function of the RegExp object, as follows:
```
const re = new RegExp("ab+c");
```
### Regex notes 
- using the test methods:
   
```
  const string = `The dog chased cat`
const regex = /the/i;

console.log(regex.test(string))

```