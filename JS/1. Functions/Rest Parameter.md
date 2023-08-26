The **rest parameter** *(...)* syntax allows a function to accept an indefinite number of arguments as an array, providing a way to represent [variadic functions](https://en.wikipedia.org/wiki/Variadic_function) in JavaScript.

```Js
function sum(a, b,...theArgs) {
  let total = 0;
  for (const arg of theArgs) {
    total += arg;
  }
  return total;
}

console.log(sum(1, 2, 3));
// Expected output: 6

console.log(sum(1, 2, 3, 4));
// Expected output: 10

```
___
**! A function definition can only have one rest parameter, and the rest parameter must be the last parameter in the function definition.**
___

### The difference between rest parameters and the [[Functions (JS)#The arguments object|arguments]] object

There are three main differences between rest parameters and the [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments) object:

1. The `arguments` object is **not a real array**, while rest parameters are [[Array(JS)|Array]] instances, meaning methods like [`sort()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort), [`map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map), [`forEach()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) or [`pop()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop) can be applied on it directly.
2. The `arguments` object has the additional (deprecated) [`callee`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments/callee) property.
3. In a non-strict function with simple parameters, the `arguments` object [syncs its indices with the values of parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments#assigning_to_indices). The rest parameter array never updates its value when the named parameters are re-assigned.
- The rest parameter bundles all the _extra_ parameters into a single array, but does not contain any named argument defined _before_ the `...restParam`. The `arguments` object contains all of the parameters — including the parameters in the `...restParam` array — bundled into one array-like object.