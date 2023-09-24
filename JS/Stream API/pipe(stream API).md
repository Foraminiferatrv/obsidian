---
tags:
  - JS
---
```js
readableSrc.pipe(writableDest)
```

In this simple line, we’re [[pipe|piping]] the output of a readable [[Stream API|stream]] — the source of data, as the input of a writable stream — the destination. The source has to be a readable stream and the destination has to be a writable one.

The `pipe` method returns the destination stream, which enabled us to do the chaining above. For streams `a` (readable), `b` and `c` (duplex), and `d` (writable), we can:

```js
a.pipe(b).pipe(c).pipe(d)

# Which is equivalent to:
a.pipe(b)
b.pipe(c)
c.pipe(d)

# Which, in Linux, is equivalent to:
$ a | b | c | d
```