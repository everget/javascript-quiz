## JavaScript Quiz
The simple test for JavaScript developers:)

## Table of Contents
1. [Labels & Blocks](#labels--blocks)
1. [Semicolons](#semicolons)
1. [Coercions](#coercions)
1. [Comparisons](#comparisons)
1. [Inequalities](#inequalities)
1. [Calculus](#calculus)
1. [Conditional statements](#conditional-statements)
1. [Destructuring assignment](#destructuring-assignment)
1. [```typeof``` operator](#typeof-operator)
1. [```,``` operator](#comma-operator)
1. [```try-catch``` statement](#try-catch-statement)
1. [Hoisting](#hoisting)
1. [Scopes & Closures & Hoisting](#scopes--closures--hoisting)
1. [Context](#context)
1. [```delete``` operator](#delete-operator)
1. [```...``` operator](#spread-operator)
1. [```void``` operator](#void-operator)
1. [```instanceof``` operator](#instanceof-operator)
1. [Template literals](#template-literals)
1. [```Object```](#object)
1. [```Function```](#function)
1. [Default parameters](#default-parameters)
1. [```arguments```](#arguments)
1. [```class```](#class)
1. [```GeneratorFunction```](#generator-function)
1. [```Promise```](#promise)
1. [```AsyncFunction```](#async-function)
1. [```Reflect```](#reflect)
1. [```Proxy```](#proxy)
1. [```Array```](#array)
1. [```Date```](#date)
1. [```RegExp```](#regexp)
1. [```Symbol```](#symbol)
1. [```String```](#string)
1. [```Number```](#number)
1. [```Boolean```](#boolean)
1. [```Math```](#math)
1. [```Window```](#window)
1. [Event loop](#event-loop)
1. [```eval``` method](#eval-method)
1. [```with``` operator](#with-operator)
1. [Miscellaneous](#miscellaneous)

### Labels & Blocks

```js
vars: var vars = vars;

vars;
```

```js
foo: { foo = 123 };

foo;
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
a: b: c: d: e: f: g: 1, 2, 3, 4, 5;
```

```js
(printing => {
  printing: {
     console.log(1);
     if (!printing) {
       break printing;
     }
     console.log(2);
  };
  console.log(3);
})(false);
```

**[Back to top](#table-of-contents)**

### Semicolons

```js
var foo = [] // Missing semicolon!
(new Date).getTime();
```

```js
!function(){console.log('awesome');}() // Missing semicolon!
!function(){console.log('language');}();
```

```js
var [foo, bar, baz] = [1, 2, 3];

foo = bar // Missing semicolon!
++baz

[foo, bar, baz];
```

```js
function foo() {
  return // Missing semicolon!
      'Some string';
}

foo() === 'Some string';
```

```js
var bar = 'bar' // Missing semicolon!
/js/g.exec('awesome js!');
```

**[Back to top](#table-of-contents)**

### Coercions

```js
!!~1;
```

```js
false % 1;
```

```js
1 / '';
```

```js
+'  -12';
```

```js
+'1 2';
```

```js
'1' - - '1';
```

```js
'5' + + '6';
```

```js
'1' + 2 + '3' + 4;
```

```js
'a' + + 'b';
```

```js
4 - '5' + 0xf - '1e1';
```

```js
!!!function() {};
```

```js
4 + 3 + 2 + '1';
```

```js
[1] + 1;
```

```js
[] + 24 + 10;
```

```js
'foo'.split('') + [];
```

```js
[] + [] + 'foo'.split('');
```

```js
[1, 2] + [3, 4];
```

```js
[1, 2, [3, 4]] + [[5, 6], 7, 8];
```

```js
[4] * [4];
```

```js
({} + {});
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
[] + null + 1;
```

```js
[4, 4] * [4, 4];
```

```js
[3 + NaN + true] + [10 / (8 * null) - 1];
```

**[Back to top](#table-of-contents)**

### Comparisons

```js
'3' - 2 === 1;
```

```js
undefined == false;
```

```js
[1] == true;
```

```js
var a = true;
var b = false;

a != b === !(a == b);
```

```js
1 + 2 + '3' == 1 + '2' + 3;
```

```js
'001' == true;
```

```js
[2] == true;
```

```js
'00' == 0;
```

```js
[true] == true;
```

```js
0 === -0;
```

```js
null == 0;
```

```js
[1, 1] == true;
```

```js
' \t\r\n' == 0;
```

```js
'0x0' == false;
```

```js
[[[[1]]]] == true;
```

```js
'002' == true;
```

```js
[] == ![];
```

**[Back to top](#table-of-contents)**

### Inequalities

```js
10 > 9 > 8;
```

```js
9 < 5 < 1;
```

```js
2 < 6 < 1;
```

```js
1 < 3 < 4;
```

```js
'10' < '9';
```

```js
+0 < -0;
```

```js
'3' > '12'
```

```js
'03' > '12';
```

```js
Infinity > -Infinity;
```

```js
({} + 'b' > {} + 'a');
```

**[Back to top](#table-of-contents)**

### Calculus

```js
0.3 - 0.1;
```

```js
0.1 * 0.2;
```

```js
.1 + .2 != .3;
```

```js
0.1 + (0.2 + 0.3) == (0.1 + 0.2) + 0.3;
```

```js
(0.2 + 0.4) / 1 == (0.1 + 0.2) * 2;
```

```js
-9 % 7;
```

```js
42 / -0;
```

```js
var
  num1 = 5,
  num2 = 10,
  num3 = num1+++num2;

`${num1} ${num2} ${num3}`;
```

```js
var c = 0;

[c+++c++, c];
```

```js
1 + - + + + - + 1;
```

```js
01 - + - 02 - + - 03;
```

```js
8 | 1;
```

```js
~~(-5.5);
```

```js
~~+'2.9'-1 == ('2.9' >> 0) - 1;
```

```js
(1.22e-10).toFixed(2);
```

```js
12..toFixed(1);
```

```js
(0.9).toFixed(0);
```

```js
(0.00008).toFixed(3) === 0;
```

```js
parseInt(1 / 0, 19);
```

```js
parseInt(null, 24) === 23;
```

```js
parseInt(null);
```

```js
parseInt(Infinity);
```

```js
parseFloat('12.3.4');
```

```js
parseFloat('\t\v\r12.34\n ');
```

```js
1 / parseFloat('-.00');
```

**[Back to top](#table-of-contents)**

### Conditional statements

```js
('false') && ('bar');
```

```js
1 || 'foo' && 0;
```

```js
1 && 3;
```

```js
1 && 'foo' || 0;
```

```js
var a, b;
a = (b = 0) && (b = 1);

[a, b];
```

```js
var a = 1;
if (false)
    a = 3;
    a = 4;

a;
```

```js
var foo = NaN;
switch (foo) {
  case NaN:
    console.log('Hello, NaN!');
    break;
  default:
    console.log('Hello, default!');
}
```

```js
var foo = {};
switch (foo) {
  case {}:
    console.log('Hello, object!');
    break;
  default:
    console.log('Hello, default!');
}
```

**[Back to top](#table-of-contents)**

### Destructuring assignment

```js
var [a] = [];
a;
```

```js
var [b = 1] = [];
b;
```

```js
var [title, title, title, title] = 'JavaScript is awesome language'.split(' ');
title;
```

```js
({ a, b } = { a: 5, b: 6, a: 7 });
```

```js
var { total, tax } = { total: total, tax: tax };

[total, tax];
```

```js
var a, { a: b = 1 } = { a };

[a, b];
```

**[Back to top](#table-of-contents)**

### typeof operator

```js
typeof (null && false);
```

```js
typeof 000;
```

```js
typeof { null: null }.null;
```

```js
typeof setTimeout(() => {}, 0);
```

```js
typeof typeof undefined;
```

```js
var b = 1, a = b = typeof a;
a;
```

```js
var a = [typeof a, typeof b][1];
typeof typeof a;
```

**[Back to top](#table-of-contents)**

### Comma operator

```js
(1, 2, 3);
```

```js
var a = 0;
var b = (a++, 99);

[a, b];
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
(1,5 - 1) * 2;
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
} else {
  console.log('dreadful js');
}
```

```js
alert('2',
  foo = (arg) => alert(arg),
  foo('1')
),
foo('3');
```

**[Back to top](#table-of-contents)**

### try catch statement

```js
function foo() {
  try {
    return 'return';
  } finally {
    console.log('finally');
  }
}

foo();
```

```js
try {
  setTimeout(function() {
    throw new Error()
  }, 1000);
} catch (err) {}
```

```js
try {
  try {
    throw new Error('oops');
  }
  catch (err) {
    console.error('inner', err.message);
    throw err;
  }
  finally {
    console.log('finally');
    return;
  }
} catch (err) {
  console.error('outer', err.message);
}
```

**[Back to top](#table-of-contents)**

### Hoisting

```js
(function() {
   console.log(a);
   console.log(bar());

   var a = 1;
   function bar() {
      return 2;
   }
})();
```

```js
function foo(a) {
  return a * 2;
}

var foo;

typeof foo;
```

**[Back to top](#table-of-contents)**

### Scopes & Closures & Hoisting

```js
var b = 1;
{
  var b = 2;
}

b;
```

```js
if (!('a' in window)) {
  var a = 1;
}

a;
```

```js
var foo = 1;
function bar() {
  foo = 10;
  return;
  function foo() {};
}

bar();
foo;
```

```js
var foo = function bar() {
  return 23;
}

typeof bar();
```

```js
a = 1;
(() => {
  return a;
  var a = 2;
})();
```

```js
var a = 1;
if (function f() {}) {
  a += typeof f;
}

a;
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
}
```

```js
var foo = 11;

function bar() {
  return foo;
  foo = 10;
  function foo() {};
  var foo = '12';
}

typeof bar();
```

```js
var foo = 1,
var bar = function foo(a) {
  a && foo(--a);
};

foo;
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

### Context

```js
function f() {
  alert(this);
}

f.call(null);
```

```js
function f() {
  return this;
}

f.call(f);
```

```js
var foo = {
  bar() { return this }
};

(foo.bar)();
```

```js
var foo = {
  bar() { return this.baz },
  baz: 1
};

typeof (f = foo.bar)();
```

```js
(function() {
  'use strict'

  var a = 10;
  var foo = {
    a: 20,
    bar() {
      var a = 30;
      return this.a;
    }
  };

  return [
    foo.bar(),
    (foo.bar)(),
    (foo.bar = foo.bar)(),
    (foo.bar, foo.bar)(),
    (foo.baz || foo.bar)()
  ];

})();
```

```js
var foo = {
  bar: function() { return this === foo },
  baz: () => this === foo
};

foo.bar() === foo.baz();
```

```js
var foo = {
  message: 'Hello',
  innerMessage: !(function() {
    console.log(this.message);
  })()
};

foo.innerMessage;
```

```js
function f() {
  var a = 5;
  return new Function('b', 'return a + b');
}

f()(1);
```

```js
(function() {
  'use strict';

  const globalOne = (function() { return this || (1, eval)('this') })();

  const globalTwo = (function() { return this })();

  return globalOne === globalTwo;
}());
```

**[Back to top](#table-of-contents)**

### delete operator

```js
var numbers = [2, 3, 5, 7, 11, 13];
delete numbers[3];

numbers.length;
```

```js
delete [].length;
```

```js
function foo() {};
delete foo.length;

typeof foo.length;
```

```js
var Person = function() {};
Person.prototype.type = 'person';

var admin = new Person();
delete admin.type;

admin.type;
```

```js
delete delete window.document;
```

```js
(function() {
  a = 1;
  window.b = 2;
  this.c = 3;
  var d = 4;

  delete a;
  delete b;
  delete c;
  delete d;

  return [typeof a, typeof b, typeof c, typeof d];
})();
```

```js
(function (a) {
  delete a;
  return a;
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

### Spread operator

```js
[...[...'...']].length
```

```js
var foo = [...[,,24]];

[0 in foo, 1 in foo, 2 in foo];
```

**[Back to top](#table-of-contents)**

### void operator

```js
(() => void (1 + 1))();
```

```js
void function() { return 'tada'; }()
```

**[Back to top](#table-of-contents)**

### instanceof operator

```js
function A() {};
function B() {};

A.prototype = B.prototype = {};

var a = new A();

a instanceof B;
```

```js
function Rabbit() {};
var rabbit = new Rabbit();

Rabbit.prototype = {};

rabbit instanceof Rabbit;
```

```js
function Animal() {};

function Rabbit() {};
Rabbit.prototype = Object.create(Animal.prototype);

var rabbit = new Rabbit();

rabbit instanceof Animal;
rabbit instanceof Object;
```

```js
function f() { return f; }

new f() instanceof f;
```

**[Back to top](#table-of-contents)**

### Template literals

```js
`use strict`;

this == null;
```

```js
typeof `${{Object}}`.prototype
```

```js
((...args) => args)``
```

```js
concat`this``is``a``test``!`();
```

```js
var foo = { `hello world`: 24 };
```

```js
var { `hello world`: a } = { 'hello world': 24 };
```

**[Back to top](#table-of-contents)**

### Object

```js
Object instanceof Function;
```

```js
Object.prototype.toString.call();
```

```js
Object.prototype.toString.call(Object);
```

```js
var proto = {
  foo: () => 'foo'
}

var obj1 = new Object(proto);
var obj2 = new Object(proto);

obj1 === obj2;
```

```js
Object.is(NaN, NaN);
```

```js
Object.is(-0, +0);
```

```js
Object.assign({ a: 1 }) == Object.assign({}, { a: 1 });
```

```js
Object.assign({}, 'function');
```

```js
Object.freeze(window);

var didItWork = true;

didItWork;
```

```js
Object.prototype.isPrototypeOf(window);
```

```js
({ 'toString': null }).propertyIsEnumerable('toString');
```

```js
{ a: 1, b: 2 }['b'];
```

```js
var obj = {
 '': ''
};

obj[''];
```

```js
var obj = {
  toString: () => '[object MyObject]',
  valueOf: () => 17
};

'object: ' + obj;
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

'hello'.someProperty;
```

```js
(function() {
  let foo = {};
  let bar = {};
  let map = {};

  map[foo] = 'foo';
  map[bar] = 'bar';

  return map[foo];
})();
```

```js
100['toString']['length'];
```

```js
{ valueOf: () => true } == '1.0e0';
```

```js
var a = 1;
var b = { toString: () => '1' };
var c = 1;

a + b + c;
```

**[Back to top](#table-of-contents)**

### Function

```js
typeof Function;
Function instanceof Function;
Function instanceof Object;
```

```js
typeof Function.prototype;
Function.prototype instanceof Function;
Function.prototype.isPrototypeOf(Function);
Function.prototype.prototype;
```

```js
Function.prototype === Function;
Function.prototype.constructor === Function;
```

```js
var getObj = () => { a: 1 };
getObj();
```

```js
var x = function() {};
var y = x.bind();

y.prototype;
```

```js
function add(x, y) {
  return x + y;
}

var plusOne = add.bind(undefined, 1);
plusOne();
```

```js
var a = () => this;
var b = function() { return this }.bind(this);

a() === b();
```

```js
function one() {};

var two = one.bind(this);

two.name;
```

```js
(function() {
  return (function (a, b) {}).length;
})();
```

```js
(function() {
  if (false) {
    let f = { g() => 1 };
  }

  return typeof f;
})()
```

```js
var x = 4;
var y = ['foo', 'bar'];
var z = { first: true };

function f(a, b, c) {
  a = 3;
  b.push('baz');
  b = ['baz'];
  c.first = false;
  c = true;
}

f(x, y, z);

[x, y, z.first];
```

```js
var x = 0;

function foo() {
  x++;
  this.x = x;
  return foo;
};

var bar = new new foo;

bar.x;
```

```js
var foo = Function.prototype.call;

foo();
```

**[Back to top](#table-of-contents)**

### Default parameters

```js
function foo(a = 24, b = 10) {
  return a + b;
}

foo(undefined, 20);
foo(null, null);
```

```js
function bar(x, y = 24, z = 10) {
  return x + y + z;
}

bar(1,,2);
```

**[Back to top](#table-of-contents)**

### arguments

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
(function() {
  console.log(
    arguments.constructor === {}.constructor,
    arguments.constructor === [].constructor
  );
})();
```

```js
(function() {
  var arguments;
  return arguments[0];
})(200);
```

```js
function bar(x, y, z) {
  arguments[2] = 10;
  return z;
}

bar(1, 2, 3);
```

```js
(() => arguments.toString())();
```

```js
function foo(a, b) {
  arguments[2] = 5;
  return b;
}

foo(1);
```

```js 
var baz = function() {
  return arguments;
}

baz() == baz();
```

**[Back to top](#table-of-contents)**

### Class

```js
var Foo = class {};

class Foo {};
```

```js
class AwesomeJS extends null {};

new AwesomeJS;
```

```js
typeof (new (class F extends (String, Array) {})).substring;
```

```js
typeof (new (class { class () {} }));
```

```js
(function() {
  let f = this ? class g {} : class h {};
  return [
    typeof f,
    typeof h
  ];
})();
```

**[Back to top](#table-of-contents)**

### Generator function

**[Back to top](#table-of-contents)**

### Promise

```js
typeof Promise;
```

```js
typeof Promise.resolve(2410);
```

```js
new Promise((resolve, reject) => resolve(24))
  .then((res) => console.log(res))
  .then((res) => console.log(res));
```

```js
Promise.resolve('foo')
  .then(Promise.resolve('bar'))
  .then((res) => console.log(res));
```

```js
Promise.resolve('foo')
  .then((res) => Promise.resolve('bar'))
  .then((res) => console.log(res));
```

```js
Promise.resolve(2)
  .then(3)
  .then((res) => console.log(res));
```

```js
Promise.resolve({ a: 24 })
  .then((res) => delete res.a)
  .then((res) => console.log(res.a));
```

```js
Promise.resolve(2410).then(
  (res) => { throw new Error(res) },
  (err) => { try {} catch(err) {} }
);
```

```js
Promise.reject(24)
  .then(null, null)
  .then(null, (reason) => console.log(reason));

Promise.reject(24)
  .then(5, null)
  .then(null, (reason) => console.log(reason));

Promise.reject(24)
  .then(null, 5)
  .then(null, (reason) => console.log(reason));
```

```js
Promise.resolve(24)
  .then(null, null)
  .then((res) => console.log(res), null);

Promise.resolve(24)
  .then(null, 5)
  .then((res) => console.log(res), null);

Promise.resolve(24)
  .then(5, null)
  .then((res) => console.log(res), null);
```

**[Back to top](#table-of-contents)**

### Async function

```js
async fn() {};

Object.prototype.toString.call(fn);
```

**[Back to top](#table-of-contents)**

### Reflect

**[Back to top](#table-of-contents)**

### Proxy

**[Back to top](#table-of-contents)**

### Array

```js
typeof [1, 2, 3];
```

```js
var arr = [];

arr instanceof Array;
arr instanceof Object;
```

```js
[,].length;
```

```js
[,,].length;
```

```js
[[[1], 2], 3].length;
```

```js
var arr = [];

arr[1] = 1;
arr[24] = 24;

arr.length;
```

```js
new Array(null);
```

```js
new Array(1)[0] + '';
```

```js
var arr = new Array('100');

arr.length;
```

```js
new Array(1, 2) == true;
```

```js
new Array([], null, undefined, null) == ',,,';
```

```js
[1, 2, 3].toString();
```

```js
[1, 2, 3, 4, 5][0..toString().length];
```

```js
[].unshift(0);
```

```js
var arr = [2, 3, 5, 7, 11];

arr.indexOf(7, 2);
arr.indexOf(2, -3);
```

```js
[NaN].indexOf(NaN);
```

```js
'0'.split(void 0, 0);
```

```js
Array(2).join();
```

```js
[1, 2].join(undefined);
```

```js
Array(4).join('tada!' - 4);
```

```js
(function() {
  return Array(5).join(',').length;
})();
```

```js
[].concat[1, 2, 3];
```

```js
[].fill.call({ length: 3 }, 4);
```

```js
Array.from({ '': '' });
```

```js
[NaN].includes(NaN);
```

```js
var arr = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

arr.slice();
arr.slice(-2);
arr.slice(3, -6);
```

```js
(function() {
  return Array(3).map(item => 'a');
})();
```

```js
Array.isArray({
  constructor: Array,
  length: 0,
  __proto__: Array.prototype
});
```

**[Back to top](#table-of-contents)**

### Date

```js
'2016/12/31' == new Date('2016/12/31');
```

```js
new Date(-666).getUTCMonth();
```

```js
new Date(0) - 0;
```

```js
new Date(0);
```

```js
new Date('0');
```

```js
new Date(0, 0);
```

```js
new Date(0, 0, 0);
```

**[Back to top](#table-of-contents)**

### RegExp

```js
/^.$/.test('');
/^..$/.test('');
```

```js
RegExp.prototype.toString = function() {
  return this.source;
}

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

### Symbol

```js
typeof Symbol;
```

```js
var foo = new Symbol();
```

```js
Symbol('foo') === Symbol('foo');
```

```js
class MySymbol extends Symbol {
  constructor() {
    super();
  }
}

var symbol = new MySymbol();
```

```js
Symbol.for('bar') === Symbol.for('bar');
```

**[Back to top](#table-of-contents)**

### String

```js
String(1.23e+2);
```

```js
String(['awesome', 'js']);
```

```js
'' instanceof String;
```

```js
'foo' == new function() { return String('foo') };
```

```js
'Hello'[-1] == 'Hello'.charAt(-1);
```

```js
new String('hello') == new String('hello');
```

```js
'Hello'.charAt(1) === 'Hello'.substring(1, 2);
```

```js
++'24'.split('')[0];
```

**[Back to top](#table-of-contents)**

### Number

```js
3 instanceof Number;
```

```js
new Number() instanceof Object;
```

```js
Number([]);
```

```js
Number([24, 10]);
```

```js
Number(undefined);
```

```js
Number({});
```

```js
Number(['awesome', 'js']);
```

```js
Number.isNaN('NaN') === window.isNaN('NaN');
```

```js
Number.prototype.compare = function(value) {
  return this === value;
}

Number(123).compare(123);
```

```js
Number.prototype.toString = function() {
  return typeof this;
}

(4).toString();
```

**[Back to top](#table-of-contents)**

### Boolean

```js
Boolean('true') === true;
```

```js
Boolean([]);
```

```js
Boolean('000');
```

```js
Boolean(-Infinity);
```

```js
if (new Boolean(false)) {
  console.log('JS');
}
```

```js
new Boolean('').valueOf();
```

```js
new Boolean(false).valueOf() === false;
```

**[Back to top](#table-of-contents)**

### Math

```js
Math instanceof Math;
```

```js
Math.round(true + .501);
```
```js
Math.round(-5.5);
```

```js
Math.ceil(5.01) === -Math.floor(-5.01);
```

```js
Math.max(2, []);
```

```js
Math.max({}, 2);
```

```js
Math.pow(+0, -1);
```

```js
Math.pow(2, 53) === Math.pow(2, 53) + 1;
```

```js
Math.pow(-0, -1);
```

**[Back to top](#table-of-contents)**

### Window

```js
typeof window;
typeof Window;
```

```js
Object.getPrototypeOf(window) === Window;
```

```js
Window.constructor === Function;
```

```js
Window.prototype.constructor === Window;
```

**[Back to top](#table-of-contents)**

### Event loop

```js
setTimeout(() => console.log(1), 1);
setTimeout(() => console.log(2), 1000);
setTimeout(() => console.log(3), 0);
console.log(4);
```

```js
setTimeout(() => {
  console.log(1);
  setTimeout(() => console.log(2), 0);
}, 500);

setTimeout(() => {
  setTimeout(() => console.log(3), 500);
}, 250);
```

```js
setTimeout(() => {
  console.log(1);
}, 300);

Promise.resolve()
  .then(() => console.log(2));

console.log(3);
```

```js
setTimeout(() => {
  console.log(1);
}, 0);

Promise.resolve(2)
  .then((res) => {
    console.log(res);
    setTimeout(() => {
      console.log(3);
    }, 0);
    return Promise.resolve(4);
  })
  .then((res) => {
    console.log(res);
  });
```

```js
setTimeout(() => {
  console.log(1);
}, 1000);

process.nextTick(() => {
  console.log(2);
});

console.log(3);
```

```js
process.nextTick(() => {
  console.log(1);
  while (true) {}
});

process.nextTick(() => {
  console.log(2);
});
```

**[Back to top](#table-of-contents)**

### eval method

```js
function foo() {
  return eval.bind(null, '(function() { return bar; })');
}

var bar = 1;

(function() {
  var bar = 2;
  foo()()();
})();
```

```js
function foo() {
  return '(function() { return bar; })';
}

var bar = 1;

(function() {
  var bar = 2;
  eval(foo())();
})();
```

**[Back to top](#table-of-contents)**

### with operator

```js
var a = 1;

var obj = {
  b: 2
};

with (obj) {
  var b;
  console.log(a + b);
}
```

```js
with ({ a: 1 }) {
  a = 2,
  b = 3
}

[window.a, window.b];
```

```js
with (function (x, undefined) {}) {
  length;
}
```

```js
({
  x: 10,
  foo() {
    function bar() {
      console.log(x);      // => ?
      console.log(y);      // => ?
      console.log(this.x); // => ?
    }

    with (this) {
      var x = 20;
      var y = 30;
      bar.call(this);
    }
  }
}).foo();
```

```js
var foo = { bar: 'baz' && 'foobarbaz' };
with (foo) var bar = eval('bar, 24');

foo.bar;
```

**[Back to top](#table-of-contents)**

### Miscellaneous

```js
(![]+[])[+[]]+(![]+[])[+!+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]];
```

```js
(function pewpew(Infinity, length, __proto__) {

  return [,,~0.[0|0]][pewpew.__proto__.length && Infinity,
                      -~String(this).length >> __proto__] << (0. === .0) + Infinity;

}).apply(typeof pewpew, [,,2]);
```

**[Back to top](#table-of-contents)**
