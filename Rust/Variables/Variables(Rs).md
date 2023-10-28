---
tag: Rs
---
> Rust allows to store variables in [[const(Rs)|constants]] and [[let(rs)|let]].

The main difference is that `let` can be [[Mutability(rs)|mutable]] by adding `mut` keyword in front of the name of a variable.

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
