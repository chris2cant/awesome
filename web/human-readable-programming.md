# Human Readable Programming

## Resume

Reduce :
  - Comments
  - Code Complexity
  - Pull Request Review Time
  - Bugs

## Example 

### Before

```typescript
// Complexity : 7
const sendToSanta = (items, discount) => {
	let totalPrice = 0;
	// Get total price
	for (let i = 0; i < items.length; i++) {
		totalPrice += items[i].price;
	}
	// Apply Discount
	if (discount >= 0) {
		totalPrice -= discount;
	} 
	// Check if the account is not too low
	if (this.myAccount.amount > 0 && this.myAccount.amount >= totalPrice) {
		// procced To Paiment
		API.paiement().subscribe(() => {
			console.log('Merry Christmas');
		}).catch(() => {
			console.error('An error appear :(');
		});
	}
}
```

### After

```typescript
// Complexity : 2
const sendToSanta = (items, discount) => {
	let totalPrice = 0;
	totalPrice = getTotalPrice(items);
	totalPrice = applyDiscount(totalPrice, discount);
	if(canPay(this.myAccount.amount, totalPrice)) {
		makeThePaiement(totalPrice);
	}
}
```

## Convert your code

### Functions

#### Before

```typescript
// Complexity : 2
const sendToSanta = (items, discount) => {
  // getTotalPrice
  let totalPrice = 0;
  for (let i = 0; i < items.length; i++) {
    totalPrice += items[i].price;
  }
  ...
}
```

#### After

```typescript
// Complexity : 1
const sendToSanta = (items, discount) => {
  let totalPrice = 0;
  totalPrice = getTotalPrice(items);
  ...
}

// Complexity : 2
const getTotalPrice = (items) => {
  let totalPrice = 0;
  for (let i = 0; i < items.length; i++) {
    totalPrice += items[i].price;
  }
  return totalPrice;
}
```

### Conditions

Why ? :
  - Easier to Read
  - Reusable

#### Before
  
```typescript
if (this.myAccount.amount > 0 && this.myAccount.amount >= totalPrice) {
 ...
}
```

#### After

```typescript
if(canPay(this.myAccount.amount, totalPrice)) {
  ...
}

const canPay = (totalPrice) => {
	return (this.myAccount.amount > 0 && this.myAccount.amount >= totalPrice)
}
```

## Articles

- [NEVER comment your code again!](https://medium.com/@devlob/never-comment-your-code-again-d230462b84f)
- [Cyclomatic Complexity — Programming Word of the Day](https://medium.com/background-thread/cyclomatic-complexity-programming-word-of-the-day-37377f7279ff)
- [Human Readable Code or Why I Don’t Like if Statements](https://medium.com/hackernoon/human-readable-code-or-why-i-dont-like-if-statements-c4fb38d3e693)
