```javascript
function foo (a = 2, b = 'c', fn = (a)=>a+1) {
  console.log(fn(2))
}


function bar (a = 2, b = 'c', fn = function(a){return a+1;}) {
  console.log(fn(2))
}

foo();
bar();
```

```javascript
'use strict';

function foo() {
  var a = arguments.length <= 0 || arguments[0] === undefined ? 2 : arguments[0];
  var b = arguments.length <= 1 || arguments[1] === undefined ? 'c' : arguments[1];
  var fn = arguments.length <= 2 || arguments[2] === undefined ? function (a) {
    return a + 1;
  } : arguments[2];

  console.log(fn(2));
}

function bar() {
  var a = arguments.length <= 0 || arguments[0] === undefined ? 2 : arguments[0];
  var b = arguments.length <= 1 || arguments[1] === undefined ? 'c' : arguments[1];
  var fn = arguments.length <= 2 || arguments[2] === undefined ? function (a) {
    return a + 1;
  } : arguments[2];

  console.log(fn(2));
}

foo();
bar();
```
