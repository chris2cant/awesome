# Write a documentation - Style guide

## Keep It Short

People don’t like to read. That is why good explanations attempt to cut down the length of sentences and supplement explanations with pictures and illustrations.

> If I had more time, I would have written a shorter letter.

## Explain your instructions

Help reader understand and give meaning to your instructions.

**Recommanded**
```
Push your code every day.

Why ? : Your computer can crash during the night.
Why ? : Your code is safer on git server (And your computer).
Why ? : You can avoid to loose your work with an accidentally "rm -rf my-folder"
Why ? : You avoid to push your code if you are sick tomorrow
```

**Avoid**
```
Push your code every day.
```

## Comment your commands

- `Why ?` : Not everyone knows what's append
- `Why ?` : The reader must understand

**Recommanded**
```sh
# -b : Create a new branch
git checkout -b feature/my-feature

# - : Return to your previous checkout branch
# Exemple : git checkout master (switch to master); git checkout my-branch (switch to my-branch); git checkout - (switch to master)
git checkout -
```

**Avoid**
```sh
git checkout -b feature/my-feature
```

## Use full option

It's recommanded to use full option instead the short version.

- `Why ?` : Easier to understand the option without manual
- `Why ?` : The reader must understand and reuse the option

**Recommanded**
```sh
Recommanded
# --save-dev : Save the package in your package.json in devDependencies
npm install bootstrap --save-dev
```
```sh
# --save-dev or -D : Save the package in your package.json in devDependencies
npm install bootstrap --save-dev
```

**Avoid**
```sh
npm install bootstrap -D
```

## Bullet points

Try to use bullet points instead long phrase.

- `Why ?` : More efficient than a long phrase.
- `Why ?` : Easier to read.

**Example 1 : Recommanded**
```txt
I want to:
  - customize tools...
  - custom shows...
  - custom animations...
```

**Example 1 : Avoid**
```txt
I want to customize tools...
I want to have custom shows...
I want to do custom animations...
```

**Example 1 : Avoid**
```txt
I want to customize tools... I want to have custom shows... I want to do custom animations...
```

**Example 2 : Recommanded**
```txt
# P = pressure
# V = volume
# n = number of gas molecules measured in moles
# R = the gas constant
# T = temperature, measured in Kelvin

PV = nRT
```

**Example 2 : Avoid**
```txt
# The product of gas pressure and gas volume is equal to the number of gas molecules measured in moles times the gas constant,
# times the temperature of the gas in Kelvin.
PV = nRT
```

## Sources

- [The Case Against Descriptive Variable Names](https://medium.com/@Jernfrost/the-case-against-descriptive-variable-names-3c09dee0bac5)
