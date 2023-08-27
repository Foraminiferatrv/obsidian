---
tag: JS
---
>I**N SHORT:** Prototype is a reference to object's parent object...

>**Prototype** is a mechanism that allow objects to [[Inheritance(JS)|inherit]] properties from on another.

So the object's prototype is the object that an object descends or inherits from.

### `[[Prototype]]`

>Built in every `object` hidden private property (which is an object itself) that holds a [[Reference|reference]] to this object's **prototype**.

![[Pasted image 20230827133843.png]]

### Prototype Chain

>Sequence of built-in `Prototype` objects each linked to a `Prototype` of a "parent" object.

Every object in JavaScript has a built-in property, which is called its **[[#` Prototype `|prototype]]**. The prototype is itself an [[Object(JS)|object]], so the prototype will have its own prototype, making what's called a **prototype chain**. The chain ends when we reach a prototype that has `null` for its own prototype.

You can access object's prototype with: `Object.getPrototypeOf()`

![[Pasted image 20230827133134.png]]

### `__proto__`

(A.K.A: the Dunder Proto or [Double Underscore Prototype](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto))*

>`__proto__ `s a property of `Object.prototype` that exposes the hidden `[[Prototype]]` property of an object and allows you to access or modify it. You should not use it as it is [**deprecated**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto), although you may come across it in older code.

### `Object.create()`

>**!LEGACY CODE!**

[`Object.create()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create) can be used to build the [[Prototype(JS)#Prototype Chain|inheritance chain]]. However, because this reassigns the `prototype` property and removes the [[Constructor|constructor]] property, it can be more error-prone, while performance gains may not be apparent if the constructors haven't created any instances yet.
___
## Behind The Scenes
