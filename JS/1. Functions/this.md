>In JavaScript, the `this` keyword refers to the current [[Object|object]] the code is being written inside

>`this` keyword is extremely useful when using [[Constructor|constructors]] to create more than one object from a single object definition, and that's the subject of the next section.


**Which** object depends on how `this` is being invoked (used or called).


The `this` keyword refers to different objects depending on how it is used:
- In an object method, `this` refers to the **object**.
- Alone, `this` refers to the **global object**.
- In a function, `this` refers to the **[[Global objects (JS)|global object]]**.
- In a function, in [[strict mode]], `this` is `undefined`.
- In an [[Events|event]], `this` refers to the **element** that received the event.
- Methods like `call()`, `apply()`, and `bind()` can refer `this` to **any object**.

In most cases, the value of `this` is determined by how a function is called (runtime [[Binding|binding]]). It can't be set by assignment during execution, and it may be different each time the function is called. 

The [[bind()]]  method can set the value of a function's this regardless of how it's called, and arrow functions don't provide their own this binding (it retains the this value of the enclosing lexical context).
