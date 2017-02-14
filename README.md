# jasmine-spy
Helper that works as a shortcut to create jasmine spies that return values or promises

## Installation

```bash
npm i --save-dev jasmine
npm i --save-dev jasmine-spy
```

## Usage

```js
const Spy = require('jasmine-spy');

describe('your test', () => {
  let myStub;
  beforeEach(() => {
    myStub = {
      'doSomething': Spy.create(),
      'doSomethingElse': Spy.returnValue('a'),
      'anotherMethod': Spy.resolve('the result'),
      'yetAnotherMethod': Spy.reject('some error'),
      'oneMore': Spy.returnValues('a', 'b', 'c'),
      'another': Spy.throwError('something went wrong'),
    };
  });
});
```

## Credits and License

Developed by [Devsu](https://devsu.com). Copyright 2017.

MIT license.
