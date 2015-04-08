#Javascript
Javascript has Two types
Primitive types and Reference types

##Primitive types
- ####Boolean
- ####Number
- ####String
- ####Null
- ####Undefined

Use typeof to identify primitive types
Null Gotcha...
```javascript
typeof for null //returns object....!!!
console( typeof null );// object
```
Instead use

```javascript
console( aVar === null );// true || false
```
##Reference Types
- ####Object
- ####Array
- ####Date
- ####Error
- ####Function
- ####RegExp

Use `instanceof` to identify Reference types

##Functions
prefer function declaration over function expression as declared ones get hoisted.
```javascript
fn declaration: function fn(){}
fn statement: var fn = function(){};
```

```javascript
fn.call( contextFor|this|, 1,2,3,4,5 ) // Comma seperated extra values
fn.apply( contextFor|this|, [1],2,3,4,5] ) // Array for extra values
```
Bind returns new fn, great for callbacks
```javascript
var newFn = fn.bind( contextFor|this| );
```
#Objects
Two types of properties, Data and Accessor
Data properties have a value
```javascript
obj.x = 5;
```
Accessor properties have a getter || && setter
```javascript
var o = {
  aaa:'aaa'
  set tripleA(value){
      ...do something
      this.aaa = value;
  },
  get tripleA(){
      ...do something
      return this.aaa;
  }
}
console.log(o.tripleA);
o.tripleA = 'AAA';
```
Define a prop`s attributes
```javascript
var o = {};
Object.defineProperty(o, 'prop', {

  // Following only for Data Properties
  value: 'a value', // assigning a value
  writable: true,  // It cannot be reassigned

  // Applicable for both Data and Accessor Properties
  enumerable: true, // will appear in: for( prop in o ){}
  configurable: true // prop can change or be deleted
});
```

Test for a prop on an obj or its chain with the |in| operator
```javascript
if('prop' in obj ){}
```
Test for a prop on an obj only with the |hasOwnProerty| method
```javascript
if( obj.hasOwnProperty('prop')){}
```
Delete prop with |delete| operator
```javascript
delete obj.propThatWillBeDeleted
```

##Constructor property
```javascript
function Fn(){};
var fn = new Fn();
fn.constructor; // function Fn(){}

var o = {};
o.constructor; // function Object() { [native code] }
```

##Prototype property
Functions have |protype| property which is just an object thus we can create dynamic props like so
```javascript
function Fn(){};
Fn.prototype.foo = function(){};
```
Objects have the internal [[prototype]] but browsers expose it via

```javascript
__proto__
```
