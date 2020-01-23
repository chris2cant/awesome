# Angular

## Package

- [Ngx Mask](https://www.npmjs.com/package/ngx-mask)
- [Extensible Dev Tools for Monorepos](https://nx.dev/angular)

## Component

### Access to the parent component

```ts
export class MslFieldComponent implements OnInit {
  constructor(private readonly parentComponent: ParentComponent) {}

  ngOnInit() {
    console.log(parentComponent);
  }
}
```

[Stackblitz Example](https://stackblitz.com/edit/angular-general-parent-injection?file=app%2Fhello.component.ts)

## Mocking 

- Why ? : Work without backend at any time.
- Why ? : Dev and test with mocked data.
- Why ? : Show your frontend without backend issues

- [Angular 7 - Mock Backend Example for Backendless Development](https://jasonwatmore.com/post/2019/05/02/angular-7-mock-backend-example-for-backendless-development)
- [Angular Http Mock Interceptor for mocked backend](https://dev.to/sanidz/angular-http-mock-interceptor-for-mocked-backend-1h5g)

## ng-select 

- [Stackblitz - Example Customisation](https://stackblitz.com/edit/ng-select)

## Articles

- Testing
  - [Integrate Jest into an angular app and library](https://blog.angularindepth.com/integrate-jest-into-an-angular-application-and-library-163b01d977ce)
- Performance
  - [Best practices for a clean and performant Angular application (2018/10/30)](https://www.freecodecamp.org/news/best-practices-for-a-clean-and-performant-angular-application-288e7b39eb6f/)
- Schematics
  - [Schematics — An Introduction](https://blog.angular.io/schematics-an-introduction-dc1dfbc2a2b2)
  - [How to create your first custom angular schematics with ease](https://medium.com/@tomastrajan/%EF%B8%8F-how-to-create-your-first-custom-angular-schematics-with-ease-%EF%B8%8F-bca859f3055d)

## Webpack Build

- [Customizing Angular CLI build](https://codeburst.io/customizing-angular-cli-6-build-an-alternative-to-ng-eject-a48304cd3b21)

## Articles & Ressources

- [Angular Performance Checkelist](https://github.com/mgechev/angular-performance-checklist)
- [Awesome Angular](https://github.com/PatrickJS/awesome-angular)

## Contributors

- Jeremy Ciamous
