```javascript

/*
Nivel: basico

Pregunta1: como contarias el numero de comas en 'hola, me llamo, juan, perez' con una for loop
Esta pregunta es para ver si el intrevistado sabe hacer for loops

*/

f00();

function f00(){
    var a = 'hola, me llamo, juan, perez';
    var count = 0;
    
    for(var i = 0; i < a.length; i++){
        if(a[i] === ','){
            count++;
        }
    } 
    console.log(count);
};

----------------------------------------

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
