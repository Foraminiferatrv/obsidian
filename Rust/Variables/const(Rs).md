---
tags:
  - Rs
---
> `const` - _constants_ are values that are bound to a name and are not allowed to change.

```rust
const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
```

>

1. [[Mutability(rs)|mut]] can't be used with `const`
2.  The [[Types(rs)|type]] of the value _must_ be annotated
3. **Constants** can be declared in any scope, including the global scope, *which makes them useful for values that many parts of code need to know about.*
4. **Constants** may be set only to a constant [[Expression|expression]], not the result of a value that could only be computed at runtime.
5. **Constants** are valid for the entire time a program runs, within the scope in which they were declared.