# App debugger
### A `console.log` with *super powers*!

Transform your `console.log` into a customizable logs in console debug.
This not override the default `console.log`, it just add a new way to debug with **css styles**.

## How to install

```js
npm install app-debugger
```

Then you call it with `import` or `require`:
```js
import debug from 'app-debugger'

//OR

const debug = require('app-debugger');
```

## How to use

The are *4 methods* the you can use:
```js
debug.show
debug.info
debug.warn
debug.danger
```

The default styles for this methods are:
```js
const styles = {
  default: 'color: gray; font-weight: bold;',
  info: 'color: blue; font-weight: bold;',
  warn: 'color: #ffc107;',
  danger: 'color: lightcoral; font-weight: bold;'
}
```

## Basic examples

See how this example are shown in console
```js
debug.show('default')();
debug.info('info')();
debug.warn('warn')();
debug.danger('danger')();
```

![demo1](demo1.png "Basic example, single messages")

You can pass how many values you want to **debug methods**, if you have more than just one, the first *string** message becames a "label message" for your log. Take a look:


```js
const arrObj = [
  {
    "obj1": "lorem value",
    "obj2": "lorem value"
  },
  {
    "obj1_2": "lorem value",
    "obj2_2": "lorem value"
  }
]
const arr = ['arr', 'arr2', 'arr3'];

const fn = function(){
  console.log('A function');
}

//call debug for each value passing a custom message label

debug.show('label message:', arrObj)();
debug.info('label message:', arr)();
debug.warn('label message:', arr, arrObj)();
debug.danger('label message:', fn)();
```

See how this example are shown in console

![demo2](demo2.png "label message")
