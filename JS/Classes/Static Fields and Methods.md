---
tag: JS
---
>Static properties are accessed by the [[Class(JS)|class]] itself. They cannot be directly accessed on instances of the class.

>Static fields and methods only exist in classes themselves but not in [[Object(JS)|objects]] created by them. 

Static methods are often utility functions, such as functions to create or clone objects, whereas static properties are useful for caches, fixed-configuration, or any other data you don't need to be replicated across instances.