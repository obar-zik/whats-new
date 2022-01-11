# Node

## Features In node 16.x

### `Object.hasOwn` An Easier Way To Check Objects Properties (16.9.0)

The `Object.hasOwn` function is a static alias for `Object.prototype.hasOwnProperty.call`

### Error Can Now Tell You What cause it (16.9.0)

When You create a new error you can now add the cause option to tell that error cause it to fire, like so

```js
const firstError = new Error("ERROR!!!!!");

const secondError = new Error("ANOTHER ERROR!!!!", { cause: firstError });
```

This can be very helpful when you have an error that caches the error log them and them throw the error again.


```js

function alwaysFails() {
  throw new Error('😱')
}

function ErrorHandler() {
  try {
    alwaysFails()
  } catch (err) {
    console.error('JACK! ITS HAPPENED AGAIN!')
    throw new Error('You handel it', { cause: err })
  }
}

```

### The New `Array.prototype.at` Function

you can now use the newly `at` function.

this function allow you to select an object in an array.

the big advantage of using `at` instead if just selecting the with the normal bracket `[]` is that the `at` function can select items from the end!

#### example

```js
const arr = [1, 2, 3, 4, 5];

const firstItem = arr.at(0);
const lastItem = arr.at(-1);

console.log(`First Item: ${firstItem}`); // prints 1
console.log(`Last Item: ${lastItem}`); // prints 5
```

### The
