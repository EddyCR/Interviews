# Interview Questions

## HTML Section
- What does a `doctype` do?
- Why is it generally a good idea to position CSS `<link>s` between `<head></head>` and JS `<script>`s just before `</body>`? 
- What are data- attributes good for?
- Describe the difference between a `cookie`, `sessionStorage` and `localStorage`?
- What is progressive rendering?

## CSS Section
- Explaing what is the box model.
- What's the difference between _"resetting"_ and _"normalizing"_ CSS?
- What are the advantages/disadvantages of using CSS preprocessors?
- What's the difference between inline and inline-block?

## Javascript Section
- What's the difference between a variable that is: `null`, `undefined`?
- Explaining JavaScript `scope` and `closures`.
    ```javascript
    function f001(){
        console.log(a);
        var a = 5;
        console.log(a);
        console.log(foo());

        for(var i = 0; i < 10; i++){
            var a = i;
        };

        function foo(){
          return 2;
        }

        console.log(a);
    };
    ```
- What'ss the difference between `==` and `===`?
    ```javascript
    var a = true;
    var b = 'true';
    var c = 1;
    var d = 0;
    var e = "0";

    console.log( a == b); // false 'true' is converted to NaN, true is converted to 1, por eso es falso
    console.log( a === b); // false
    console.log( a == c); // true
    console.log( a === c); // false
    console.log( d == e); // true
    console.log( d === e); // false
    ```
- What's a Ternary expression? Give an example
  ```javascript
  condition ? expr1 : expr2
  ```
- What is `"use strict";`? what are the advantages and disadvantages to using it?
- Explain the difference between _synchronous_ and _asynchronous_ functions.
- What's the difference between `.call` and `.apply`?
- Explain _"hoisting"_.
    ```javascript
    f001();
    f002();

    function f001(){
         function a() {
            console.log('a');
        }

        a();
    };

    function f002(){
        var b = undefined;

        b();

        b = function() {
            console.log('b');
        }
    };
    ```
- What's the difference between an _"attribute"_ and a _"property"_?
- What is event loop?
  - What is the difference between `call stack` and `task queue`?
- Explain the difference between _mutable_ and _immutable_ objects.
  - What is an example of an immutable object in JavaScript?
- Vanilla Methods, ask for functionality of the list bellow using the fruits array
```javascript
   var fruits = ["Banana", "Orange", "Apple", "Mango"];
   splice, slice, .map
```

## Angular Section
