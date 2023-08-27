---
tag: JS
---

> **TDZ** - is a block of code in which  the variable(`const`, `let`,  and `class`) has not been initialized with a value.

A variable declared with `let`, `const`, or `class` is said to be in a "temporal dead zone" (TDZ) from the start of the block until code execution reaches the line where the variable is declared and initialized.

While inside the TDZ, the variable has not been initialized with a value, and any attempt to access it will result in a [`ReferenceError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError). The variable is initialized with a value when execution reaches the line of code where it was declared. If no initial value was specified with the variable declaration, it will be initialized with a value of `undefined`.

This differs from `var` variables, which will return a value of `undefined` if they are accessed before they are declared. The code below demonstrates the different result when `let` and `var` are accessed in code before the line in which they are declared.