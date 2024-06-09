---
author: Sam Lam
categories: ["studio tips"]
date: 09/6/2024
featured: false
image: ./images/photoshoot.jpg
title: 30 Days of JavaScript
---

## What is Closure ?

● A closure is created when a function is defined inside another function, and the inner function references variables in the outer function's scope. When the inner function is returned from the outer function, it retains a reference to the outer function's scope, and can continue to access those variables even after the outer function has finished executing. Vice-Versa is not true!!

● In simple terms a closure can "remember" values from its outer function's scope and use them later, even if the outer function has returned and those values would normally be out of scope.

## When to use closure concept ?

FIrst let's summarize the definition as usually the definition gives the answer for when to use..

● From definition you can see that it's used for retrival of values from outer parent function so we can understand that closure can be used for retrival of dead values which have become out of scope. also we can comprehend that it can used for privating some varibles or function.

● Thus closures are useful for creating private variables and functions, implementing partial function application, and preserving state in asynchronous code.

● While writing the code whenever there is a need for these types of thing try to incorporate this closure concept i.e. In a programmer languge it's called lexical environment

## When and How to use closure concept ?
```js
Private variables and functions
const makeCounter = () => {
  let count = 0;

  return () => {
    count++;
    console.log(count);
  }
}

let counter = makeCounter();
counter(); // 1
counter(); // 2
counter(); // 3
```

```js
Partial function
function add(x) {
  return function(y) {
    return x + y;
  }
}

let add5 = add(5);
console.log(add5(3)); // 8
```

