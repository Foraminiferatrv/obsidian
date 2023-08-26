---
tag: JS
---
>A JavaScript function is a block of code designed to perform a particular task.
____
> In JavaScript  ==**functions are objects(!)**==. Functions are inside the **[[Data Types (JS)#^bc81c3|non-primitive]]** category, which means that when you define a function you are creating an object. 
> Functions are not just objects, they are **[[Built-in Objects|Function]]** objects
____
>A JavaScript function is executed when "something" invokes it (calls it).

Functions are [[First-class Functions|first-class objects]] in JS, because they can be passed to other functions, returned from functions, and assigned to variables and properties. They can also have properties and methods just like any other object. What distinguishes them from other objects is that functions can be called.

Arguments are always [_passed by value_](https://en.wikipedia.org/wiki/Evaluation_strategy#Call_by_reference) and never _passed by reference_. This means that if a function reassigns a parameter, the value won't change outside the function. More precisely, object arguments are [_passed by sharing_](https://en.wikipedia.org/wiki/Evaluation_strategy#Call_by_sharing), which means if the object's properties are mutated, the change will impact the outside of the function. For example: 

```JS
function updateBrand(obj) {
  // Mutating the object is visible outside the function
  obj.brand = "Toyota";
  // Try to reassign the parameter, but this won't affect
  // the variable's value outside the function
  obj = null;
}

const car = {
  brand: "Honda",
  model: "Accord",
  year: 1998,
};

console.log(car.brand); // Honda

// Pass object reference to the function
updateBrand(car);

// updateBrand mutates car
console.log(car.brand); // Toyota
```

The [[this]] keyword refers to the object that the function is accessed on — it does not refer to the currently executing function, so you must refer to the function value by name, even within the function body.

___
### [Defining functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions#defining_functions)

Broadly speaking, JavaScript has four kinds of functions:

- Regular function: can return anything; always runs to completion after invocation
- Generator function: returns a [[Generator]] object; can be paused and resumed with the [`yield`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/yield) operator
- Async function: returns a [[Promises|`Promise`]]; can be paused and resumed with the [`await`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await) operator
- Async generator function: returns an [`AsyncGenerator`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/AsyncGenerator) object; both the `await` and `yield` operators can be used

For every kind of function, there are three ways to define it:
- Declaration
[`function`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function), [`function*`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*), [`async function`](Async functions.md), [`async function*`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function*)
``` JS
// Declaration
function multiply(x, y) {
  return x * y;
} // No need for semicolon here
```

- [[Expressions|Expression]]
[`function`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function), [`function*`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function*), [`async function`](Async functions.md), [`async function*`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/async_function*)
``` JS
// Expression; the function is anonymous but assigned to a variable
const multiply = function (x, y) {
  return x * y;
  
// Expression; the function has its own name
const multiply = function funcName(x, y) {
  return x * y;
};
};```

- Constructor
[`Function()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/Function), [`GeneratorFunction()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/GeneratorFunction/GeneratorFunction), [`AsyncFunction()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/AsyncFunction/AsyncFunction), [`AsyncGeneratorFunction()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/AsyncGeneratorFunction/AsyncGeneratorFunction)
``` JS
// Constructor
const multiply = new Function("x", "y", "return x * y");
```

In addition, there are special syntaxes for defining [[Arrow functions| arrow functions]] and [methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions), which provide more precise semantics for their usage. [[Class|Classes]] are conceptually not functions (because they throw an error when called without `new`), but they also inherit from `Function.prototype` and have `typeof MyClass === "function"`.

```JS
// Arrow function
const multiply = (x, y) => x * y;

// Method
const obj = {
  multiply(x, y) {
    return x * y;
  },
};

```

### #Syntaxis_differences
All syntaxes do approximately the same thing, but there are some subtle behavior differences.
- The `Function()` [[Constructor|constructor]], `function` expression, and `function` declaration syntaxes create ==full-fledged **function [[Object(JS)|objects]]**(!),== which can be constructed with [[The new Operator|new]]. However, [[Arrow functions|arrow functions]] and methods cannot be constructed. [[Async functions|Async functions]], generator functions, and async generator functions are not constructible regardless of syntax.
- The `function` declaration creates functions that are [[Function hoisting|hoisted]]. Other syntaxes ***do not hoist*** the function and the function value is only visible after the definition.
- The arrow function and `Function()` constructor always create _anonymous_ functions, which means they can't easily call themselves [[Recursion|recursively]]. One way to call an arrow function recursively is by assigning it to a variable.
- The arrow function `()=>{}` syntax does not have access to `arguments` or [[this]].
- The `Function()` constructor cannot access any local variables — it only has access to the global [[Scope (JS)|scope]].
- The `Function()` constructor causes runtime compilation and is often slower than other syntaxes.

For `function` expressions, there is a distinction between the function name and the variable the function is assigned to. **The function name cannot be changed, while the variable the function is assigned to can be reassigned.*** The function name can be different from the variable the function is assigned to — they have no relation to each other. The function name can be used only within the function's body.
___
### Function parameters

Each function parameter is a simple identifier that you can access in the local scope.

```js
function myFunc(a, b, c) {
  // You can access the values of a, b, and c here
}
```

There are three special parameter syntaxes:

- [_Default parameters_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters) `function (a, b = 30){}` allow formal parameters to be initialized with default values if no value or `undefined` is passed.
- The [[Rest Parameter|rest parameter]]  `function (...otherParams){}` allows representing an indefinite number of arguments as an array.
- [_Destructuring_](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) `function ({a, b}){}` allows unpacking elements from arrays, or properties from objects, into distinct variables.
___
### The arguments object
You can refer to a function's arguments within the function by using the arguments object.

`arguments`
An array-like object containing the arguments passed to the currently executing function.

`arguments.callee`
The currently executing function.

`arguments.length`
The number of arguments passed to the function.

___
### [[Getters & Setters|Getter and setter functions]]

You can define accessor properties on any standard built-in object or user-defined object that supports the addition of new properties. Within object literals and classes, you can use special syntaxes to define the getter and setter of an accessor property.

`get`
Binds an object property to a function that will be called when that property is looked up.

`set`
Binds an object property to a function to be called when there is an attempt to set that property.

Note that these syntaxes create an object property, not a method. The getter and setter functions themselves can only be accessed using reflective APIs such as `Object.getOwnPropertyDescriptor().`