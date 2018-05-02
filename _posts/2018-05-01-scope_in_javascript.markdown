---
layout: post
title:      "Scope in JavaScript"
date:       2018-05-02 02:51:25 +0000
permalink:  scope_in_javascript
---


In JavaScript, scope refers to the applicable context of your code; and scopes can be globally or locally defined.


1. Global Scope

When a variable is declared globally, that variable is recognized by any code within that document.

```
var sample = 2;

console.log(sample); //output: 2
scope(); //output: 2

function scope(){
  return sample; 
}

```


2. Local Scope

On the other hand, when a variable is declared locally, that variable is recognized only within that local environment(i.e., function).

```
console.log(sample); //ReferenceError: sample is not defined
scope(); //output: 2

function scope(){
  var sample = 2; //same result if declared/assigned a value through var or const.
  return sample; 
}

```

3. Function scoped 'var' vs. Block scoped 'let' 'const'

'var' declarations are function scoped, which means that when it's declared within a function, it's locally scoped within that function.  
But when it's declared within a block/curly bracket (e.g., if statement), it may be recognized outside suck block.

```
var bool = true;
if (!!bool){
  var time = 10;
}

console.log(time); //output: 10

```

In contrast, 'const' or 'let' declarations are block scoped, therefore, such declarations will not be recognized outside their block (including a function).

```
var bool = true;
if (!!bool){
  var time = 10;
}

console.log(time); //output: ReferenceError: time is not defined

```






