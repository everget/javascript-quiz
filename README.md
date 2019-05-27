## JavaScript Quiz

## Table of Contents
1. [Labels](#labels)
1. [Semicolons](#semicolons)
1. [Coercions](#coercions)
1. [Comparisons](#comparisons)
1. [Inequalities](#inequalities)
1. [Calculus](#calculus)
1. [Conditional statements](#conditional-statements)
1. [Destructuring assignment](#destructuring-assignment)
1. [```void``` operator](#void-operator)
1. [```typeof``` operator](#typeof-operator)
1. [```,``` operator](#comma-operator)
1. [```try-catch``` statement](#try-catch-statement)
1. [Hoisting](#hoisting)
1. [Scopes & Closures & Hoisting](#scopes--closures--hoisting)
1. [Context](#context)
1. [```delete``` operator](#delete-operator)
1. [```...``` operator](#spread-operator)
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

### Labels

```js
vars: var vars = vars;

vars;
```

```js
foo: { foo = 123 };

foo;
```

```js
var foo = {};
var bar = 1;

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
!function(){console.log('Awesome');}() // Missing semicolon!
!function(){console.log('JS');}();
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
      'Awesome JS';
}

foo() === 'Awesome JS';
```

```js
var bar = 'bar' // Missing semicolon!
/JS/g.exec('Awesome JS');
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
+'1'++;
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
'foo' + + 'bar';
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
++[];
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

```js
[][[]];
```

```js
[[]][0];
```

```js
++[[]][+[]];
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
var x = true;
var y = false;

x != y === !(x == y);
```

```js
!!'false' ==  !!'true';
!!'false' === !!'true';
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

```js
[[]] == 0;
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
+0 < -0;
```

```js
01 < 1;
```

```js
0,0000008 < 8;
```

```js
[10] < [2];
```

```js
'10' < '9';
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
({} + 'y' > {} + 'x');
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
9999999999999999 === 1e16;
```

```js
1e16 === 1e16 + 1;
```

```js
1e16 + 1.1 < 1e16 + 2;
```

```js
var x = 5;
var y = 10;
var z = x+++y;

[x, y, z];
```

```js
var x = 0;

[x+++x++, x];
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
parseInt('08');
```

```js
parseInt(null);
```

```js
parseInt(null, 24);
```

```js
parseInt(Infinity);
```

```js
parseInt(1 / 0, 19);
```

```js
parseInt('Infinity', 23)
```

```js
parseFloat('12.3.4');
```

```js
parseFloat('\t\v\r12.34\n ');
```

```js
parseFloat('-.00');
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
var x, y;
x = (y = 0) && (y = 1);

[x, y];
```

```js
var x = 1;
if (false)
    x = 3;
    x = 4;

x;
```

```js
var foo = NaN;
switch (foo) {
  case NaN:
    console.log('NaN');
    break;
  default:
    console.log('default');
}
```

```js
var foo = {};
switch (foo) {
  case {}:
    console.log('object');
    break;
  default:
    console.log('default');
}
```

**[Back to top](#table-of-contents)**

### Destructuring assignment

```js
var [x] = [];
x;
```

```js
var [x = 1] = [];
x;
```

```js
var [x, x, x, x] = 'JS is awesome language'.split(' ');
x;
```

```js
({ x, y } = { x: 5, y: 6, x: 7 });
```

```js
var { x, y } = { x: x, y: y };

[x, y];
```

```js
var x, { x: y = 1 } = { x };

[x, y];
```

```js
var o1 = { a: 1 },
    o2 = { b: 2 },
    o3 = { c: 3 }

[o1, o2, o3] = [o3, o2, o1];

o3;
```

**[Back to top](#table-of-contents)**

### void operator

```js
(() => void (1 + 1))();
```

```js
void function() { return 'foo'; }();
```

**[Back to top](#table-of-contents)**

### typeof operator

```js
typeof 000;
```

```js
typeof (null && false);
```

```js
typeof (void null);
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
var y = 1, x = y = typeof x;
x;
```

```js
var x = [typeof x, typeof y][1];
typeof typeof x;
```

**[Back to top](#table-of-contents)**

### Comma operator

```js
(1, 2, 3);
```

```js
var x = 0;
var y = (x++, 99);

[x, y];
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
typeof ('x', 3);
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
  console.log('if');
} else {
  console.log('else');
}
```

```js
alert('2',
  foo = (x) => alert(x),
  foo('1')
),
foo('3');
```

**[Back to top](#table-of-contents)**

### try catch statement

```js
(() => {
  try {
    return 'try';
  } finally {
    console.log('finally');
  }
})();
```

```js
var foo = () => {
  var o = { foo: 24 };
  window.bar = () => {
    return o;
  };

  try {
    return o;
  } finally {
    o = null;
  }
};

foo(); // => ?
bar(); // => ?
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
    throw new Error('try');
  } catch (err) {
    console.error('inner', err.message);
    throw err;
  } finally {
    console.log('finally');
  }
} catch (err) {
  console.error('outer', err.message);
}
```

```js
(() => {
  label: try {
    return 0;
  } finally {
    break label;
    return 1;
  }
  return 2;
})();
```

```js
(() => {
  try {
      throw new Error('try')
  } catch (err) {
      throw err;
  } finally {
      throw new Error('finally');
  }
})();
```

**[Back to top](#table-of-contents)**

### Hoisting

```js
var bar;
f();

function f() {
  return bar;
}

var bar = 2410;
```

```js
(function() {
   console.log(x);
   console.log(f());

   var x = 1;
   function f() {
      return 2;
   }
})();
```

```js
function f(x) {
  return x * 2;
}

var f;

typeof f;
```

**[Back to top](#table-of-contents)**

### Scopes & Closures & Hoisting

```js
var x = 1;
{
  var x = 2;
}

x;
```

```js
if (!('y' in window)) {
  var y = 1;
}

y;
```

```js
(function() {
  var x = x = 3;
})();

[typeof x, typeof y];
```

```js
var foo = function bar() {
  return 'bar';
}

typeof bar();
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
x = 1;
(() => {
  return x;
  var x = 2;
})();
```

```js
var x = 1;
if (function f() {}) {
  x += typeof f;
}

x;
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
var bar = function foo(x) {
  x && foo(--x);
};

foo;
```

```js
(function() {
  var foo = 'x';

  (function (foo) {
    foo = 'y';
  })(foo);

  return foo;
})();
```

```js
(function f(f) {
  return typeof f();
})(() => 1);
```

```js
function f() {
  var x = 5;
  return new Function('y', 'return x + y');
}

f()(1);
```

```js
var x = 1;

function f() {
  var x = 2;
  return new Function('', 'return x');
}

f()();
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
(function() {

  var f = function() {
    return this * 2;
  };

  return [
    f.call(undefined),
    f.call(null),
    f.call(1)
  ];

})();
```

```js
var user = {
  name: 'Alex',
  _user: this
};

user._user.name;
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

  var x = 10;
  var foo = {
    x: 20,
    bar() {
      var x = 30;
      return this.x;
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
  bar: 'bar',
  baz: !(function() {
    console.log(this.bar);
  })()
};

foo.baz;
```

```js
(function() {
  'use strict';

  const g1 = (function() { return this || (1, eval)('this') })();
  const g2 = (function() { return this })();

  return g1 === g2;
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
  x = 1;
  window.y = 2;
  this.z = 3;
  var w = 4;

  delete x;
  delete y;
  delete z;
  delete w;

  return [typeof x, typeof y, typeof z, typeof w];
})();
```

```js
(x => {
  delete x;
  return x;
})(1);
```

```js
var x = 1;
y = 1;

(function() {
  return (delete window.x) === (delete window.y);
})();
```

```js
void typeof delete this;
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

### instanceof operator

```js
function A() {};
function B() {};

A.prototype = B.prototype = {};

var a = new A();

a instanceof B;
```

```js
function A() {};
var a = new A();

A.prototype = {};

a instanceof A;
```

```js
function A() {};

function B() {};
B.prototype = Object.create(A.prototype);

var b = new B();

b instanceof A;
```

```js
function f() { return f; }

new f() instanceof f;
```

**[Back to top](#table-of-contents)**

### Template literals

```js
`${1.0}`;
```

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
var foo = { `hello world`: 24 };
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
Object.is(NaN, NaN);
```

```js
Object.is(-0, +0);
```

```js
Object.assign({}, 'function');
```

```js
var foo = 'abc';
var bar = Object(foo);

Object.prototype.toString.call(bar);
```

```js
Object.freeze(window);

var didItWork = true;

didItWork;
```

```js
({ 'toString': null }).propertyIsEnumerable('toString');
```

```js
{ x: 1, y: 2 }['x'];
```

```js
var obj = {
 '': ''
};

obj[''];
```

```js
{ [{}]: {} };
```

```js
var obj = {
  1: 'foo'
};

obj[1] == obj[[1]];
obj[[1]] == obj['1'];
```

```js
'foo'.someProperty = 17;

'foo'.someProperty;
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
100['toString']['length'];
```

```js
({}).valueOf();
```

```js
{ valueOf: () => true } == '1.0e0';
```

```js
var foo = {
  toString: () => '[object Foo]',
  valueOf: () => 2410
};

'object: ' + foo;
```

```js
var x = 1;
var y = { toString: () => '1' };
var z = 1;

x + y + z;
```

```js
var foo = { x: 1 };
foo.y = foo = { x: 2 };

foo.y;
```

```js
var t = true;
var obj = ({[t]: t});

obj;
```

```js
var t = true;
var obj = ({[`${t}`]: t, [t]: t});

obj;
```

```js
('__proto__').__proto__.__proto__.__proto__;
```

```js
var proto = {
  x: () => 'x'
}

var foo = new Object(proto);
var bar = new Object(proto);

foo === bar;
```

```js
Object.create(null) instanceof Object;
```

```js
var bar = { bar: 'bar'};

function foo() {}
foo.prototype = bar;

[bar instanceof foo, Object.create(bar) instanceof foo];
```

```js
Object.prototype.isPrototypeOf(window);
```

```js
var foo = { __proto__: null };

Object.getPrototypeOf(foo) === null;
```

```js
var __proto__ = 'bar';
var foo = { __proto__ };

Object.getPrototypeOf(foo) === Object.prototype;
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
(function (x, y) {}).length;
```

```js
(function (foo) {
  return typeof foo.bar;
})({ foo: { bar: 1 } });
```

```js
var f = () => { x: 1 };
f();
```

```js
function f() {};

f.bind(this).name;
```

```js
var f = function() {};
var g = f.bind();

g.prototype;
```

```js
function f(x, y) {
  return x + y;
}

f.bind(1)();
```

```js
function f() {
  return this.value;
}

f.bind({ value: 1 }).call({ value: 2 });
```

```js
var f = () => this;
var g = function() { return this }.bind(this);

f() === g();
```

```js
function f() {}

var fBind = f.bind({});
var obj = new f();

[obj instanceof f, obj instanceof fBind];
```

```js
function foo() {
  return Function.bind(null, 'console.log(bar);');
}

var bar = 1;

(function() {
  var bar = 2;
  foo()()();
})();
```

```js
(function() {
  if (false) {
    let f = { g() => 1 };
  }

  return typeof f;
})();
```

```js
var foo = 2410;
var bar = ['a', 'b'];
var baz = { first: true };

function f(x, y, z) {
  x = 3;
  y.push('c');
  y = ['c'];
  z.first = false;
  z = true;
}

f(foo, bar, baz);

[foo, bar, baz.first];
```

```js
function f(name) {
  this.name = name;
}

var name = 'foo';
var person = f('bar');

[name, person];
```

```js
var x = 0;

function f() {
  x++;
  this.x = x;
  return f;
}

var foo = new new f;

foo.x;
```

```js
var c = 'constructor';

c[c][c]('console.log(c)')();
```

```js
var f = Function.prototype.call;

f();
```

```js
console.log.call.call.call.call.call.apply(x => x, [1, 2]);
```

**[Back to top](#table-of-contents)**

### Default parameters

```js
function f(x = 24, y = 10) {
  return x + y;
}

foo(undefined, 20);
foo(null, null);
```

```js
function g(x, y = 24, z = 10) {
  return x + y + z;
}

g(1,,2);
```

```js
var bar = 1;

function f(bar = bar) {
  return bar;
}

f();
```

```js
var x = 1;

function f(y = function() { return x; }) {
  var x = 2;
  return y();
}

f();
```

```js
function f(x, y = function() { return x; }) {
  console.log(x);
  var x = 1;
  console.log(y());
}

f(2);
```

```js
function f(x, y = function() { console.log(x); x = 1; }) {
  var x;
  console.log(x);
  x = 2;
  y();
  console.log(x);
}

f(3);
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
function f(x, y, z) {
  arguments[2] = 10;
  return z;
}

f(1, 2, 3);
```

```js
(() => arguments.toString())();
```

```js
function f(x, y) {
  arguments[2] = 5;
  return y;
}

f(1);
```

```js
function f(foo, bar, baz) {
  return Array.from(arguments);
}

f(...['foo', , 'bar']);
```

```js 
var g = function() {
  return arguments;
};

g() == g();
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

```js
class A {
  foo() {
    console.log('A.foo');
  }
}

class B extends A {
  foo() {
    super.foo();
  }
}

class C {
  foo() {
    console.log('C.foo');
  }
}

var D = {
  foo: B.prototype.foo,
};

Object.setPrototypeOf(B, C.constructor);

D.foo();
```

**[Back to top](#table-of-contents)**

### Generator function

```js
function* g() {
  yield 'foo';
}

g[Symbol.toStringTag] === g()[Symbol.toStringTag];
```

```js
function* g() {
  yield 'foo';
  yield yield 'bar';
  yield yield yield 'baz';
}

var gen = g();

[...gen];
```

```js
(function* f() { yield f })().next()
```

**[Back to top](#table-of-contents)**

### Promise

```js
typeof Promise.resolve(2410);
```

```js
Promise.reject(Promise.resolve());
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
Promise.resolve({ x: 24 })
  .then((res) => delete res.x)
  .then((res) => console.log(res.x));
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
```

```js
Promise.reject(24)
  .then(10, null)
  .then(null, (reason) => console.log(reason));
```

```js
Promise.reject(24)
  .then(null, 10)
  .then(null, (reason) => console.log(reason));
```

```js
Promise.resolve(24)
  .then(null, null)
  .then((res) => console.log(res), null);
```

```js
Promise.resolve(24)
  .then(null, 10)
  .then((res) => console.log(res), null);
```

```js
Promise.resolve(24)
  .then(10, null)
  .then((res) => console.log(res), null);
```

**[Back to top](#table-of-contents)**

### Async function

```js
async function f(x) {
  return x * x;
}

f(2) === 4;
```

```js
var y = 2;
async function f(x = await y) {
  return x * x;
}

f();
```

```js
(() => {
  'use strict';
  async function eval(x, y) {
    await x * y;
  }

  eval(1, 2);
})();
```

```js
async function f(x) {
  return await x * (await x);
}

f(2).then(res => console.log(res));
```

```js
async function User(firstname, lastname) {
  this.firstname = await firstname;
  this.lastname = await lastname;
}

var user = new User('John', 'Doe');
```

```js
(async function(){}).__proto__.__proto__ == (function(){}).__proto__;
```

**[Back to top](#table-of-contents)**

### Reflect

```js
Reflect.get(Reflect, Reflect.get(Reflect, 'get').name);
```

```js
Reflect.setPrototypeOf(Reflect, Array.prototype);

typeof Reflect.slice;
```

```js
Reflect.preventExtensions(Reflect);

Reflect.isExtensible(Reflect);
```

**[Back to top](#table-of-contents)**

### Proxy

```js
var proxy = new Proxy({}, {});

proxy instanceof Proxy;
```

```js
(() => {
  Proxy.prototype = null;

  class P extends Proxy {
    constructor() {
      super(window, {});
      this.foo = 'foo';
    }
  };

  new P;
  console.log(window.foo);
})();
```

```js
(() => {
  Proxy.prototype = null;

  class P extends Proxy {
    constructor() {
      super(window, {
        getPrototypeOf() { return P.prototype }
      });
    }
  };

  console.log((new P) instanceof P === true);
})();
```

**[Back to top](#table-of-contents)**

### Array

```js
[].valueOf();
```

```js
typeof [1, 2, 3];
```

```js
var arr = [];

arr[1] = 1;
arr[24] = 24;

arr.length;
```

```js
var arr = [];
var i = 3;

arr[--i] = ++i;

arr;
```

```js
[].length = -2;
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
new Array(null);
```

```js
new Array(1)[0] + '';
```

```js
new Array('100').length;
```

```js
new Array(1, 2) == true;
```

```js
new Array([], null, undefined, null) == ',,,';
```

```js
var arr = new Array(3);

arr.map((value, index) => index);
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
[,,,].join() === ',,';
```

```js
Array(4).join('js!' - 4);
```

```js
Array(5).join(',').length;
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
[1, 2, 3].slice(0, null);
```

```js
Array(3).map(item => 'x');
```

```js
Array.apply(null, new Array(4)).map((el, i) => i);
```

```js
Array.apply(null, { length : 3 });
```

```js
[...new Set([1, 1, 2, 3, 5, 8, 13])];
```

```js
var arr = [1, 2, 3];
var pushResult = arr.push(4, 5, 6);

[pushResult, arr];
```

```js
var arr = [undefined, , true];

arr.filter(() => true);
```

```js
var arr = new Array(2);
var i = 0;

arr.forEach(() => i++);

i;
```

```js
var arr = [80, 9, 34, 23, 5, 1];
arr.sort(); // => ?
```

```js
new Array(10).map((el, i) => i + 1);
```

```js
var bag = new Array(3).fill([]);
bag[0].push(1);
bag[1].push(1);
bag; // => ?
```

```js
Array.isArray({
  constructor: Array,
  length: 0,
  __proto__: Array.prototype,
});
```

```js
Array.prototype.push(1, 2, 3);
```

```js
Array.prototype[1] = 'foo';

var arr = [undefined, ,];

0 in arr; // => ?
1 in arr; // => ?
arr.hasOwnProperty(1); // => ?
```

**[Back to top](#table-of-contents)**

### Date

```js
new Date(undefined);
```

```js
new Date(null);
```

```js
'2016/12/31' == new Date('2016/12/31');
```

```js
typeof (new Date() + new Date());
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

```js
var f = Date.bind.call(Date, 2000, 0, 1);
var g = Function.bind.call(Date, null, 2000, 0, 1);

new f().toString() === new g().toString();
```

**[Back to top](#table-of-contents)**

### RegExp

```js
/[a-z]/ === /[a-z]/;
```

```js
RegExp.prototype.toString = function() {
  return this.source;
}

/3/3/ - /1/;
```

```js
(() => {
    class CustomRegExp extends RegExp {
      constructor() {
        super();
      }
    }

    return new CustomRegExp;
})();
```

```js
'foobar'.replace(/^/, "$'");
```

```js
/foo.bar/.test('foo\nbar');
```

```js
/^$/.test('');
```

```js
/$^/.test('');
```

```js
/^.$/.test('');
```

```js
/^..$/.test('');
```

```js
'xy'.split(/x*?/);
```

```js
'xy'.split(/(?:xy)*/);
```

```js
'xy'.split(/x*/);
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
/^$^$^$^$^$^$$$$^^^/.test('');
```

```js
new RegExp(/xy+z/, 'i');
```

```js
new RegExp([].join('|'));
```

```js
var foo = /[/ + 'javascript'[0] + '///';
foo;

var bar = /\[/ + 'javascript'[0] + '///';
bar;
```

**[Back to top](#table-of-contents)**

### Symbol

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

```js
Symbol.keyFor(Symbol.iterator);
```

```js
var obj = {
  [Symbol('foo')]: 'foo',
  [Symbol('bar')]: 'bar'
};

Object.keys(obj);
```

```js
var obj = {};

obj[Symbol('foo')] = true;

obj[Symbol('foo')] = false;

Object.getOwnPropertySymbols(obj).length;
```

**[Back to top](#table-of-contents)**

### String

```js
String(1.23e+2);
```

```js
String(['foo', 'bar']);
```

```js
'' instanceof String;
```

```js
'foo' == new function() { return String('foo') };
```

```js
'foo'[-1] == 'foo'.charAt(-1);
```

```js
'foo'.charAt(1) === 'foo'.substring(1, 2);
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
Number.MAX_VALUE > 0;
Number.MIN_VALUE > 0;
```

```js
Number();
```

```js
Number(undefined);
```

```js
Number('');
```

```js
Number([]);
```

```js
Number([24, 10]);
```

```js
Number({});
```

```js
Number.isNaN('NaN') === window.isNaN('NaN');
```

```js
Number('0.') === Number('.0');
```

```js
Number.prototype.compare = function(value) {
  return this === value;
};

Number(123).compare(123);
```

```js
Number.prototype.toString = function() {
  return typeof this;
};

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
  console.log('Awesome JS');
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
Math.max() > Math.min();
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

```js
(() => {
  console.log(window);
  var window = window;
})();
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
new Promise((resolve, reject) => {
  console.log(1);
  resolve();
}).then(() => {
  console.log(2);
});

console.log(3);
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
async function f() {
  console.log(await new Promise(resolve => {
     setTimeout(() => resolve(2), 0);
  }));
}

console.log(1);
f();
console.log(3);
```

```js
// Node.js
setTimeout(() => {
  console.log(1);
}, 1000);

process.nextTick(() => {
  console.log(2);
});

console.log(3);
```

```js
// Node.js
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
  foo()()(); // => ?
})();
```

```js
function foo() {
  return '(function() { return bar; })';
}

var bar = 1;

(function() {
  var bar = 2;
  eval(foo())(); // => ?
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
  console.log(a + b); // => ?
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
  length; // => ?
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
({[{}]:{[{}]:{}}})[{}][{}];
```

```js
(function pewpew(Infinity, length, __proto__) {

  return [,,~0.[0|0]][pewpew.__proto__.length && Infinity,
                      -~String(this).length >> __proto__] << (0. === .0) + Infinity;

}).apply(typeof pewpew, [,,2]);
```

**[Back to top](#table-of-contents)**
