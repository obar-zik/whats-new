# Node 16.13.1

### New `Array.prototype.at` function

you can now use the newly `at` function.

this function allow you to select an object in an array.

the big advantage of using `at` instead if just selecting the with the normal bracket `[]` is that the `at` function can select items from the end!

#### example

```js
const arr = [1, 2, 3, 4, 5];

const firstItem = arr.at(0)
const lastItem = arr.at(-1)

console.log(`First Item: ${firstItem}`) // prints 1
console.log(`Last Item: ${lastItem}`) // prints 5
```
