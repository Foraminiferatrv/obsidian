---
tags:
  - JS
---
>**`Number`** values represent floating-point numbers like `37` or `-9.25`.

```js
255; // two-hundred and fifty-five
255.0; // same number
255 === 255.0; // true
255 === 0xff; // true (hexadecimal notation)
255 === 0b11111111; // true (binary notation)
255 === 0.255e3; // true (decimal exponential notation)
```

When used as a function, `Number(value)` converts a string or other value to the Number type. If the value can't be converted, it returns [`NaN`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NaN).