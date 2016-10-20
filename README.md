## JavaScript Quiz
The simple test for JavaScript developers:)

```js
{ foo: 'bar' }; // ..?

{ 'foo': 'bar' }; // ..?

({ 'foo': 'bar' }); // ..?
```

```js
{ foo = 123 };
```

```js
vars: var vars = vars;
```

```js
var x = 1;
{
  var x = 2;
}

alert(x);
```

```js
'1' - - '1';
```

```js
delete delete window.document;
```

```js
'3' - 2 === 1;
```

```js
[] + {};

[] * {};
```

```js
if (9, 0) alert('ok');
```

```js
var a = []
(new Date).getTime();
```

```js
{} === {};
```

```js
[1] == true;
```

```js
1 && 3;
```

```js
{} + [];
```

```js
function foo() {
  return 'Какая-то строка';
};

function bar() {
  return
      'Какая-то строка';
};

foo() == bar();
```

```js
typeof (null && false);
```

```js
new String('foo') === 'foo';
```

```js
'5'+ +'6';
```

```js
var foo = {};
foo === foo;
```

```js
alert('2',
  foo = function (arg) {
    alert(arg)
  },
  foo('1')
),
foo('3');
```

```js
[3 + NaN + true] + [10 / (8 * null) - 1];
```

```js
10 > 9 > 8 === true;
```

```js
Math.max({}, 2);
```

```js
new Array([], null, undefined, null) == ',,,';
```

```js
(1, function(){})();
```

```js
'1.0e0' == { valueOf: function() { return true; } };
```

```js
Object.prototype.toString.call();
```

```js
if ( !('a' in window) ) {
  var a = 1;
};

alert(a);
```

```js
'00' == 0;
```

```js
'foo'.split('') + [];
```

```js
'foo' == new function() { return String('foo'); };
```

```js
{ break; 4; };
```

```js
' \t\r\n' == 0;
```

```js
RegExp.prototype.toString = function() { return this.source };

/3/-/2/;
```

```js
delete [].length;
```

```js
[2] == true;
```

```js
Array(2).join();
```

```js
Number.prototype.x = function() { return this === 123; };
Number(123).x();
```

```js
({} + 'b' > {} + 'a');
```

```js
[1, 2, 3, 4, 5][0..toString.length];
```

```js
1 || 'foo' && 0;

1 && 'foo' || 0;
```

```js
// TODO: remove
{ a: { b: 2 } };
```

```js
[4] * [4];
```

```js
{ a: 1, b: 2 }[['b']];
```

```js
1 + 2 + '3' == 1 + '2' + 3;
```

```js
a: b: c: d: e: f: g: 1, 2, 3, 4, 5;
```

```js
01-+-02-+-03;
```

```js
++'52'.split('')[0];
```

```js
var date = new Date('1999/12/31');
alert(date == '1999/12/31');
```

```js
[true, false][+true, +false];
```

```js
// TODO: remove
function isEven(arg) {
  if (arg % 2 == 0) return !!1;
  return;
};

if (isEven(3) == false) {
  alert('Odd number!');
};
```

```js
{ foo: 1 }[0];
```

```js
0.1 + (0.2 + 0.3) == (0.1 + 0.2) + 0.3;
```

```js
(1, 2, 3);
```

```js
if (new Boolean(false)) {
  alert('true');
};
```

```js
[] + [];
```

```js
'hello'.someProperty = 17;
'hello'.someProperty;
```

```js
Array.isArray({__proto__: Array.prototype });
```

```js
var s = new String('hello');
typeof 'hello';
typeof s;
```

```js
'Hello'[-1] == 'Hello'.charAt(-1);
```

```js
0 === -0;
```

```js
/^.$/.test('');
/^..$/.test('');
```

```js
Math.max(2, []);
```

```js
for (var i = 0; i < 10; i++) {
  setTimeout(function() {
       alert(i);
  }, 100);
};
```

```js
var s1 = new String('hello');
var s2 = new String('hello');
alert(s1 == s2);
alert(s1 === s2);
```

```js
x = 1; (function() {
  return x;
  var x = 2;
}());
```

```js
[4, 4] * [4, 4];
```

```js
var num1 = 5;
var num2 = 10;

num1+++num2;
```

```js
var x = function() {
  return arguments;
};

x() == x();
```

```js
function a(x) {
  return x * 2;
};

var a;
alert(a);
```

```js
[1 , 1] == true;
[[1], [1]] == true;
```

```js
var x = 0;
function foo() {
  x++;
  this.x = x;
  return foo;
};

var bar = new new foo;
alert(bar.x);
```

```js
1/0 === 1/-0;
```

```js
var a = 1,
var b = function a(x) {
  x && a(--x);
};

alert(a);
```

```js
var smth = (45, 87) > (195, 3) ? 'bar' : (54, 65) > (1, 0) ? '' : 'baz';
```

```js
function foo(a, b) {
  arguments[1] = 2;
  alert(b);
};

foo(1);
```

```js
(0.2 + 0.4) / 1 == (0.1 + 0.2) * 2;
```

```js
function b(x, y, a) {
  arguments[2] = 10;
  alert(a);
};

b(1, 2, 3);
```

```js
null == 0;
```

```js
function a() {
  alert(this);
};

a.call(null);
```

```js
(function() {
  return typeof arguments;
})();
```

```js
var f = function g() { return 23; }
typeof g();
```

```js
[[[[1]]]] == true;
```

```js
(function (x) {
  delete x;
  return x;
})(1);
```

```js
var y = 1, x = y = typeof x;
x;
```

```js
(function f(f) {
   return typeof f();
})(function() { return 1; });
```

```js
var foo = {
  bar: function() { return this.baz; }
  baz: 1
};

(function() {
  return typeof arguments[0]();
})(foo.bar);
```

```js
var foo = {
  bar: function() { return this.baz; }
  baz: 1
};
typeof (f = foo.bar);
```

```js
var f = (function f() { return '1'; }, function g() {return 2; })();
typeof f;
```

```js
alert('1', alert('2', alert('3')));
```

```js
var x = 1;
if ( function f() {} ) {
  x += typeof f;
};

x;
```

```js
[true] == true;
```

```js
var x = [typeof x, typeof y][1];
typeof typeof x;
```

```js
[3, 4, 5, 6][1, 2];
```

```js
(function (foo) {
  return typeof foo.bar;
})({ foo: { bar: 1 } });
```

```js
(function f() {
  function f() { return 1; }
  return f();
  function f() { return 2; }
})();
```

```js
function f() { return f; }
new f() instanceof f;
```

```js
var x = 5,
var o = {
  x: 10,
  doIt: function doIt() {
    var x = 20;
    setTimeout(function() {
        alert(this.x);
    }, 10);
  }
};

o.doIt();
```

```js
var o = {
  x: 8,
  valueOf: function() {
    return this.x + 2;
  },
  toString: function() {
    return this.x.toString();
  }
},
result = o < '9';

alert(o);
```

```js
var o = {
  b: function() {
      alert(this === o);
  }
};

o['b']();
```

```js
(function tada(printTwo) {
  printing: {
      console.log('one');
      if (!printTwo) break printing;
      console.log('two');
  }
  console.log('three');
})(true);
```

```js
var obj = {
  toString: function() {
    return '[object MyObject]';
  },
  valueOf: function() {
    return 17;
  }
};

alert('object: ' + obj);
```

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
