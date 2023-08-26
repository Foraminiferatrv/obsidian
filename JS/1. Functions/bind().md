---
tag: JS
---
## `Function.prototype.bind()`

==With the `bind()` method, an object can borrow a method from another object.==

>The **`bind()`** method of [[Functions (JS)|Function]] instances creates a new function that, when called, calls this function with its `this` keyword set to the provided value, and a given sequence of arguments preceding any provided when the new function is called.

```JS
const person = {  
  firstName:"John",  
  lastName: "Doe",  
  fullName: function () {  
    return this.firstName + " " + this.lastName;  
  }  
}  
  
const member = {  
  firstName:"Hege",  
  lastName: "Nilsen",  
}  
  
let fullName = person.fullName.bind(member);
```

#### Sometimes the `bind()` method has to be used to prevent losing **this**.
 
*Example:*

```JS
const person = {  
  firstName:"John",  
  lastName: "Doe",  
  display: function () {  
    let x = document.getElementById("demo");  
    x.innerHTML = this.firstName + " " + this.lastName;  
  }  
}  
  
person.display();
```

When a function is used as a callback, **`this`** is lost.

This example will try to display the person name after 3 seconds, but it will display **`undefined`** instead:

*Example:*

```js
const person = {  
  firstName:"John",  
  lastName: "Doe",  
  display: function () {  
    let x = document.getElementById("demo");  
    x.innerHTML = this.firstName + " " + this.lastName;  
  }  
}  
  
setTimeout(person.display, 3000);
```

The `bind()` method solves this problem.

In the following example, the `bind()` method is used to bind `person.display` to person.

This example will display the person name after 3 seconds:

*Example:*

```js
const person = {  
  firstName:"John",  
  lastName: "Doe",  
  display: function () {  
    let x = document.getElementById("demo");  
    x.innerHTML = this.firstName + " " + this.lastName;  
  }  
}  
  
let display = person.display.bind(person);  
setTimeout(display, 3000);
```