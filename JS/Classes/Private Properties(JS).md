>Class fields are [[Public Properties(JS)|public]] by default, but **private class members** can be created by using a hash `#` prefix. The privacy encapsulation of these class features is enforced by JavaScript itself.

Private properties allow you to hide the internal workings of an object from the outside.

```js
class ClassWithPrivate {
  #privateField;
  #privateFieldWithInitializer = 42;

  #privateMethod() {
    // …
  }

  static #privateStaticField;
  static #privateStaticFieldWithInitializer = 42;

  static #privateStaticMethod() {
    // …
  }
}

```
