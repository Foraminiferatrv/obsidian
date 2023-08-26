---
tag: JS
---

[Source: MDN]( https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)

>In short: Objects are variables that can contain many values.

An **object** is a collection of related data and/or functionality. These usually consist of several variables and functions (which are called ***properties*** and ***methods*** when they are inside objects). 

The value of an object member can be pretty much anything.

When the object's members are functions there's a simpler syntax. Instead of `bio: function ()` we can write `bio()`.

``` js
const objectName = {
  objectField: objectProperty,
  objectMethod: ()=>{},
  objectMethod2() {
		//Do Smth  
	},
  member3Name: member3Value,
};
```

An object like this is referred to as an **object [[Literal|literal]]** — we've literally written out the object contents as we've come to create it. This is different compared to objects instantiated from [[Class|classes]].

Properties of an object can be accessed using **dot notation** or bracket notation `person["age"]`.


The **`Object`** type represents one of [[Data Structures (JS)|data structures]]. It is used to store various keyed collections and more complex entities. Objects can be created using the [`Object()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/Object) constructor or the [object initializer / literal syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer).

___
### "this" keyword
The `this` keyword refers to the current object the code is being written inside.

_____


[[The "new" Operator|new]]