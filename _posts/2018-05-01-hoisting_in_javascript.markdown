---
layout: post
title:      "Hoisting in JavaScript"
date:       2018-05-02 01:56:23 +0000
permalink:  hoisting_in_javascript
---


In essence, hoisting is a JavaScript behavior that moves declarations of functions/variables to the **top** of their scope before code execution.

This allows a variable/function to be used **before** it has been declared.

There is one important caveat through--hoisting moves declarations to the top, but assignments remains intact.  

So, as shown in the example below, if a variable is used before it is declared and assigned a value, the interpreter will recognize the variable as previously declared but only as "undefined".

```
console.log(hoisting); //output: undefined
var hoisting = 2;

```

This is because after hoisting, the above code becomes equivalent to the code below:

```
var hoisting; // After hoisting, the declaration is moved to the top as an undefined variable.

console.log(hoisting); // Therefore, output: undefined
hoisting = 2;

```

Further, when hoisting a function, it's important to note that while function declarations are hoisted, function expressions are not.

In the below example, the function declaration is hoisted, thereby the function value 2 will be recognized by the interpreter.
```
sample(); //output: 2

function sample(){
  return 2;
}

```

However, in the below example, hoisting() will return a ReferenceError because it is defined later through a function expression.
```
hoisting(); //output: ReferenceError: hoisting is not defined

hoisting = function sample(){
  return 2;
}

```

Of further note, a more recent version of JavaScript, ES6, comes with a few changes that affects the hoisting mechanism.  One most important change is that ES6 is not so kind to variables that are used before their 'let' or 'const' declaration and assignments.

This difference is demonstrated by the different outputs resulting from the examples below:

Example 1
```
sample(); //output: undefined
function sample(){
  return hoisting;
  var hoisting = 2;
}

```

Example 2 (same result when the value is declared with 'const'
```
sample(); //output: ReferenceError: hoisting is not defined
function sample(){
  return hoisting;
  let hoisting = 2;
}

```
Accordingly, under ES6,  users should always declare and assign value to a variable before its use.



On a side note:

* With declarations through 'let', it's important to note that 'let' declared variable's scope is bound to the block in which it is declared and not the function in which it is declared.
* With declarations through 'const', it's important to note that 'const' declared variable's value cannot be modified once assigned.

So, when a value is declared within a function through 'let' without assignment, the function will return 'undefined' whereas a value declared with 'const' without assignment will return a 'SyntaxError'.


