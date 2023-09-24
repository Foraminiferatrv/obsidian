---
tags:
  - JS
---
>The Streams API allows  to programmatically access [[Data stream|streams of data]] received over the network and process them as desired by the developer.

```js
  const src = fs.createReadStream('./big.file');
```

[[Data stream|Streams]] are collections of data — just like [[Array(JS)|arrays]] or [[string (JS)]]. The difference is that streams might not be available all at once, and they don’t have to fit in memory. This makes streams really powerful when working with large amounts of data, or data that’s coming from an external source one _chunk_ at a time.

![[Pasted image 20230924114810.png]]

### Stream Types

There are four fundamental stream types in Node.js: Readable, Writable, Duplex, and Transform streams.

- A [[Readable Stream]] is an abstraction for a source from which data can be consumed. An example of that is the `fs.createReadStream` method.
- A [[Writable Stream|writable stream]] is an abstraction for a destination to which data can be written. An example of that is the `fs.createWriteStream` method.
- A [[Duplex Stream|duplex streams]] is both Readable and Writable. An example of that is a TCP socket.
- A [[Transform Stream|transform stream]] is basically a [[Duplex Stream|duplex stream]] that can be used to modify or transform the data as it is written and read. An example of that is the `zlib.createGzip` stream to compress the data using gzip. You can think of a transform stream as a function where the input is the writable stream part and the output is readable stream part. You might also hear transform streams referred to as “_through streams_.”

All streams are instances of `EventEmitter`. They emit events that can be used to read and write data. However, we can consume streams data in a simpler way using the [[pipe(stream API)|pipe]] method. 
The [[pipe(stream API)|pipe]] method is the easiest way to consume streams. It’s generally recommended to either use the `pipe` method or consume streams with events, but avoid mixing these two.

