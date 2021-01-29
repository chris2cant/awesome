# CSS Styleguide

## Conventions

- BEM

```css
// block
.button {}
// Child
.button__icon {}
.button__content {}
// Modifier
.button--disabled {}
.button--primary {}
.button--primary-inverted {}
```

```html
<button class="button button--primary button--disabled">
  Submit
</button>
```

- [ABEM](https://css-tricks.com/abem-useful-adaptation-bem/)

```css
// block
.button {}
// Child
.button__icon {}
.button__content {}
// Modifier
.button.-disabled {}
.button.-primary {}
.button.-primary-inverted {}
```

```html
<button class="button -primary -disabled">
  Submit
</button>
```
