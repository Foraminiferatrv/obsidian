
>An **arrow function expression** is a compact alternative to a traditional [[Functions (JS)|function]] [[Expression|expression]], with some semantic differences and deliberate limitations in usage:

- Arrow functions don't have a [[Prototype(JS)|prototype property]]
- Arrow functions don't have their own [bindings](https://developer.mozilla.org/en-US/docs/Glossary/Binding) to [[this]], [`arguments`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments), or [[super Operator|super]], and should not be used as [methods](https://developer.mozilla.org/en-US/docs/Glossary/Method).
- Arrow functions cannot be used as [[Constructor|constructors]]. Calling them with [[The new Operator|new]] throws a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError). They also don't have access to the [`new.target`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new.target) keyword.
- Arrow functions cannot use [`yield`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/yield) within their body and cannot be created as generator functions.