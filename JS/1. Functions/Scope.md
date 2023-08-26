---
tag: JS
---

The scope is a current context of execution in which all variables and expressions are "visible" or can be [[Reference|referenced]].  

If the variable or expression is out of the scope, it will not be available to use.
Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.


JavaScript has the following kinds of scopes:

- **Global scope:** The default scope for all code running in script mode.
- **Module scope**: The scope for code running in [[Modules|module]] mode.
- **Function scope**: The scope created with a [[Functions (JS)|function]].

In addition, variables declared with [[Variables (JS)|let]] or [[Variables (JS)|const]] can belong to an additional scope:

- Block scope: The scope created with a pair of curly braces (a [block](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/block)).


A [[Functions (JS)|function]] creates a scope, so that (for example) a variable defined exclusively within the function cannot be accessed from outside the function or within other functions. For instance, the following is invalid:

``` js
function exampleFunction() {
  const x = "declared inside function"; // x can only be used in exampleFunction
  console.log("Inside function");
  console.log(x);
}

console.log(x); // Causes error
```


Blocks only scope `let` and `const` declarations, but not [[Variables (JS)|var]] declarations.


```js
{
  var x = 1;
}
console.log(x); // 1
```


``` js
{
  const x = 1;
}
console.log(x); // ReferenceError: x is not defined
```