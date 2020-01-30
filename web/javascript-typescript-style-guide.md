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

## Spacing

### Instruction 


## Indentation

```js
// Don't
if (condition) return (value); 

// Don't
if (condition) {return (value);}

// Do
if (condition)
{
  return (value);
}
```

## Sources

- [Coding like Shakespeare](https://dmitripavlutin.com/coding-like-shakespeare-practical-function-naming-conventions/)
- [AngularJS - Style Guide](https://github.com/johnpapa/angular-styleguide/blob/master/a1/README.md)
- [Data Structures Algorithms](https://github.com/amejiarosario/dsa.js-data-structures-algorithms-javascript/blob/master/README.md)
- [Clean code typescript](https://github.com/labs42io/clean-code-typescript/blob/master/README.md)
