Function bodies are made up of a series of [[Statements]] statements optionally ending in an [[Expressions]] expression.

- #Statements are instructions that perform some action and do not return a value.
- #Expressions evaluate to a resultant value. Let’s look at some examples.

## Statement
___
Statement - is a one "instruction".
``` Rust
fn main() {
    let y = 6;
}
```

## Expression
___
Expressions can be part of statements: in Listing 3-1, the `6` in the statement `let y = 6;` is an expression that evaluates to the value `6`. Calling a function is an expression. Calling a macro is an expression. A new scope block created with curly brackets is an expression, for example:

```rust
fn main() {
    let y = {
        let x = 3;
        x + 1
    };

    println!("The value of y is: {y}");
}
```

This expression:

``` rust
{ 
	let x = 3;    
	x + 1 
}
```
