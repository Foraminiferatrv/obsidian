---
tag: JS
---

	A variable is a container for a value, like a number we might use in a sum, or a string that we might use as part of a sentence.

**JavaScript Variables can be declared in 4 ways:**
- Automatically
- Using `var` _(only for old browsers )
- Using `let` _(mutable variable)
- Using `const` 

## When to Use var, let, or const?

1. Always declare variables
2. Always use `const` if the value should not be changed
3. Always use `const` if the type should not be changed (Arrays and Objects)
4. Only use `let` if you can't use `const`
5. Only use `var` if you MUST support old browsers.


___
## JavaScript Identifiers

All JavaScript **variables** must be **identified** with **unique names**.

These unique names are called **identifiers**.

Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).


**The general rules for constructing names for variables (unique identifiers) are:**
- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter.
- Names can also begin with $ and _.
- Names are case sensitive (y and Y are different variables).
- Reserved words (like JavaScript keywords) cannot be used as names.

---
## One Statement, Many Variables

You can declare many variables in one statement.

Start the statement with `let` and separate the variables by **comma**:



```JS
let person = "John Doe", carName = "Volvo", price = 200;
```

___
## JavaScript Underscore (`_`)

Since JavaScript treats underscore as a letter, identifiers containing _ are valid variable names:

```js
let _lastName = "Johnson";  
let _x = 2;  
let _100 = 5;  
```

*Using the underscore is not very common in JavaScript, but a convention among professional programmers is to use it as an alias for "private (hidden)" variables.*
