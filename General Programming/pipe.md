---
tags:
  - JS
  - CS
---
>`pipe` is a function, that calls other functions on the same value in order.

>The concept of `pipe` is simple — it combines `n` functions. It’s a pipe flowing left-to-right, calling each function with the output of the last one.

```js
pipe = (...fns) => (x) => fns.reduce((v, f) => f(v), x);
```

```js
pipe(
  getName,
  uppercase,
  get6Characters,
  reverse
)({ name: 'Buckethead' });
// 'TEKCUB'
```

