# Angular - Testing

## SpyOn

```javascript
// Should call
it('Should call myFunc', () => {
  const spiedFunction = spyOn<any>(component, 'myFunc');
  component.myMethod();
  expect(spiedFunction).toHaveBeenCalled();
});

// Should not call
it('Should not call myFunc', () => {
  const spiedFunction = spyOn<any>(component, 'myFunc');
  component.myMethod();
  expect(spiedFunction).not.toHaveBeenCalled();
});
```

### External function

```javascript
import * as dateHelper from './date.helper';

it('Should call dayIsValid', () => {
  const spiedFunction = spyOn<any>(
    dateHelper,
    'isValid'
  ).and.returnValue({});
  component.myMethod();
  expect(spiedFunction).toHaveBeenCalled();
});
```

### Private method

```javascript
it('Should call myFunc', () => {
  const spiedFunction = spyOn<any>(component, 'myFunc');
  component.myMethod();
  expect(spiedFunction).toHaveBeenCalled();
});
```

## Service

## Have been called

```ts
let myCustomService: MyCustomService;
  beforeEach(async(() => {
    TestBed.configureTestingModule({
      imports: [],
      declarations: [],
      providers: [{ provide: MyCustomService, useClass: MockedMyCustomService }]
    }).compileComponents();
  }));
  
  beforeEach(() => {
    fixture = TestBed.createComponent(MyCustomComponent);
    component = fixture.componentInstance;
    fixture.detectChanges();
    myCustomService = TestBed.get(MyCustomService);
  });
  
  it('Should diplay a modal', () => {
    const spiedFunction = spyOn(myCustomService, 'open');
    component.methodWhoCallMyCustomService();
    expect(spiedFunction).toHaveBeenCalled();
  });
```

## Rxjs

### throwError

```ts
// Your code
function methodThatReturnsThrowingObs() {
  return throwError({
    error: 'My error'
  });
}

// Your test
it('should throw an error', (done: DoneFn) => {
  methodThatReturnsThrowingObs().subscribe({
    error: (err) => {
      expect(err).toEqual({ error: 'My error' });
      done();
    }
  })
});
```

## Tools

- [Spectator](https://github.com/ngneat/spectator)
- [BackstopJS](https://github.com/garris/BackstopJS)
- [Jasmine Marbles](https://github.com/synapse-wireless-labs/jasmine-marbles) - Observable testing

## Articles

- [Angular Testing Cheatsheet](https://dev.to/lysofdev/an-angular-testing-cheatsheet-5hj2)
