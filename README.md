# Hoisting
Breakdown For JavaScript Hoisting

Hoisting is a JavaScript mechanism where variables and function declarations are **moved to the top of their containing scope** during the compile phase **before** the code is executed. 
This means that regardless of where variables and functions are declared within a scope, they are moved to the top of that scope by the JavaScript engine.

```
console.log(x); // undefined
var x = 5;
```

**NB:** Only the declarations are hoisted, not the initializations. 
