# javascript-quiz
Simple:) test for javascript developers

``` js
/***********************************************/

{ foo: 'bar' } // .. ?

{ 'foo': 'bar' } // .. ?

({ 'foo': 'bar' }) // .. ?

/***********************************************/

"1" - - "1";

/***********************************************/

var a = []
(new Date).getTime()

/***********************************************/

{} === {};

/***********************************************/

  typeof (null && false);
  typeof (null && []);

/***********************************************/

  10 > 9 > 8 === true;

/***********************************************/

Object.prototype.toString.call();
Object.prototype.toString.call([]);
Object.prototype.toString.call({});
Object.prototype.toString.call(true);
Object.prototype.toString.call(null);

/***********************************************/

'1.0e0' == { valueOf: function () { return true; } };

/***********************************************/

  if ( !('a' in window) ) {
    var a = 1;
  }
  alert(a);

/***********************************************/

  var text = 'Hello JS';
  var calc = 2 * 2;
  alert(text.length + calc);

  var Up = text.toUpperCase();
  alert(Up > text);

  var Pi = calc + 3.141592;
  alert(Pi.toFixed(2));

/***********************************************/

  'foo'.split('') + []

/***********************************************/

  'foo' == new function (){ return String('foo'); };

/***********************************************/

  {break;4;}

/***********************************************/

  RegExp.prototype.toString = function () { return this.source };
  n/3/-/2/;

/***********************************************/

  delete [].length;

/***********************************************/

  x = 1; (function () {
    return x;
    var x = 2;
  }())

/***********************************************/

  { foo = 123 }

/***********************************************/

  vars: var vars = vars;

/***********************************************/

  Array(2).join();

/***********************************************/

  Number.prototype.x = function () { return this === 123; };
  n(123).x();

/***********************************************/

  ({} + 'b' > {} + 'a');

/***********************************************/

  [1,2,3,4,5][0..toString.length];

/***********************************************/

  (function (){}());

/***********************************************/

  { a: { b:2 } };

/***********************************************/

  { a: 1, b: 2 }[['b']];

/***********************************************/

  a: b: c: d: e: f: g: 1, 2, 3, 4, 5;

/***********************************************/

  ++'52'.split('')[0];

/***********************************************/

  [true, false][+true, +false];

/***********************************************/

  { foo:1 }[0];

/***********************************************/

  (1, 2, 3)

/***********************************************/

  function a(x) {
    return x * 2;
  }
  var a;
  alert(a);

/***********************************************/

  var x = 0;
  function foo() {
      x++;
      this.x = x;
      return foo;
  }
  var bar = new new foo;
  console.log(bar.x);

/***********************************************/

  var a = 1,
      b = function a(x) {
        x && a(--x);
      };
  alert(a);

/***********************************************/

  function foo(a, b) {
    arguments[1] = 2;
    alert(b);
  }
  foo(1);

/***********************************************/
  function b(x, y, a) {
    arguments[2] = 10;
    alert(a);
  }
  b(1, 2, 3);


/***********************************************/

  function a() {
    alert(this);
  }
  a.call(null);

/***********************************************/

  (function (){
    return typeof arguments;
  })();

/***********************************************/

  var f = function g() { return 23; }
      typeof g();

/***********************************************/

  (function (x) {
    delete x;
    return x;
  })(1); // 1

/***********************************************/

  var y = 1, x = y = typeof x;
  x;

/***********************************************/

  (function f(f) {
     return typeof f();
  })(function () { return 1; });

/***********************************************/

  var foo = {
    bar: function () { return this.baz; }
    baz: 1
  };

  (function () {
    return typeof arguments[0]();
  })(foo.bar);

/***********************************************/

  var foo = {
    bar: function () { return this.baz; }
    baz: 1
  };
  typeof  (f = foo.bar);

/***********************************************/

  var f = (function f() { return '1'; }, function g() {return 2; })();
  typeof f;

/***********************************************/

  var x = 1;
  if ( function f() {} ) {
    x += typeof f;
  }
  x;

/***********************************************/

  var x = [typeof x, typeof y][1];
  typeof typeof x;

/***********************************************/

  (function (foo) {
    return typeof foo.bar;
  })({ foo: { bar: 1 } });

/***********************************************/

  (function f() {
    function f() { return 1; }
    return f();
    function f() { return 2; }
  })();

/***********************************************/

 function f() { return f; }
  new f() instanceof f;

/***********************************************/

with (function (x, undefined) {}) length;

/***********************************************/

  var x = 1;
  {
    var x = 2;
  }
  alert(x);

/***********************************************/

  var x = 5,
      o = { x: 10,
            doIt: function doIt() {
                    var x = 20;
                    setTimeout( function () {
                        alert(this.x);
                    }, 10);
            }
       };
  o.doIt();

/***********************************************/

  var o = {
            x: 8,
            valueOf: function () {
              return this.x + 2;
            },
            toString: function () {
              return this.x.toString();
            }
          },
          result = o < '9';
  alert(o);

/***********************************************/

  function foo() {
    return 'Как правило, на этом срезаются новички';
  }

  function bar() {
    return
        'Как правило, на этом срезаются новички';
  }

  foo();
  bar();

/***********************************************/

  var o = { 
            b: function () { 
                  alert(this === o); 
                } 
          };
  o['b']();

/***********************************************/

  for(var i = 0; i < 10; i++) {
    setTimeout(function () {
         alert(i);
    }, 100);
  }

/***********************************************/

  function isEven(arg) {
    if (arg % 2 == 0) return 1;
    return undefined;
  }
  if (isEven(3) == false) {
      alert('ба, нечетное число!');
  }

/***********************************************/

  var obj = {
              toString: function () {
                return '[object MyObject]';
              },
              valueOf: function () {
                return 17;
              }
            };
  'object: ' + obj;

/***********************************************/

  'hello'.someProperty = 17;
  'hello'.someProperty;

/***********************************************/

  var s = new String('hello');
  typeof 'hello';
  typeof s;

/***********************************************/
  ' clef'.length;
  'G clef'.length;

/***********************************************/

  var x1 = /[/ + 'javascript'[0] + '///';
  // Ответ: /[\/ + 'javascript'[0] + '/

  var x2 = /\[/ + 'javascript'[0] + '///';
  // Ответ: /\[/j///

/***********************************************/

  'Hello'[-1];
  'Hello'.charAt(-1);

/***********************************************/

  if ( new Boolean (false) ) alert('true') // .. ?

/***********************************************/

  with({a: 1}) {
    a = 2,
    b = 3
  }

  [window.a, window.b];

/***********************************************/

  if(false) {
    function x() { a = 1 }
  }

  x();

/***********************************************/

  new Promise( function () {}).then( function () { throw 'err' })

  setTimeout( function () { 'no Error:)'}, 1000);

/***********************************************/

  (function pewpew(Infinity, length, __proto__) {
    return [,,~0.[0|0]][pewpew.__proto__.length && Infinity, -~String(this).length >> __proto__] << (0. === .0) + Infinity;
  }).apply(typeof pewpew, [,,2]) ;  // -1




```
