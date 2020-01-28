# Design Token

Design tokens are the visual design variables of the design system. (Color / Size / Spacing / Shape / etc...)

- **Why ?** : Keep the consistency.
- **Why ?** : Simplify understanding between UX, UI & Dev ($primary instead #6200EE)

## Methodology

### Shirt size

- **Why ?** : Limit the amount of choice
- **Why ?** : Easy to use

Only 6 choices : `xs` `s` `m` `l` `xl` `xxl`

## Colors 

### Theme

```scss
$primary: #6200EE;
$on-primary: white;
$secondary: #3700B3;
$on-secondary: white;
$accent: #03DAC6;
$on-accent: white;

$background: white;
$on-background: black;
$surface: white;
$on-surface: black;

$error: #B00020;
$on-error: black;
```

### Grey scale

```scss
$grey-100: #f5f5f5;
$grey-200: #ececec;
$grey-300: #e9e9e9;
$grey-400: #d8d8d8;
$grey-500: #cccccc;
$grey-600: #999999;
$grey-700: #454545;
$grey-800: #222222;
```

## Fonts

### Weight

```scss
$font-weight-s: 400;
$font-weight-m: 500;
$font-weight-l: 700;
```

### Size

```scss
$font-size: (1.1rem, 1.2rem, 1.4rem, 1.5rem, 1.8rem, 2.3rem, 3.4rem, 4rem);
```

### Line height

```scss
$line-height: (1.6rem, 2.4rem, 3.2rem, 4.8rem, 5.6rem);
```

## Spacing

```scss
$spacing-xs: 0.8rem;
$spacing-s: 1.6rem;
$spacing-m: 2.4rem;
$spacing-l: 3.2rem;
$spacing-xl: 4rem;
$spacing-xxl: 6.4rem;
```

## Shape

```scss
$radius-s: 0.3rem;
$radius-m: 0.5rem;
$radius-l: 0.7rem;
```

## disabled

```scss
$disabled-border-color: $grey-600;
$disabled-border-size: 1px;
```
