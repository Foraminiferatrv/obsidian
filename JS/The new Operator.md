
>`new` [[Operators (JS)|operator]]  is an operator that creates a new instance *(екземпляр)* of a object

The **`new`** operator lets developers create an instance of a user-defined object type or of one of the built-in object types that has a [[Constructor|constructor]] function.

When a function is called with the **`new`** keyword, the function will be used as a [[Constructor|constructor]]. `new` will do the following things:

1. Creates a blank, plain JavaScript [[Object(JS)|object]]. For convenience, let's call it `newInstance`.
2. Points `newInstance`'s [[Prototype]] to the constructor function's `prototype` property, if the `prototype` is an [[Object(JS)|Object]]. Otherwise, `newInstance` stays as a plain object with `Object.prototype` as its [[Prototype]].
3.  Executes the constructor function with the given arguments, binding `newInstance` as the [[this]] context (i.e. all references to `this` in the constructor function now refer to `newInstance`).
4. If the constructor function returns a [[Data Types (JS)#^bc81c3|non-primitive]], this return value becomes the result of the whole `new` expression. Otherwise, if the constructor function doesn't return anything or returns a [[Data Types (JS)#^472e0c|primitive]], `newInstance` is returned instead. (Normally constructors don't return a value, but they can choose to do so to override the normal object creation process.)

>[[Class|Classes]] can only be instantiated with the `new` operator — attempting to call a class without `new` will throw a `TypeError`.