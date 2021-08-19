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

  **Type Inference:** TS tries to figure out what type of value a variable refers to. This works if we declare (`const variable`) and the initialization(` = 'string'`) on the same step

  * try to avoid the `any` type at all costs. it means TS does not know the type and cannot perform any type checking on this variable.

  **Type Annotations: (For Functions)** Code that we write to tell TS what type of arguments a function will receive and what is its return value type.

  **Type Inference: (For Functions)** TS tries to figure out what type of value a function will return.

  * type `never` is used when we are 100% sure that we will not return anything from a function, like a function that is only throwing an error.

  * When we use the `|` to indicate a type like this `arg: typeOne | typeTwo` arg will only have access to common properties on both types.

  * union-ing two types like the note above is always associated with a Type-Guard approach in the code (when you check for the variable type using typeof and instanceof to act accordingly), this pattern is not good as it means every time we want to hadle a new type, we will add it to the union `typeOne | typeTwo | ...` and then in the code add a new `if(var instanceof typeThree)` with the handling for that type inside the if statement.

  * When working with node.js, TS might complain about a native module not found, this actually might be baecause `@types/node` library is not installed. Which is a type definitions for Node Standard Library.

### Tuple:

  * It is like an array but the order of the elements is important, and it basically represents properties about a record.
  * In TS we can define a tuple like this: `const variable: [boolean, number] = [true, 100]`.
  * Most of the time tuples are not the best type to represent data types.

### Interfaces:

  * The main usage of interfaces is to create a new type and define the property name and value types of an object.
  * TS will iterate through an object and make sure it has all the properties that are in the interface.
