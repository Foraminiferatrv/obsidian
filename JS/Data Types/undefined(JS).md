>The undefined global property represents the primitive value undefined.

`undefined` is a [[Data Types (JS)#^472e0c|primitive]] value automatically assigned to variables that have just been declared, or to formal arguments for which there are no actual arguments.

Conceptually, `undefined` indicates the absence of a _value_, while `null` indicates the absence of an [[Object(JS)|object]]

`undefined` is a property of the [[Global objects (JS)|global object]]. That is, it is a variable in global scope.

A return statement with no value (return;) implicitly returns undefined.
Accessing a nonexistent object property (obj.iDontExist) returns undefined.
A variable declaration without initialization (let x;) implicitly initializes the variable to undefined.
Many methods, such as Array.prototype.find() and Map.prototype.get(), return undefined when no element is found.