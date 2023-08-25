---
tag: Rs
---

Every value in Rust is of a certain _data type_, which tells Rust what kind of data is being specified so it knows how to work with that data. 

**Types of... types:**
-  scalar
-  compound

	Rust is a _statically typed_ language, which means that it must know the types of all variables at compile time. The compiler can usually infer what type we want to use based on the value and how we use it. In cases when many types are possible, such as when convert a `String` to a numeric type using `parse`, we must add a type annotation, like this:

``` Rust
let guess: u32 = "42".parse().expect("Not a number!");
```


 ***
### **Scalar Types**
***
A **_scalar_** type represents a single value.

**Primary scalar types:**
- integers (1234)
- floating-point numbers (3.14)
- Booleans
- characters

### Integer Types
-----
An _integer_ is a number without a fractional component.

| Length  | Signed | Unsigned |
| ------- | ------ | -------- |
| 8-bit   | `i8`   | u8       |
| 16-bit  | `i16`  | u16      |
| 32-bit  | `i32`  | u32      |
| 64-bit  | `i64`  | u64      | 
| 128-bit | i128   | u128     |
| arch    | isize  | usize    |
 
 - Each variant can be either signed or unsigned and has an explicit size. 

 - **_Signed_** and **_unsigned_** refer to whether it’s possible for the number to be negative—in other words, whether the number needs to have a sign **(+-)** with it (signed) or whether it will only ever be positive and can therefore be represented without a sign (unsigned).

 - Each signed variant can store numbers from $-(2n - 1)$ to $2n - 1 - 1$ inclusive, where _n_ is the number of bits that variant uses. So an `i8` can store numbers from $-(27)$ to $27 - 1$, which equals -128 to 127. Unsigned variants can store numbers from 0 to 2n - 1, so a `u8` can store numbers from 0 to 28 - 1, which equals 0 to 255.

 
 **Integer Literals in Rust**

|Number literals|Example|
|---|---|
|Decimal|`98_222`|
|Hex|`0xff`|
|Octal|`0o77`|
|Binary|`0b1111_0000`|
|Byte (`u8` only)|`b'A'`|


