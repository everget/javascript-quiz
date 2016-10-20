## JavaScript Quiz (splited by divisions)
### Assignments

### Semicolon

### Coercions

### Hoisting

### Scopes

### Comma operator

### Constructors

### Miscellaneous
```js
var x1 = /[/ + 'javascript'[0] + '///';
x1;

var x2 = /\[/ + 'javascript'[0] + '///';
x2;
```

```js
with ({a: 1}) {
  a = 2,
  b = 3
};

[window.a, window.b];
```

```js
with (function (x, undefined) {}) length;
```

```js
(![]+[])[+[]]+(![]+[])[+!+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]];
```

```js
(function pewpew(Infinity, length, __proto__) {
  return [,,~0.[0|0]][pewpew.__proto__.length && Infinity, -~String(this).length >> __proto__] << (0. === .0) + Infinity;
}).apply(typeof pewpew, [,,2]);
```
