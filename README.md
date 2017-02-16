## JavaScript Quiz
The simple test for JavaScript developers:)

## Table of Contents
1. [Labels & Blocks](#labels--blocks)
1. [Semicolons](#semicolons)
1. [Coercions & Comparisons](#coercions--comparisons)
1. [Calculus](#calculus)
1. [Conditional statements](#conditional-statements)
1. [Typeof operator](#typeof-operator)
1. [Comma operator](#comma-operator)
1. [Try Catch Statement](#try-catch-statement)
1. [Scopes & Closures & Hoisting](#scopes--closures--hoisting)
1. [Properties](#properties)
1. [Delete operator](#delete-operator)
1. [Object](#object)
1. [Function](#function)
1. [Custom constructors](#custom-constructors)
1. [Promise](#promise)
1. [Symbol](#symbol)
1. [Array](#array)
1. [Date](#date)
1. [RegExp](#regexp)
1. [String](#string)
1. [Number](#number)
1. [Boolean](#boolean)
1. [Arguments](#arguments)
1. [Math](#math)
1. [Miscellaneous](#miscellaneous)

### Labels & Blocks

```js
{ break; 4; }; // => ?
```

```js
vars: var vars = vars; // => ?
```

```js
{ foo = 123 };
```

```js
var bar = 1,
    foo = {};

foo: {
    bar: 2;
    baz: ++bar;
};

foo.baz + foo.bar + bar;
```

```js
{ 1; 2; } 3
```

```js
{ foo: 1 }[0];
```

```js
a: b: c: d: e: f: g: 1, 2, 3, 4, 5;
```

```js
xxx: {
  console.log(111);
  break xxx;
  console.log(222);
};
```

```js
(function tada(printTwo) {
  printing: {
     console.log('one');
     if (!printTwo) break printing;
     console.log('two');
  };
  console.log('three');
})(true);
```

**[Back to top](#table-of-contents)**

### Semicolons

```js
var a = []
(new Date).getTime();
```

```js
let [a, b, c] = [1, 2, 3];

a = b
++c

[a, b, c]; // => ?
```

```js
function foo() {
  return 'Some string';
};

function bar() {
  return
      'Some string';
};

foo() == bar(); // => ?
```

```js
a = b
/hi/g.exec(c).map(d);
```

**[Back to top](#table-of-contents)**

### Coercions & Comparisons

```js
!!~1;
```

```js
'3' - 2 === 1;
```

```js
[1] == true;
```

```js
'1' - - '1';
```

```js
'5' + + '6';
```

```js
1 + 2 + '3' == 1 + '2' + 3;
```

```js
'1' + 2 + '3' + 4;
```

```js
[2] == true;
```

```js
'a' + + 'b';
```

```js
[4] * [4];
```

```js
++'24'.split('')[0];
```

```js
4 + 3 + 2 + '1';
```

```js
[true] == true;
```

```js
null == 0;
```

```js
[1 , 1] == true;
```

```js
' \t\r\n' == 0;
```

```js
'foo'.split('') + [];
```

```js
[[1], [1]] == true;
```

```js
({} + 'b' > {} + 'a');
```

```js
[] + [] + 'foo'.split('');
```

```js
[[[[1]]]] == true;
```

```js
[] + {};

[] * {};
```

```js
{} + [];
```

```js
[] + [];
```

```js
[][[]];
```

```js
[4, 4] * [4, 4];
```

```js
var foo = {};
foo === foo;
```

**[Back to top](#table-of-contents)**

### Calculus

```js
-9 % 7;
```

```js
var
  num1 = 5,
  num2 = 10,
  num3 = num1+++num2;

`${num1} ${num2} ${num3}`; // => ?
```

```js
1 + - + + + - + 1;
```

```js
0 === -0;
```

```js
var c = 0;

c+++c++; // => ?
```

```js
~~(-5.5);
```

```js
10 > 9 > 8 === true;
```

```js
'00' == 0;
```

```js
+0 < -0; // => ?
```

```js
0.1 + (0.2 + 0.3) == (0.1 + 0.2) + 0.3;
```

```js
(0.00008).toFixed(3) === 0;
```

```js
Infinity > - Infinity; // => ?
```

```js
parseInt(null, 24) === 23;
```

```js
0 < 5 < 3; // => ?
```

```js
01 - + - 02 - + - 03;
```

```js
12..toFixed(1);
```

```js
(0.2 + 0.4) / 1 == (0.1 + 0.2) * 2;
```

```js
1 / 0 === 1 / -0;
```

```js
1 / parseFloat('-0') !== -Infinity;
```

```js
~~+'2.9'-1 == ('2.9' >> 0) - 1;
```

```js
4 - '5' + 0xf - '1e1';
```

```js
(0.9).toFixed(0);
```

```js
[3 + NaN + true] + [10 / (8 * null) - 1];
```

```js
parseInt(1 / 0, 19);
```

```js
'3' > '12' === '03' > '12';
```

```js
parseFloat('\t\v\r12.34\n ');
```

**[Back to top](#table-of-contents)**

### Conditional statements

```js
('false') && ('bar'); // => ?
```

```js
1 || 'foo' && 0; // => ?

1 && 'foo' || 0; // => ?
```

```js
1 && 3; // => ?
```

```js
let x = NaN;
switch (x) {
  case NaN: console.log('Hello, NaN!');
            break;
  default: console.log('Hello, default!');
};
// => ?
```

```js
let a, b;
a = (b = 0) && (b = 1);

[a, b]; // => ?
```

```js
let x = {};
switch (x) {
  case {}: console.log('Hello, object!');
           break;
  default: console.log('Hello, default!');
};
// => ?
```

**[Back to top](#table-of-contents)**

### Typeof operator

```js
var y = 1, x = y = typeof x;
x;
```

```js
typeof JSON;
```

```js
var x = [typeof x, typeof y][1];
typeof typeof x;
```

```js
typeof (null && false);
```

```js
typeof new ReferenceError; // => ?
```

```js
typeof typeof(typeof(undefined)); // => ?
```

```js
typeof new Number(4);
```

```js
((foo) => typeof foo.bar)({ foo: { bar: 1 } }); // => ?
```

**[Back to top](#table-of-contents)**

### Comma operator

```js
(1, 2, 3);
```

```js
var a = 0;
var b = (a++, 99);

[a, b]; // => ?
```

```js
(1, function(){})();
```

```js
if (9, 0) console.log('ok');
```

```js
[true, false][+true, +false];
```

```js
var smth = (45, 87) > (195, 3) ? 'bar' : (54, 65) > (1, 0) ? '' : 'baz';
```

```js
alert('1', alert('2', alert('3')));
```

```js
typeof ('a', 3);
```

```js
var f = (function f() { return '1' }, function g() { return 2 })();
typeof f;
```

```js
[3, 4, 5, 6][1, 2];
```

```js
if ((1, true) && (2, false) || (3, false) && (4, true) || (5, true)) {
  console.log('awesome js');
};
```

```js
alert('2',
  foo = (arg) => alert(arg),
  foo('1')
),
foo('3');
```

**[Back to top](#table-of-contents)**

### Try Catch Statement

```js
try {
 throw new Error();
} catch (err) {}
```

```js
try {
  setTimeout(function() {
   throw new Error()
  }, 1000);
} catch (err) {}
```

**[Back to top](#table-of-contents)**

### Scopes & Closures & Hoisting

```js
var x = 1;
{
  var x = 2;
}

x; // => ?
```

```js
if (!('a' in window)) {
  var a = 1;
};

a; // => ?
```

```js
function a(x) {
  return x * 2;
};

var a;
typeof a; // => ?
```

```js
var foo = 1;
function bar() {
  foo = 10;
  return;
  function foo() {};
};

bar();
foo; // => ?
```

```js
var foo = function bar() { return 23 };
typeof bar();
```

```js
x = 1;
(() => {
  return x;
  var x = 2;
})();
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
function a() {
  alert(this);
};

a.call(null);
```

```js
var x = 1;
if (function f() {}) {
  x += typeof f;
};

console.log(x);
```

```js
var foo = {
  bar: function() { return this.baz },
  baz: 1
};

typeof (f = foo.bar);
```

```js
var x = 3;
var foo = {
  x: 2,
  baz: {
    x: 1,
    bar: function() {
        return this.x;
    }
  }
};

var go = foo.baz.bar;

go() === foo.baz.bar();
```

```js
(function f() {
  function f() { return 1; }
  return f();
  function f() { return 2; }
})();
```

```js
for (var i = 0; i < 10; i++) {
  setTimeout(() => alert(i), 100);
};
```

```js
var foo = 11;
function bar() {
  return foo;
  foo = 10;
  function foo() {};
  var foo = '12';
};

typeof bar();
```

```js
function f() {
  var a = 5;
  return new Function('b', 'return a + b');
};

f()(1);
```

```js
var a = 1,
var b = function a(x) {
  x && a(--x);
};

a; // => ?
```

```js
f.call(f);

function f() {
  return this;
};
```

```js
(function() {
  var foo = 'a';

  (function (foo) {
    foo = 'b';
  })(foo);

  return foo;
})();
```

```js
(function f(f) {
  return typeof f();
})(() => 1);
```

**[Back to top](#table-of-contents)**

### Properties

```js
{ a: 1, b: 2 }['b'];
```

```js
let obj = {
 '': ''
};

obj['']; // => ?
```

```js
var obj = {
  toString: () => '[object MyObject]',
  valueOf: () => 17
};

'object: ' + obj; // => ?
```

```js
var o = {
  x: 8,
  toString: () => this.x.toString()
};

o.toString(); // => ?
```

```js
var obj = {
  1: 'I love this awesome language'
};

obj[1] == obj[[1]];
obj[[1]] == obj['1'];
```

```js
'hello'.someProperty = 17;
'hello'.someProperty; // => ?
```

```js
(function() {
  return (function (a, b) {}).length;
})();
```

```js
({ 'toString': null }).propertyIsEnumerable('toString');
```

```js
(function() {
  var foo = {};
  var bar = {};
  var map = {};

  map[foo] = 'foo';
  map[bar] = 'bar';

  return map[foo];
})();
```

```js
var o = {
  a: function() { return this === o },
  b: () => this === o
};

o.a() === o.b();
```

```js
'1.0e0' == { valueOf: () => true };
```

```js
var a = 1;
var b = { toString: () => '1' };
var c = 1;

a + b + c;
```

**[Back to top](#table-of-contents)**

### Delete operator

```js
var numbers = [2, 3, 5, 7, 11, 13];
delete numbers[3];

numbers.length; // => ?
```

```js
delete [].length;
```

```js
function foo() {};
delete foo.length;

typeof foo.length; // => ?
```

```js
var Person = function() {};
Person.prototype.type = 'person';

var admin = new Person();
delete admin.type;

admin.type; // => ?
```

```js
delete delete window.document;
```

```js
(function (x) {
  delete x;
  return x;
})(1);
```

```js
var a = 1;
b = 1;

(function() {
  return (delete window.a) === (delete window.b);
})();
```

**[Back to top](#table-of-contents)**

### Object

```js
Object.prototype.toString.call();
```

```js
Object.prototype.toString.call(Object);
```

```js
Object.is(NaN, NaN);
Object.is(-0, +0);
```

```js
var proto = {
  x: () => 'x'
}

var o1 = new Object(proto);
var o2 = new Object(proto);

o1 === o2;
```

```js
Object.prototype.isPrototypeOf(window);
```

**[Back to top](#table-of-contents)**

### Function

```js
Function instanceof Function;
```

```js
Function.prototype.prototype; // => ?
```

```js
function x() {};

let y = x.bind();

y.prototype; // => ?
```

```js
function add(x, y) {
  return x + y;
};

const plus1 = add.bind(undefined, 1);

plus1(); // => ?
```

```js
let a = () => this;

let b = function() { return this }.bind(this);

a() === b(); // => ?
```

```js
function one() {};

let two = one.bind(this);

two.name; // => ?
```

```js
async myFunc() {};

Object.prototype.toString.call(myFunc);
```

**[Back to top](#table-of-contents)**

### Custom constructors

```js
var x = 0;
function foo() {
  x++;
  this.x = x;
  return foo;
};

var bar = new new foo;
bar.x; // => ?
```

```js
function CustomType() {};

new CustomType instanceof CustomType; // => ?
```

```js
function f() { return f; }

new f() instanceof f; // => ?
```

**[Back to top](#table-of-contents)**

### Promise

```js
typeof Promise;
```

```js
let promise = Promise(() => {}, () => {});
```

**[Back to top](#table-of-contents)**

### Symbol

```js
typeof Symbol;
```

```js
class MySymbol extends Symbol {
  constructor() {
    super()
  }
}

let symbol = new MySymbol(); // => ?
```

**[Back to top](#table-of-contents)**

### Array

```
typeof [1, 2, 3];
```

```js
[].unshift(0);
```

```js
Array(2).join();
```

```js
[1, 2, 3].toString();
```

```js
var arr = [2, 3, 5, 7, 11];

arr.indexOf(7, 2);
arr.indexOf(2, -3);
```

```
'0'.split(void 0, 0);
```

```js
[].concat[1,2,3];
```

```js
[1, 2, 3, 4, 5][0..toString().length];
```

```js
Array(4).join('tada!' - 4);
```

```js
[NaN].indexOf(NaN);
```

```js
var arr = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

arr.slice();
arr.slice(-2);
arr.slice(3, -6);
```

```js
new Array([], null, undefined, null) == ',,,';
```

```js
(function() {
  return Array(3).map(function (item) { return 'a' });
})();
```

```js
[1, 2].join(undefined);
```

```js
Array.isArray({__proto__: Array.prototype });
```

```js
(function() {
  return Array(5).join(',').length;
})();
```

**[Back to top](#table-of-contents)**

### Date

```js
var date = new Date('2016/12/31');
date == '2016/12/31';
```

**[Back to top](#table-of-contents)**

### RegExp

```js
var smth = /()/;
```

```js
/^.$/.test('');
/^..$/.test('');
```

```js
RegExp.prototype.toString = function() { return this.source };

/3/-/2/;
```

```js
'ab'.split(/a*?/);
```

```js
'ab'.split(/(?:ab)*/);
```

```js
'ab'.split(/a*/);
```

```js
'.'.split(/(.?)(.?)/);
```

```js
'.'.split(/()()/);
```

```js
''.split(/.?/);
```

```js
'test'.split(/(?:)/, -1);
```

```js
typeof (/()??/).exec('')[1];
```

```js
var x1 = /[/ + 'javascript'[0] + '///';
x1;

var x2 = /\[/ + 'javascript'[0] + '///';
x2;
```

**[Back to top](#table-of-contents)**

### String

```js
'' instanceof String == '';
```

```js
new String('foo') === 'foo';
```

```js
'foo' == new function() { return String('foo') };
```

```js
'Hello'[-1] == 'Hello'.charAt(-1);
```

```js
var s1 = new String('hello');
var s2 = new String('hello');

s1 == s2;
s1 === s2;
```

```js
'Hello'.charAt(1) === 'Hello'.substring(1, 2);
```

**[Back to top](#table-of-contents)**

### Number

```js
3 instanceof Number;
```

```js
(123).toString();
```

```js
Number(5) === 5 || new Number(5) === Number(5);
```

```js
Number(undefined);
```

```js
new Number() instanceof Object;
```

```js
Number.isNaN('NaN') === window.isNaN('NaN');
```

```js
Number.prototype.x = function() { return this === 123 };
Number(123).x();
```

```js
Number.prototype.toString = function() {
  return typeof this;
};

(4).toString(); // => ?
```

**[Back to top](#table-of-contents)**

### Boolean

```js
Boolean('true') === true;
```

```js
var a = '';
new Boolean(a).valueOf();
```

```js
if (new Boolean(false)) {
  console.log('I love this wonderful language!');
};
```

**[Back to top](#table-of-contents)**

### Arguments

```js
var myArray = [1,2,3];

function setNull(param) {
  param = null;
};

setNull(myArray);

myArray; // => ?
```

```js
(function() {
  return typeof arguments;
})();
```

```js
(function() {
  return arguments.toString();
})();
```

```js
function bar(x, y, z) {
  arguments[2] = 10;
  return z;
};

bar(1, 2, 3);
```

```js
(() => arguments.toString())();
```

```js
function foo(a, b) {
  arguments[2] = 5;
  return b;
};

foo(1);
```

```js
var baz = function() {
  return arguments;
};

baz() == baz();
```

```js
[].slice.call((function() {
  return arguments
})(9, 8, 7), -2);
```

**[Back to top](#table-of-contents)**

### Math

```js
(1.22e-10).toFixed(2);
```

```js
Math.max(2, []);
```

```js
Math.pow(+0, -1);
```

```js
Math.round(true + .501);
```

```js
Math.pow(2, 53) === Math.pow(2, 53) + 1;
```

```js
Math.max({}, 2);
```

```js
Math.round(-5.5);
```

```js
Math.pow(-0, -1);
```

```js
Math.ceil(5.01) === -Math.floor(-5.01); // => ?
```

```js
Math instanceof Math;
```

```js
// what does it do ?
function whatDoesItDo(num) {
  return Math.max(0, Math.min(10, num));
};
```

**[Back to top](#table-of-contents)**

### Miscellaneous

```js
8 | 1; // => ?
```

```js
(() => void (1 + 1))();
```

```js
(function() {
  'use strict';
  return this || (1, eval)('this');
})();
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
var foo = { bar: 'baz' && 'foobarbaz' }; with (foo) var bar = eval('bar, 24');
foo;
```

```js
(![]+[])[+[]]+(![]+[])[+!+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]];
```

```js
(function pewpew(Infinity, length, __proto__) {
  return [,,~0.[0|0]][pewpew.__proto__.length && Infinity, -~String(this).length >> __proto__] << (0. === .0) + Infinity;
}).apply(typeof pewpew, [,,2]);
```

**[Back to top](#table-of-contents)**
