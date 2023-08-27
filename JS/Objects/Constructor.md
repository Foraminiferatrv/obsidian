>The **`constructor`** method is a special method of a [[Class(JS)|class]] for creating and initializing an object instance of that class.

>Constructors are functions called with [[The new Operator|new]].

```js
class Polygon {
  constructor() {
    this.name = 'Polygon';
  },
  method(){}
}
```
A constructor is just a function ==**called using the [[The new Operator|new]] keyword**==. When you call a constructor, it will:
- create a new [[Object(JS)|object]]
- [[Binding|bind]] `this` to the new object, so you can refer to `this` in your constructor code
- run the code in the constructor
- return the new object.

Constructors, by convention, start with a capital letter and are named for the type of object they create. 

---
The first version of the `constructor` is just a function and it can be used to create [[Object(JS)|objects]] with the `new` operator:

```js
function Person(name) {
  this.name = name;
  this.introduceSelf = function () {
    console.log(`Hi! I'm ${this.name}.`);
  };

const frank = new Person('Frank');

frank.name;
frank.introduceSelf();
//"Hi! I'm Frank."
```



