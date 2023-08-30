>The undefined global property represents the primitive value undefined.

`undefined` is a [[Data Types (JS)#^472e0c|primitive]] value automatically assigned to variables that have just been declared, or to formal arguments for which there are no actual arguments.

Conceptually, `undefined` indicates the absence of a _value_, while `null` indicates the absence of an [[Object(JS)|object]]

`undefined` is a property of the [[Global objects (JS)|global object]]. That is, it is a variable in global scope.

- A [`return`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/return) statement with no value (`return;`) implicitly returns `undefined`.
- Accessing a nonexistent [[Object(JS)|object]] property (`obj.iDontExist`) returns `undefined`.
- A variable declaration without initialization (`let x;`) implicitly initializes the variable to `undefined`.
- Many methods, such as [`Array.prototype.find()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find) and [`Map.prototype.get()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map/get), return `undefined` when no element is found.

`null` is used much less often in the core language. The most important place is the end of the [prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain) — subsequently, methods that interact with prototypes, such as [`Object.getPrototypeOf()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/getPrototypeOf), [`Object.create()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create), etc., accept or return `null` instead of `undefined`.

`null` is a **keyword**, but `undefined` is a normal **identifier** that happens to be a global property. In practice, the difference is minor, since `undefined` should not be redefined or [[Shadowing|shadowed]].