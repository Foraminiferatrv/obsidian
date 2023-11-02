---
tags:
  - rust
---
>	`'static'` - is a [[Lifetimes|lifetime]] indicates that the data pointed to by the reference lives for the entire lifetime of the running program. 

There are two ways to make a variable with `'static` lifetime, and both are stored in the read-only memory of the binary:

- Make a constant with the `static` declaration.
- Make a `string` literal which has type: `&'static str`.