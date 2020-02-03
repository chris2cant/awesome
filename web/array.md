# JS - Array

## Map

**Data**

```ts
let animals = [
    {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2},
    {name: 'Fluffball', type: 'rabbit', isNeutered: false, age: 1},
    {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}
  ]
```

**Example 1**

```ts
// What you need: 
// ['Tibbers', 'Fluffball', 'Strawhat']

let animalNames = animals.map(animal => {return animal.name});
```

**Example 2**
```ts
// what you need: 
// [{name: 'Tibbers', species: 'cat'}, {name: 'Fluffball', species: 'rabbit'}, {name: 'Strawhat', species: 'cat'}]

let petDetails = animals.map(animal => {
    return {
        name: animal.name, 
        species: animal.type
    };
});
```

## Filter

**Without filter**

```ts
let animals = [
   {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2},
   {name: 'Fluffball', type: 'rabbit', isNeutered: false, age: 1},
   {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}
 ]

let neuteredAnimals = [];

for (let i=0; i < animals.length; i++){
  let a = animals[i];
  if(a.isNeutered){
    neuteredAnimals.push(a);
  }
}
```

**With filter**

```ts
let animals = [
    {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2},
    {name: 'Fluffball', type: 'rabbit', isNeutered: false, age: 1},
    {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}
]

let neuteredAnimals = animals.filter((a) => {
    return a.isNeutered;
});
```

## Find

Instead of filter

```ts
let animals = [
    {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2},
    {name: 'Fluffball', type: 'rabbit', isNeutered: false, age: 1},
    {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}
  ]

animalTypeFound = animals.find( animal => animal.type === 'cat' );
// animalTypeFound will return:
// {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2}

animalTypeFilter = animals.filter( animal => animal.type === 'cat' );
// animalTypeFilter will return:
// [{name: 'Tibbers', type: 'cat', isNeutered: true, age: 2}, {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}]
```

## Reduce

```ts
// Prototype
arr.reduce(callback( accumulator, currentValue[, index[, array]] )[, initialValue])
```

```ts
// what you need:
// 130

let numbers = [100, 20, 10];

result = numbers.reduce((total, currentValue) => { return total + currentValue; });

// Explaination
// the first time, x = 100, y = 20
// the second time, x = 120, y = 10
```

```ts
// Data
let animals = [
    {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2},
    {name: 'Fluffball', type: 'rabbit', isNeutered: false, age: 1},
    {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}
  ]

// What you need ?
// Sum of animals age
// 8

let totalAge = animals.reduce((acculmulator, animal) => {
    return acculmulator + animal.age;
}, 0);

// lets say you want to find out the oldest animal 
// code below will return {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}

let oldestPet = animals.reduce((oldest, animal) => {
    return (oldest.age || 0) > animal.age ? oldest : animal;
  }, {});

  // decrypting the code above and how terniaries work 
  // the condition --> (oldest.age || 0) > animal.age 
  // if true --> ? oldest
  // else --> : animal
```

## Every

```ts
let animals = [
    {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2},
    {name: 'Fluffball', type: 'rabbit', isNeutered: false, age: 1},
    {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}
  ]

let allNeutered = animals.every(animal => {return animal.isNeutered});

//will return false because not all values under isNeutered evaluates to true
```

## Some 

```ts
let animals = [
    {name: 'Tibbers', type: 'cat', isNeutered: true, age: 2},
    {name: 'Fluffball', type: 'rabbit', isNeutered: false, age: 1},
    {name: 'Strawhat', type: 'cat', isNeutered: true, age: 5}
  ]

let someAreCats = animals.some(animal => {return animal.type === 'cat'});

// will return true because at least one animal.type returned 'cat'
```

## Sources 

- [6 Array Methods to Simplify Your JavaScript](https://medium.com/better-programming/simplify-your-javascript-with-these-6-array-methods-db4c278f08c9)
