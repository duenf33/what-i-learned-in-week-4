# 🥴 what-i-learned-in-week-4

![eat sleep code repeat](gifs/eat-sleep-code-repeat.gif)

Last week we were `whiling-away`. It was interesting the many things we are able to accomplish with such simple `while` statement.<br>
**Now** we are going to start off with the:
## ⇢ **`For loop` statement :** <br>

A for loop repeats until a specified condition evaluates to false.<br>
A for statement looks as follows ⇲<br>
```javascript
for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement
```
When a for loop executes, the following occurs ⇲<br>

1. The initializing expression initialExpression, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.<br>
1. The conditionExpression expression is evaluated. If the value of conditionExpression is true, the loop statements execute. If the value of condition is false, the for loop terminates. (If the condition expression is omitted entirely, the condition is assumed to be true.)<br>
1. The statement executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.<br>
1. If present, the update expression incrementExpression is executed.<br>
1. Control returns to Step 2.<br>

For example ⇲<br>
```javascript
function yellingChars(input){
  let str = '';
  for(let i = 0; i < input.length; i++){
    str += input[i] + '!';
  }
  return str;
}
yellingChars('goodness');   // g!o!o!d!n!e!s!s!
yellingChars('oh hello');   // o!h! !h!e!l!l!o!
```
---

## ⇢ **What is an array?**

`Arrays` are generally described as `list-like objects`. They are basically single objects that contain multiple values stored in a list. `Array objects` can be stored in `variables` and dealt with in much the same way as any other type of value, the difference being that we can access each value inside the list individually and being able to loop through it and do the same thing to every value.<br>

Arrays consist of square brackets and elements that are separated by commas. Here below are some examples ⇲<br>
```javascript
let shopping = ['bread', 'milk', 'cheese', 'hummus', 'noodles'];

shopping;
```
In the above example, each element is a string, but in an array we can store various `data types` - `strings`, `numbers`, `objects`, and even `other arrays`. We can also mix `data types` in a `single array` — we do not have to limit ourselves to storing only numbers in one array, and in another only strings. For example ⇲<br> 
```javascript
let sequence = [1, 1, 2, 3, 5, 8, 13];
let random = ['tree', 795, [0, 1, 2]];
```



JavaScript: Converts the first letter of each word of a string in upper case
https://www.w3resource.com/javascript-exercises/javascript-function-exercise-5.php

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice
The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice
The slice() method extracts a section of a string and returns it as a new string, without modifying the original string.