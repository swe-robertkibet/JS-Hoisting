# Hoisting

Hoisting is a JavaScript mechanism where variables and function declarations are **moved to the top of their containing scope** during the compile phase **before** the code is executed. 
This means that regardless of where variables and functions are declared within a scope, they are moved to the top of that scope by the JavaScript engine.


**NB:** Only the declarations are hoisted, not the initializations. 


## 1. Variable Hoisting

When you declare a variable using *var*, *let*, or *const*, the declaration is hoisted to the top of its scope. 
However, the initialization remains in place. 

For example:
```javascript
console.log(x); // undefined
var x = 5;
```
This code behaves as if it were interpreted like this:
```javascript
var x;
console.log(x); // undefined
x = 5;
```

## 2. Function Hoisting
Function declarations are also hoisted to the top of their scope. 

For example:

```javascript
foo(); // "Hello, I'm foo!"

function foo() {
    console.log("Hello, I'm foo!");
}
```

This code behaves as if it were interpreted like this:
```javascript
function foo() {
    console.log("Hello, I'm foo!");
}

foo(); // "Hello, I'm foo!"
```

## 3. Function Expressions
Function expressions are not hoisted in the same way as function declarations. 
Only the variable declaration gets hoisted, not the function definition. 
For example:
```javascript
bar(); // TypeError: bar is not a function

var bar = function() {
    console.log("Hello, I'm bar!");
};
```
This code behaves as if it were interpreted like this:
```javascript
var bar;
bar(); // TypeError: bar is not a function

bar = function() {
    console.log("Hello, I'm bar!");
};

```

*Relying too much on hoisting attracts bugs*
