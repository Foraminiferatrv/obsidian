---
tags:
  - JS
---
> A duplex streams is both [[Readable Stream|Readable]] and [[Writable Stream|Writable]]. An example of that is a [[TCP]] [[Web Sockets|socket]].

```javascript
mport stream from 'stream';

const duplex = new stream.Duplex({
  write: (chunk, encoding, next) {
    // Do something with the chunk and then call next() to indicate 
    // that the chunk has been processed. The write() fn will handle
    // data piped into this duplex stream. After the write() has
    // finished, the data will be processed by the read() below.
    next();
  },
  read: ( size ) {
    // Add new data to be read by streams piped from this duplex
    this.push( "some data" )
  }
})
```

