## Syntax and features:

  * In this section, TS's syntax and features will be explained.
  * Definition and a quick overview will be given, examples, why do we care, and when to use such features.

### Type:

  * A Type is an easy way for us to refer to all properties and functions a value has.
  * Ts has two main categories of types:
    1. Primitive types: string, number, boolean, null, undefined, symbol, void.
    2. Object types : functions, objects, arrays, classes. - Any type we create or that comes built in TS.

  * TS compiler uses these types to analyze out code and catch errors during development.
  * Also TS types help other engineers reading the code to understand what values are flowing around in our App.
  * Types are/should be used every where in our App.

  **Type Annotations:** Code that we write to tell TS what type of value a variable has.

  **Type Inference:** TS tries to figure out out what type of value a variable refers to. This works if we declare (`const variable`) and the initialization(` = 'string'`) on the same step
