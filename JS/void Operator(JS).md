>The `void` operator evaluates the given expression and then returns [[undefined(JS)|undefined]].

This operator allows evaluating expressions that produce a value into places where an expression that evaluates to [[undefined(JS)|undefined]] is desired.

The `void` operator is often used merely to obtain the `undefined` primitive value, usually using `void(0)` (which is equivalent to `void 0`). In these cases, the global variable [`undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) can be used.

```js
const output = void 1;
console.log(output);
// Expected output: undefined

void console.log('expression evaluated');
// Expected output: "expression evaluated"

void (function iife() {
  console.log('iife is executed');
})();
// Expected output: "iife is executed"

void function test() {
  console.log('test function executed');
};
try {
  test();
} catch (e) {
  console.log('test function is not defined');
  // Expected output: "test function is not defined"
}

```