
>An **arrow function expression** is a compact alternative to a traditional [[Functions (JS)|function]] [[Expression|expression]], with some semantic differences and deliberate limitations in usage:



- Arrow functions don't have a [[Prototype(JS)|prototype property]]
- Arrow functions don't have their own [bindings](https://developer.mozilla.org/en-US/docs/Glossary/Binding) to [[this]], [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments), or [[super Operator|super]], and should not be used as [methods](https://developer.mozilla.org/en-US/docs/Glossary/Method).
- Arrow functions cannot be used as [[Constructor|constructors]]. Calling them with [[The new Operator|new]] throws a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError). They also don't have access to the [`new.target`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new.target) keyword.
- Arrow functions cannot use [`yield`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/yield) within their body and cannot be created as generator functions.
>Arrow functions are also [[First-class Functions|first-class]] [[Object(JS)|objects]] but they are more "lightweight" but lack the ability to be fully customized like regular functions due to their lack of individual properties and methods.

Arrow functions are always unnamed. If the arrow function needs to call itself, use a named function [[Expression|expression]] instead. You can also assign the arrow function to a variable so it has a name.

### Cannot be used as methods

Arrow function expressions should only be used for non-method functions because they do not have their own [[this]]. Let's see what happens when we try to use them as methods:

>Arrow functions establish [[this]] based on the scope the arrow function is defined within,