---
tag: JS
---

>The `extends` keyword is used to create a [[Class(JS)|class]] that is a child of another class. 

```Js
class DateFormatter extends Date {
  getFormattedDate() {
    const months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'];
    return `${this.getDate()}-${months[this.getMonth()]}-${this.getFullYear()}`;
  }
}
```

## extends Under the Hood

We can set the [[Prototype(JS)|Prototype]] of `Constructor.prototype` via the `Object.setPrototypeOf()` function.
>This is an equivalent to using `extends` keyword in classes.

```js
function Base() {}
function Derived() {}
// Set the `[[Prototype]]` of `Derived.prototype`
// to `Base.prototype`
Object.setPrototypeOf(Derived.prototype, Base.prototype);

const obj = new Derived();
// obj ---> Derived.prototype ---> Base.prototype ---> Object.prototype ---> null
```