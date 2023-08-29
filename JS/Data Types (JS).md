---
tag: JS
---

Types in JavaScript are categorized by:
- **Primitives ([[string (JS)|string]], [[number (JS)|number]], [[null(JS)|null]], [[boolean(JS)|boolean]], [[undefined(JS)|undefined]], [[symbol(JS)|symbol]])**: these are immutable data types. They are not objects, don't have methods and they are stored in memory by value. ^472e0c
- **Non-Primitives ([[Functions (JS)|functions]], [[Array(JS)|arrays]] and [[Object(JS)|objects]])**: these are mutable data types. They are objects and they are stored in [[Memory(JS)|memory]] by reference. ^bc81c3

>`function` = Object
>`array` = Object
>`object` = Object

All primitive types, except [[null(JS)|null]] and [[undefined(JS)|undefined]], have their corresponding object wrapper types, which provide useful methods for working with the primitive values.

When a property is accessed on a primitive value, JavaScript automatically wraps the value into the corresponding wrapper object and accesses the property on the object instead. However, accessing a property on `null` or `undefined` throws a `TypeError` exception, which necessitates the introduction of the [[Optional Chaining Operator|optional chaining]] operator.

| Type                                                                                                | `typeof` return value | Object wrapper                                                                                        |
| --------------------------------------------------------------------------------------------------- | --------------------- | ----------------------------------------------------------------------------------------------------- |
| [Null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#null_type)           | `"object"`            | N/A                                                                                                   |
| [Undefined](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#undefined_type) | `"undefined"`         | N/A                                                                                                   |
| [Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#boolean_type)     | `"boolean"`           | [`Boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#number_type)       | `"number"`            | [`Number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)   |
| [BigInt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#bigint_type)       | `"bigint"`            | [`BigInt`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)   |
| [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#string_type)       | `"string"`            | [`String`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)   |
| [Symbol](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#symbol_type)       | `"symbol"`            | [`Symbol`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)   |

