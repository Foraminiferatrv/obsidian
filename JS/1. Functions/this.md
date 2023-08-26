In most cases, the value of `this` is determined by how a function is called (runtime [[Terms#Binding|binding]]). It can't be set by assignment during execution, and it may be different each time the function is called. 

The `bind()`  method can set the value of a function's this regardless of how it's called, and arrow functions don't provide their own this binding (it retains the this value of the enclosing lexical context).

## Function.prototype.bind()

The **`bind()`** method of [`Function`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function) instances creates a new function that, when called, calls this function with its `this` keyword set to the provided value, and a given sequence of arguments preceding any provided when the new function is called.