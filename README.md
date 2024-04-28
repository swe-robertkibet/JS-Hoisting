# Hoisting

Hoisting is a JavaScript mechanism where variables and function declarations are **moved to the top of their containing scope** during the compile phase **before** the code is executed. 
This means that regardless of where variables and functions are declared within a scope, they are moved to the top of that scope by the JavaScript engine.


**NB:** Only the declarations are hoisted, not the initializations. 


## Variable Hoisting

When you declare a variable using var, let, or const, the declaration is hoisted to the top of its scope. 
However, the initialization remains in place. For example:
```
console.log(x); // undefined
var x = 5;
```
This code behaves as if it were interpreted like this:
```
var x;
console.log(x); // undefined
x = 5;
```

