---
tag: Rs
---

**Constants** 
***
```Rust
const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
```

***Constants*** - are values that are bound to a name and are not allowed to change

*Constants:*
-  You aren’t allowed to use  `mut` with constants.
-  Constants can be declared in any scope, including the global scope, which makes them useful for values that many parts of code need to know about.


***Note:** Rust’s naming convention for constants is to use all uppercase with underscores between words.*



**Shadowing**
___
You can recreate a variable with the same name which also allows you to change it's type.

``` Rust
fn main() {
    let x = 5;

    let x = x + 1;

    {
        let x = x * 2;
        println!("The value of x in the inner scope is: {x}");
    }

    println!("The value of x is: {x}");
}
```
