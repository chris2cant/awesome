# Javascript/Typescript - Style Guide

This style guide is inspired from the john papa style guide.

## Small Functions

**Pro** :
- Easy to :
  - Test
  - Read
  - Reuse
  - Maintain
  
## Naming 

### Variables 

#### Boolean

```javascript
// IS
isLoading, isActive, isLogged, isSet, isVisible, isFinished, isFound, isOpen
// HAS
hasError, hasLicense, hasCar
// CAN
canEvaluate, canEdit, canRead
```

#### Number Of

```javascript
numberOfUsers, numberOfCars, numberOfItems, numberOfMessages, numberOfTickets
```

#### List of ids

- Why ? : A list of ids (plural), each belonging to a single user (singular)

```javascript
// Recommanded
userIds

// Avoid
usersId
```

### Function

#### Computed

```javascript
cars.computeTotalPrice();
```

### Complement name

```javascript
get/set, add/remove, create/destroy, start/stop, insert/delete, increment/decrement, old/new, begin/end, first/last, up/down, min/max, next/previous, old/new, open/close, show/hide, suspend/resume, etc.
```

## Named Functions instead Anonymous Function

**Pro Named Function** :
- Easy to :
  - Test
  - Reuse

### Examples

```javascript
// Avoid
myArray.filter((value) => {
   return item > 0 ? true : false;
});
```

```javascript
// Recommanded
// + Test separately isPositive function
// + Reuse isPositive
// + Easier to read myFunc(isPositive);
const isPositive = (value) => {
   return item > 0 ? true : false;
};

myArray.filter(isPositive);
```

## Spacing & Indentation

- **Why?** : Improve comprehension

- Space after `if` `else` `while` `for`
```ts
// Don't (No space after "if" and "return")
if(condition) {
  return(value);
}

// Do
if (condition) {
  return (value);
}
```

- Curly Brace required

```ts
// Don't (No curly brace)
if (condition)
  return (value);

// Do
if (condition) {
  return (value);
}

// Don't (No curly brace)
if (condition)
  if (condition2)
    return (value2);
  return (value);

// Do
if (condition) {
  if (condition2) {
    return (value2);
  }
  return (value);
}
```

- Align the closed curly brace with statement

```js
// Don't (Closed Curly brace not align with second if)
if (condition) {
  if (condition2) {
    return (value);
    } // <- Not aligned
  return (value);
}

// Do
if (condition) {
  if (condition2) {
    return (value2);
  }
  return (value);
}
```

- No code and curly brace on the same line
- Space instead Tab
- Use 2 spaces size
  - **Why ?** : Enougth to indent
  - **Why ?** : Keep your code under 80 columns
  - **Why ?** : Used by Airbnb, NodeJS, etc...

```js
// Don't (4 spaces per indentation)
if (condition) {
    return (value);
}

// Do (2 spaces per indentation)
if (condition) {
  return (value);
}
```

- 1 space after `,` and `;`

```js
// Don't
for (let i = 0;i < 9;i++) {
  myFunction(name,age);
}

// ✅Do
for (let i = 0; i < 9; i++) {
  myFunction(name, age);
}
```

- 1 space before and after binary operator (``)

```js
// Don't
x+=10*++x;

// ✅Do
x += 10 * ++x;
```

**Spaces to be clear**



**2 Spaces instead 1 Tab**



```js
// Don't (No Curly braces & One line)
if (condition) return (value); 

// Don't (One line)
if (condition) {return (value);}

// Don't (4 spaces per indentation)
if (condition) {
    return (value);
}

// Don't (No space after "if")
if(condition) {
  return (value);
}

// Don't (No space after ")")
if (condition){
  return (value);
}

// ✅Do
if (condition)
{
  return (value);
}

// ✅Do
if (condition) {
  return (value);
}
```

```js
// Don't
if (condition) return (value) else return (-1); 

// Don't
if (condition) {return (value);} else {return (-1);}

// Do
if (condition)
{
  return (value);
}
else
{
  return (-1);
}

// Do
if (condition) {
  return (value);
} else {
  return (-1);
}
```

## Tools

- [Refactoring Guru](https://refactoring.guru/)

## Sources

- [Coding like Shakespeare](https://dmitripavlutin.com/coding-like-shakespeare-practical-function-naming-conventions/)
- [AngularJS - Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md)
- [Data Structures Algorithms](https://github.com/amejiarosario/dsa.js-data-structures-algorithms-javascript/blob/master/README.md)
- [Clean code typescript](https://github.com/labs42io/clean-code-typescript/blob/master/README.md)
- [Epita - Norme](https://www.lrde.epita.fr/~raph/docs/epita-css/norme-fr.pdf)
- [Stop Using isLoading booleans](https://kentcdodds.com/blog/stop-using-isloading-booleans)
