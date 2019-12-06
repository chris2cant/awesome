# 🏗 Angular - Schematics

## Build

[tsconfig](https://github.com/angular-extensions/model/blob/master/tsconfig.schematics.json)

```json
{
  "scripts": {
  "schm:build": "tsc -p tsconfig.schematics.json && cpx schematics/**/{collection.json,schema.json,files/**} dist/schematics"
  }
}
```


## Build in "dist" folder

`tsconfig.ts`
```json
{
  "compilerOptions": {
    "outDir": "dist"
  }
}
```

## 🗒 Articles

- [Use Angular Schematics to Simplify Your Life](https://developer.okta.com/blog/2019/02/13/angular-schematics)
