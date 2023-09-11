---
tags:
  - JS
---
>✅Does not mutate an array

The **`find()`** method of [[Array(JS)|Array]] instances returns the first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, [[undefined(JS)|undefined]] is returned.

- If you need the **index** of the found element in the array, use [`findIndex()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex).
- If you need to find the **index of a value**, use [`indexOf()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf). (It's similar to [`findIndex()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex), but checks each element for equality with the value instead of using a testing function.)
- If you need to find if a value **exists** in an array, use [`includes()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes). Again, it checks each element for equality with the value instead of using a testing function.
- If you need to find if any element satisfies the provided testing function, use [`some()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some).