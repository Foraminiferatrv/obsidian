---
tags:
  - JS
---
>Symbols are often used to add unique property keys to an object

>Behind the scenes `symbol` is like a *"long, unique number"* that always stays unique

>`Symbol('indentifier')` - parameters of the symbol constructor don't affect the value of a symbol. They are like keys that help identify different symbols. 

**`Symbol`** is a built-in [[Object(JS)|object]] whose [[Constructor|constructor]] returns a `symbol` [[Data Types (JS)#Primitive Types|primitive]] — also called a **Symbol value** or just a **Symbol** — that's guaranteed to be **unique**.

---
Basically `Symbol()` is only used as unique keys for objects.

```js 
let user = {
	id: 9451,
	name: 'Dominique',
	city: 'Siena',
	age: 59
}

const idSym = Symbol('id')
user[idSym] = 215485633215498732
```
___
To create a new primitive Symbol, you write `Symbol()` with an optional string as its description:

```JS
const sym1 = Symbol();
const sym2 = Symbol("foo");
const sym3 = Symbol("foo");
```

The following syntax with the [[The new Operator|new]] operator will throw a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError):

```js
const sym = new Symbol(); // TypeError
```

Because symbols are the only primitive data type that has reference identity (that is, you cannot create the same symbol twice), they behave like objects in some way. For example, they are garbage collectable and can therefore be stored in [[WeakMap]], [[WeakSet]], [[WeakRef]], and [`FinalizationRegistry`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/FinalizationRegistry) objects.

### [Shared Symbols in the global Symbol registry](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol#shared_symbols_in_the_global_symbol_registry)

The above syntax using the `Symbol()` function will create a Symbol whose value remains unique throughout the lifetime of the program. To create Symbols available across files and even across realms (each of which has its own global scope), use the methods [`Symbol.for()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/for) and [`Symbol.keyFor()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/keyFor) to set and retrieve Symbols from the global Symbol registry.