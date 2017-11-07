```javascript
/*
Nivel: intermedio

Pregunta: que impreme los console logs?
Respuesta: undefined, 5, 2, 9

Con está pregunta, se puede evaluar:
-El entrevistado sabe que el scope de javascript es por funcion y no por blocks. 
*/

f001();

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

-------------------------------------
/*
Nivel: intermedio

Pregunta1: cual es la diferencia en funcionamiento al comparar con === vs ==
=== usa igualdad estricta. Los valores no son convertidos a otro valor antes de hacer la comparacion. Si los valores son de diferente typo, entonces no son iguales. 
Si los valores tienen el mismo typo y el mismo valor, entonces son considerados iguales
== compara que los valores sean iguales despues de haberlos convertido a un typo comun.
*/

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

--------------------------------------
/*
Nivel: intermedio - avanzado

Pregunta1: cual de estas funciones causa un error al ser llamada?
Respuesta: f002

Pregunta 2: por que foo1 no causa ningun error?
Esta pregunta es para ver si el entrivistado entiende la diferencia entre function declaration y function expressions, y para ver tambien si 
entiende el concepto de 'hoisting'.

a() es una function declaration
b() es una function expression

Function declarations and variables son 'hoisted', lo cual significa que son movidas al inicio del scope por el interpretador de javascript. 
Expreciones no son hoisted.

por ejemplo, f001 quedaría asi por el interpretador y por eso no hay ningun error:

f001(){
     function a() {
        console.log('a');
    }
    
    a();
}

mientras que f002 quedaria asi por el interpretador:

function f002(){
    var b = undefined;
    
    b(); // error: b no es una funcion, es undefined
    
    b = function() {
        console.log('b');
    }
}
*/

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

----------------------------------
/*
 Preunta: Cuál es el resultado del output?
 Respuesta: undefined

 El operador delete es usado para eliminar una propiedad de un object.
 En el ejemplo x es un objeto que tiene una propiedad foo, output es una funcion de selft-invoking que va a eleminar la propiedad foo del objecto .
 Despues de hacer eso cuando se intenta referenciar la propiedad foo el resultado va a ser undefined
 */

var x = { foo : 1};
var output = (function(){
    delete x.foo;
    return x.foo;
  })();

  console.log(output);

  ----------------------------------


```
