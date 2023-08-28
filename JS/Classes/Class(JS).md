> Classes are a template for creating objects.

>Classes are **[[Functions (JS)|functions]]**. Because they are used to build [[Object(JS)|objects]].

Classes in JS are built on [[Prototype(JS)|prototypes]] but also have some syntax and semantics that are unique to classes.

Classes are in fact "special [[Functions (JS)|functions]]", and just as you can define [function expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function) and [function declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function), a class can be defined in two ways: a [class expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/class) or a [class declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/class).

```js
//Class Declaration
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

	getHight(){
  	console.log(this.height)
  }

	static setArea(){
		this.area = this.height * this.width
	}
}

const rect = new Rectangle(2, 25)

//Class Expression; the class is anonymous but assigned to a variable
const Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
```

>Classes are not [[Hoisting|hoisted]] and just like `let` and `const` have a [[Temporal dead zone (TDZ)]].  

**A class element can be characterized by three aspects:**

- *Kind*: [[Getters & Setters|Getter]], [[Getters & Setters|setter]], method, or field
- *Location*: [[Static Fields and Methods|Static]] or instance
- *Visibility*: [[Private and Public Properties(JS)|Public or private]] 