---
tag: JS
---
>**Prototype** is a mechanism that allow objects to [[Inheritance(JS)|inherit]] properties from on another.

### `[[Prototype]]`

>Built in every `object` hidden private property (which is an object itself) that holds a [[Reference|reference]] to this object's prototype.



### Prototype Chain

>Sequence of built-in `Prototype` objects each linked to a `Prototype` of a "parent" object.

Every object in JavaScript has a built-in property, which is called its **[[#` Prototype `|prototype]]**. The prototype is itself an [[Object(JS)|object]], so the prototype will have its own prototype, making what's called a **prototype chain**. The chain ends when we reach a prototype that has `null` for its own prototype.

You can access object's prototype with: `Object.getPrototypeOf()`

![[Pasted image 20230827133134.png]]

