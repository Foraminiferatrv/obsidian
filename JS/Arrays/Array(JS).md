> `Arrays` are basically single objects that contain multiple values stored in a list.

To add one or more items to the end of an array we can use [[push()]]. Note that you need to include one or more items that you want to add to the end of your array.

To remove the last item from the array, use [[pop()]].
To remove the first item from an array, use [[shift()]].
If you know the index of an item, you can remove it from the array using [[ splice()]].


| ⚠️ Mutable    | Immutable ✅     |
| ------------- | ---------------- |
| [[push()]]    | [[map()]]        |
| [[pop()]]     | [[filter()]]     |
| [[shift()]]   | [[concat()]]     |
| [[unshift()]] | [[slice()]]      |
| [[reverse()]] | [[toReversed()]] |
| [[sort()]]    | [[reduce()]]     |
| [[splice()]]  | [[find()]]       |
| [[fill()]]    |                  |

___
In JavaScript, arrays aren't [[Data Types (JS)#Primitive Types|primitives]] but are instead `Array` [[Object(JS)|objects]] with the following core characteristics:

- **JavaScript arrays are resizable** and **can contain a mix of different [[Data Types (JS)|data types]]. (When those characteristics are undesirable, use [[Typed arrays |typed arrays]] instead.)
- **JavaScript arrays are not associative arrays** and so, array elements cannot be accessed using arbitrary strings as indexes, but must be accessed using nonnegative integers (or their respective string form) as indexes.
- **JavaScript arrays are [zero-indexed](https://en.wikipedia.org/wiki/Zero-based_numbering)**: the first element of an array is at index `0`, the second is at index `1`, and so on — and the last element is at the value of the array's [`length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length) property minus `1`.
- **JavaScript [array-copy operations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#copy_an_array) create [shallow copies](https://developer.mozilla.org/en-US/docs/Glossary/Shallow_copy)**. (All standard built-in copy operations with _any_ JavaScript objects create shallow copies, rather than [deep copies](https://developer.mozilla.org/en-US/docs/Glossary/Deep_copy)).