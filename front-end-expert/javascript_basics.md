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