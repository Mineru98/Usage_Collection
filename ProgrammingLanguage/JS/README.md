JavaScript
==========

# 1. ES5 vs ES6
## Default Parameters
### ES5 Syntax 
```JS
var link = function (height, color, url) {
    var height = height || 50
    var color = color || 'red'
    var url = url || 'http://azat.co'
    ...
}
```

### ES6 Syntax
```JS
var link = function(height = 50, color = 'red', url = 'http://azat.co') {
  ...
}
```

## Template Literals
### ES5 Syntax
```JS
var first = 'TK';
var last = 'Lee';
var id = 1;
var name = 'Your name is ' + first + ' ' + last + '.'
var url = 'http://localhost:3000/api/messages/' + id
```
### ES6 Syntax
```JS
var first = 'TK';
var last = 'Lee';
var id = 1;
var name = `Your name is ${first} ${last}.`
var url = `http://localhost:3000/api/messages/${id}`
```

## Multi-line Strings
### ES5 Syntax
```JS
var roadPoem = 'Then took the other, as just as fair,\n\t'
    + 'And having perhaps the better claim\n\t'
    + 'Because it was grassy and wanted wear,\n\t'
    + 'Though as for that the passing there\n\t'
    + 'Had worn them really about the same,\n\t'

var fourAgreements = 'You have the right to be you.\n\
    You can only be you when you do your best.'
```

### ES6 Systax
```JS
const roadPoem = `Then took the other, as just as fair,
    And having perhaps the better claim
    Because it was grassy and wanted wear,
    Though as for that the passing there
    Had worn them really about the same,`

const fourAgreements = `You have the right to be you.
    You can only be you when you do your best.`
```

## Destructuring Assignment
### ES5 Syntax
```JS
// Node.js
var jsonMiddleware = require('body-parser').json

var body = req.body, // body has username and password
  username = body.username,
  password = body.password
```

### ES6 Systax
```JS
// Node.js
var {jsonMiddleware} = require('body-parser')

var {username, password} = req.body
```

## Enhanced Object Literals
### ES5 Syntax
```JS
var serviceBase = {port: 3000, url: 'azat.co'},
    getAccounts = function(){return [1,2,3]}

var accountServiceES5 = {
  port: serviceBase.port,
  url: serviceBase.url,
  getAccounts: getAccounts,
  toString: function() {
    return JSON.stringify(this.valueOf())
  },
  getUrl: function() {return "http://" + this.url + ':' + this.port},
  valueOf_1_2_3: getAccounts()
}
```

### ES6 Systax
```JS
var serviceBase = {port: 3000, url: 'azat.co'},
    getAccounts = function(){return [1,2,3]}
var accountService = {
    __proto__: serviceBase,
    getAccounts,
    toString() {
     return JSON.stringify((super.valueOf()))
    },
    getUrl() {return "http://" + this.url + ':' + this.port},
    [ 'valueOf_' + getAccounts().join('_') ]: getAccounts()
};
```

## Arrow Functions
### ES5 Syntax
```JS
var ids = ['5632953c4e345e145fdf2df8','563295464e345e145fdf2df9']
var messages = ids.map(function (value) {
  return "ID is " + value // explicit return
});
```

### ES6 Systax
```JS
const ids = ['5632953c4e345e145fdf2df8','563295464e345e145fdf2df9']
const messages = ids.map(value => `ID is ${value}`) // implicit return
```

## Promises
### ES5 Syntax
```JS
setTimeout(function(){
  console.log('Yay!')
}, 1000)

setTimeout(function(){
  console.log('Yay!')
  setTimeout(function(){
    console.log('Wheeyee!')
  }, 1000)
}, 1000)
```

### ES6 Systax
```JS
const wait1000 =  new Promise(function(resolve, reject) {
  setTimeout(resolve, 1000)
}).then(function() {
  console.log('Yay!')
})

const wait1000 =  ()=> new Promise((resolve, reject)=> {setTimeout(resolve, 1000)})

wait1000()
    .then(function() {
        console.log('Yay!')
        return wait1000()
    })
    .then(function() {
        console.log('Wheeyee!')
    });
```

## Block-Scoped Constructs Let and Const
### ES5 Syntax
```JS
function calculateTotalAmount (vip) {
  var amount = 0
  if (vip) {
    var amount = 1
  }
  { // more crazy blocks!
    var amount = 100
    {
      var amount = 1000
      }
  }
  return amount
}
console.log(calculateTotalAmount(true))
```

### ES6 Systax
```JS
// let is variable
// const is a constant

// let
function calculateTotalAmount (vip) {
  var amount = 0 // probably should also be let, but you can mix var and let
  if (vip) {
    let amount = 1 // first amount is still 0
  }
  { // more crazy blocks!
    let amount = 100 // first amount is still 0
    {
      let amount = 1000 // first amount is still 0
      }
  }
  return amount
}
console.log(calculateTotalAmount(true))

// const
function calculateTotalAmount (vip) {
  const amount = 0
  if (vip) {
    const amount = 1
  }
  { // more crazy blocks!
    const amount = 100
    {
      const amount = 1000
      }
  }
  return amount
}
console.log(calculateTotalAmount(true))
```

## Classes
### ES5 Syntax
```JS
var Person = (function () {
  // Constructor
  function Person(name) {
    this._name = name;
  }

  // public method
  Person.prototype.sayHi = function () {
    console.log('Hi! ' + this._name);
  };

  // return constructor
  return Person;
}());

var me = new Person('Lee');
me.sayHi(); // Hi! Lee.

console.log(me instanceof Person); // true
```

### ES6 Systax
```JS
// 클래스 선언문
class Person {
  // constructor(생성자)
  constructor(name) {
    this._name = name;
  }

  sayHi() {
    console.log(`Hi! ${this._name}`);
  }
}

// 인스턴스 생성
const me = new Person('Lee');
me.sayHi(); // Hi! Lee

console.log(me instanceof Person); // true
```

## Modules
### ES5 Syntax
```JS
// module.js
module.exports = {
  port: 3000,
  getAccounts: function() {
    ...
  }
}

// index.js
var service = require('module.js')
console.log(service.port) // 3000
```

### ES6 Systax
```JS
// module.js
export var port = 3000
export function getAccounts(url) {
  ...
}

// index.js
import {port, getAccounts} from 'module'
console.log(port) // 3000

or

import * as service from 'module'
console.log(service.port) // 3000

```



