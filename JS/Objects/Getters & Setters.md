---
tag: JS
---
>JavaScript **getters** and **setters** are special methods that provide access to [[Object(JS)|object]] properties. Getters are used to read values of properties, while setters are used to write values to properties.

#### Why use it?
- Getters and setters allow you to control how your object properties are accessed and modified.
- **Getters and setters can be used to validate data before it is set to an object.**
- Getters and setters can be used to create properties that are calculated on the fly.
## Getter

>Getters are often used to access values from an object that are not directly accessible, such as nested properties.

Getters are [[Functions (JS)|functions]] that are used to access properties on an [[Object(JS)|object]]. They are similar to methods, but they are not called on an instance of an object. Instead, they are called on the object itself. 

Getters are very useful for retrieving complex data from an object, and for creating computed properties.

Getters are defined using the `get` keyword, followed by a [[Functions (JS)|function]]. This function takes *no arguments* and returns a value. The value returned can be any valid JavaScript value, including objects and arrays.

```javascript
let person = {
  name: 'John',
  get personsName() {
    return this.name;
  }
};

const theName = person.personsName //'John'
```

## Setter

>The setter is a method that allows you to set the value of a property in an object.

It is a special type of method that is used to set the value of a property in an [[Object(JS)|object]]. The setter method takes one argument, which is the value that you want to set the property to. The setter method is defined with the keyword "set".

```javascript
const user = {
  name: '',
  set name(value) {
    this.name = value;
  },
};

user.name = 'John';
console.log(user.name); // John
```

The setter method is a great way to ensure that the value of a property is always set correctly. For example, if we want to make sure that the value of the "name" property is always a string, we can use a setter method to check the type of the value and throw an error if it is not a string.