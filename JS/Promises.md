---
tags:
  - JS
---
>The **`Promise`** [[Object(JS)|object]] represents the eventual completion (or failure) of an asynchronous operation and its resulting value.

A `Promise` is an object representing the eventual completion or failure of an asynchronous operation.
Essentially, a promise is a returned object to which you attach callbacks, instead of passing callbacks into a function.

A `Promise` is in one of these states:

- 🟡 _pending_: initial state, neither fulfilled nor rejected.
- 🟢 _fulfilled_: meaning that the operation was completed successfully.
- 🔴 _rejected_: meaning that the operation failed.
___
The `Promise` class offers four static methods to facilitate async task concurrency:

[`Promise.all()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all)

Fulfills when **all** of the promises fulfill; rejects when **any** of the promises rejects.

[`Promise.allSettled()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/allSettled)

Fulfills when **all** promises settle.

[`Promise.any()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/any)

Fulfills when **any** of the promises fulfills; rejects when **all** of the promises reject.

[`Promise.race()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/race)

Settles when **any** of the promises settles. In other words, fulfills when any of the promises fulfills; rejects when any of the promises rejects.