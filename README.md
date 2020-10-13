# 🥴 what-i-learned-in-week-4

![eat sleep code repeat](gifs/eat-sleep-code-repeat.gif)

Last week we were `whiling-away`. It was interesting the many things we are able to accomplish with such simple `while` statement.<br>
**Now** we are going to start off with the:
## ⇢ **`For loop` statement ↘︎** <br>

A for loop repeats until a specified condition evaluates to false.<br>
A for statement looks as follows ⇲<br>
```javascript
for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement
```
When a `'for loop executes'`, the following occurs ⇲<br>

1. The initializing expression `'initialExpression'`, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.<br>
1. The `'conditionExpression'` expression is evaluated. If the value of `'conditionExpression'` is true, the loop statements execute. If the value of `'condition'` is false, the `for loop` terminates. (If the `'condition'` expression is omitted entirely, the condition is assumed to be true.)<br>
1. The `'statement'` executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.<br>
1. If present, the update expression `'incrementExpression'` is executed.<br>
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

## ⇢ **🛑 What is an array ❓**
![angry-coder](gifs/angry-coder.gif)

`Arrays` are generally described as `list-like objects`. They are basically single objects that contain multiple values stored in a list. `Array objects` can be stored in `variables` and dealt with in much the same way as any other type of value, the difference being that we can access each value inside the list individually and being able to loop through it and do the same thing to every value.<br>

Arrays consist of square brackets and elements that are separated by commas. Here below are some examples ⇲<br>
```javascript
let shopping = ['bread', 'milk', 'cheese', 'hummus', 'noodles'];

shopping;
```
In the above example, each element is a string, but in an array we can store various `data types` - `strings`, `numbers`, `objects`, and even `other arrays`. We can also mix `data types` in a `single array` — we do not have to limit ourselves to storing only numbers in one array, and in another only strings. For example ⇲<br> 
```javascript
let sequence = [1, 1, 2, 3, 5, 8, 13];
let random = ['tree', 795, 0, 1, 2];
```
We can then ***access*** individual items in the array using bracket notation, in the same way that you accessed the letters in a string.<br>
```javascript
random[0];
// returns 'tree'
```
We can also modify an item in an array by simply giving a single array item a new value. Try this ⇲<br>
```javascript
radom[0] = 'numbers'
// random will return ['number', 795, 0, 1, 2];
```
We can find out the `length` of an `array`, meaning counting how many items are in the specific `array` in exactly the same way as we find out the length, in characters, of a `string` by using the length property. For example ⇲<br>
```javascript
random.length;
// it will return 5
```
This has other uses, but now going back to the previous topic, it is most commonly used to tell a `loop` to keep going until it has looped through all the items in an `array`. For example ⇲<br>
```javascript
let example = [1, 1, 2, 3, 5, 8, 13];
for (let i = 0; i < example.length; i++) {
  console.log(example[i]);
}
```
👆 This `for loop` starts **looping** at item number `0` in the `array`, then it stops **looping** at the `item  number` equal to the `length` of the `array`. This works for an `array` of `any length`, but in this case it stops `looping` at item `number 7` <br>

---

## `🕳 Array Methods 🕳`
![coding-monkey](gifs/coding-monkey.gif)
There are different types of methods that are used for many different things in conjunction with `arrays` and `loops`. These help `push`, `pop`, `unshift`, `shift`,`split`, `slice`, `splice`,  etc. an array in order to accomplish the code desired.<br>
Here below we are going to list only a few of the methods that are out there, only the few that we are allowed to use in this `week 🤷‍♂️` ⇲ <br>

* **`push()`⇲**<br>
  This method adds one or more elements to the end of an array and returns the new length of the array.<br>
  ```javascript
    const animals = ['pigs', 'goats', 'sheep'];
    const count = animals.push('cows');

    console.log(count);
    // output: 4
    console.log(animals);
    // output: Array ["pigs", "goats", "sheep", "cows"]
    ```
* **`pop()`⇲**<br>
  This method removes the *last* *element* from an array and returns that element. This method changes the length of the array.<br>
  ```javascript
    const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];

    console.log(plants.pop());
    // output: "tomato"
  ```
* **`unshift()`⇲**<br>
  This method adds new items to the beginning of an array and returns the new length. This method changes the length of an array. To add new items at the end of an array, use the push() method.<br>
  ```javascript
    const array1 = [1, 2, 3];

    console.log(array1.unshift(4, 5));
    // output: 5

    console.log(array1);
    // output: Array [4, 5, 1, 2, 3]
  ```
  
* **`shift()`⇲**<br>
  This method removes the first element from an array and returns that removed element. This method changes the length of the array.<br>
  ```javascript
    const array1 = [1, 2, 3];

    const firstElement = array1.shift();

    console.log(array1);
    // output: Array [2, 3]

    console.log(firstElement);
    // output: 1
  ```
  
* **`split()`⇲**<br>
  The split() method divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array.  The division is done by searching for a pattern; where the pattern is provided as the first parameter in the method's call.<br>
  ```javascript
    const str = 'The quick brown fox jumps over the lazy dog.';

    const words = str.split(' ');
    console.log(words[3]);
    // output: "fox"

    const chars = str.split('');
    console.log(chars[8]);
    // output: "k"

    const strCopy = str.split();
    console.log(strCopy);
    // output: Array ["The quick brown fox jumps over the lazy dog."]
  ```
  
* **`slice()`⇲**<br>
  This method returns a copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. The original array will not be modified.<br>
  ```javascript
    const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

    console.log(animals.slice(2));
    // expected output: Array ["camel", "duck", "elephant"]

    console.log(animals.slice(2, 4));
    // expected output: Array ["camel", "duck"]

    console.log(animals.slice(1, 5));
    // expected output: Array ["bison", "camel", "duck", "elephant"]
  ```
  
* **`splice()`⇲**<br>
  The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.<br>
  ```javascript
    const months = ['Jan', 'March', 'April', 'June'];
    months.splice(1, 0, 'Feb');
    // inserts at index 1
    console.log(months);
    // expected output: Array ["Jan", "Feb", "March", "April", "June"]

    months.splice(4, 1, 'May');
    // replaces 1 element at index 4
    console.log(months);
    // expected output: Array ["Jan", "Feb", "March", "April", "May"]
  ```
  
And there are more methods that we have also used such as ⇲<br>
* The charAt() method is used to get the specified character from a string.<br>

* The toUpperCase() method is used to convert the string value to uppercase.<br>

* The toLowerCase() method is used to convert the string value to lowercase.<br>

* The join() method joins all elements of an array into a string.<br>

After completing a for loop we would return the final string :<br>
```javascript
return newarray1.join(' ');
```


https://www.w3resource.com/javascript-exercises/javascript-function-exercise-5.php