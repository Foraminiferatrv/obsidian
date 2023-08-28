---
tag: JS
---
>Inheritance in JavaScript mechanism that allows objects "inherit" properties and methods of other objects (*their parent objects*) by accessing a [[Prototype(JS)|prototype]] (link) of those objects.

When it comes to **inheritance**, JavaScript only has one construct: [[Object(JS)|objects]].
Each object has a [[Private Properties(JS)|private]] property which holds a link to another object called its **[[Prototype(JS)|prototype]]**.

When trying to access a property of an object, the property will not only be sought (шукане(?)) on the object but on the **[[Prototype(JS)|prototype]]** of the object, the prototype of the prototype, and so on until either a property with a matching name is found or the end of the [[Prototype(JS)#Prototype Chain|prototype chain]] is reached.

