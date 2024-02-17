# Javascript Basics

## Variables and Scoping

```js
console.log('varNum', varNum);
console.log('letNum', letNum);

var varNum = 0;
let letNum = 0;
```
Difference between var and let is that var is hoisted and let is not. Hoisting means that variable is declared by JS before it is used automatically. In the above example varNum would show undefined and letNum would thriw error.

Most of the time we shoud be using let because the roles for let is more natural and easy to understand whereas var can see ambiguous due to Hoisting.

```js
const constNum = 0;
let letNum = 0;
const arr = [1,2,3,4];
arr.push(5);
console.log(arr);
```

The above would work because we are not reassigning the arr. We are only pushing a new element into it.

> Javascript is very functional language. Most often we try to call functions on values rather than reassign.

## Objects

```js
const myKey = 'key';
const website = {
    name: 'Optum',
    rating: 5,
    'multi word key': 0, //multi word key should be enclosed in single quotes.
    [myKey]: 1234
}
```
### Getting Object Values

```js
website['key'];
website.name // commonly used unless you have to use a variable as a key or a multi word key.
```

### Inheritance

```js
const website = {
    name: 'Optum',
    rating: 5,
    'multi word key': 0 // multi word key should be enclosed in single quotes.
    [myKey]: 1234
}

const obj = {
    __proto__: website // this is how an object can inherit the propertyies of another object
};
```
### Equality and Type Coersion

## Equality
```js
console.log(5 == 5); // loose quality: only compare values.
console.log(5 === 5); // strict quality: compare type and values.
console.log('abc' == NaN) // this is false, bacause when abc is coersed to a number, it becomes NN and, Nan is not equal to anything even itself.
```
#### Loose Quality
- If both values are null or undefined, return ```true```
- convert boolean to numbers, true converts to 1 and false to 0.
- when string and numbers are compared, convert string to a number.
- when comparing object and string, convert object to string using toString() or valueOf() methods.

 > Strict Quality is preferred because it is easy to predict.
 > NaN is not equal to anything including itself.

 #### Strict Quality
 - if either values is NaN, return false.
 - if the values have different types, return false.
 - If both the values are null or both the values are undefined, return true.
 - if both the values are objects, return true if they are the same object else return false.
 
 ### Type Coercion

 Conversion of the object from one type to another implicitly during equality check or explicit is called type coercion.

 > Implicit type conversion: coercion and explicit type coercion: type casting.