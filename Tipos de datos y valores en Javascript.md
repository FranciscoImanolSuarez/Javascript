# Tipos de datos y valores en Javascript

El tipo de dato es una propiedad de un valor que determina valores que puede tomar, que tipos de operaciones podemos realizar sobre este y cómo su representación interna.

En JavaScript encontramos diferentes tipos de valores y tipos de datos para almacenar en variables.

### Valores y tipos

*Tipo principales (primitivos)*

> string
> number
> boolean

*Tipo compuesto*

> Objeto

> Matriz

*Tipo especiales*

> Null

> Undefined

En el caso de **ES6** se presenta un nuevo tipo de este tipo de denominación como `symbol `este tipo de datos cuyos valores son únicos y no pueden ser alterados.

JavaScript proporciona un operador llamado `typeof`este operador que puede examinar un valor y decirle qué tipo es:

Como les comentaba en el capitulo [anterior](https://medium.com/@imanol_suarez/javascript-diferentes-operadores-6840ba8cf29) JavaScript presenta un operador llamado `typeof `este operador nos permite a nosotros como desarrolladores saber de que tipo es la variable:

```
var x;
typeof x;                // "undefined"
```

```
y = 21;
typeof y;                // "number"
```

```
m = undefined;
typeof m;                // "undefined"
```

```
j = "hello world";
typeof j;                // "string"

k = true;
typeof k;                // "boolean"

n = null;
typeof n;                // "object"
```

Este operador es especial dado que nos permite a nosotros conocer el tipo(number, boolean, undefined,object,) que tiene la variable sobre la cual vamos a realizar una acción.

#### String

Un valor de cadena es un conjunto de caracteres Unicode(letras,digitos,signos de puntuación y mas),este tipo de dato es el encargado de representar texto en JavaScript

```
"Hola mundo!"
'"La base de datos de virus a sido actualizada' 
"55"
'c'
```

#### Number

En JavaScript, no se distingue entre los valores enteros y de punto flotante; un número de JavaScript puede ser cualquiera de ellos (internamente, JavaScript representa todos los números como valores de punto flotante).

```
var x = 1;
var y = 1.23;
```

#### Boolean

Este tipo de dato almacena 1 bit puede ser `true` o `false` son utilizados para registrar un estado (VERDADERO O FALSO)

```
var verdadero = true;
var falso= false;
```

#### Objetos

Dado que JavaScript esta diseñado en un paradigma basado a objetos. Decimos que un objeto es una colección de propiedades, estos objetos se pueden comparar con objetos de la vida real objetos tangibles.

```
var auto= {
    a: "Ford",
    b: 2014,
    c: rojo
};
```

```
auto.a;        // "Ford"
auto.b;        // 2014
auto.c;        // rojo
```

Otra manera de acceder a las propiedades de estos objetos es de la siguiente manera:

```
var auto= {
    a: "Ford",
    b: 2014,
    c: rojo
};
```

```
auto["a"];    // "Ford"
auto["b"];    // 2014
auto["c"];    // rojo
```

```
var nombres = [‘Pedro’, ‘Mariano’];
```

```
console.log(nombres.length);
//Esto arroja como resultado 2 dado que la cantidad de datos dentro del array es de 2(Pedro y Mariano)
```

**Acceder (por índice) a un elemento Array**

```
var nombre = nombres[0];
```

```
// Pedro
```

```
var nombre = nombre[1];
```

```
// Mariano
```

Ahora si nos ponemos a pensar la posición nombre[1] debería ser **Mariano**, bueno al comenzar a programar esto puede sonar un poco raro, pero en programación arrancamos a contar desde el numero cero(0).

**Otro ejemplo**

```
var marcasDeComputadoras = [‘HP’,’Macbook Air’,’Macbook Pro’, ‘Lenovo’,’Acer’];
```

Este array(marcasDeComputadoras) esta compuesto por 5 elementos arrancando por HP y finalizando en Acer

```
var computadora = marcasDeComputadoras[0]; //HP
```

```
var computadora = marcasDeComputadoras[1]; //Macbook Air
```

```
var computadora = marcasDeComputadoras[2]; //Macbook P
```

```
var computadora = marcasDeComputadoras[3]; //Lenovo
```

```
var computadora = marcasDeComputadoras[4]; //Acer
```

#### Undefined

Este tipo de dato se utiliza cuando no sabemos el contenido de una variable o todavia no fue definido.

```
var x;
typeof x; // "undefined"
```

#### Null

El tipo de dato `null` tiene solamente el valor `null`. La palabra clave reservada `null` no puede ser utilizada como nombre de una funcion o una variable

Una variable que contiene `null` no contiene ningun tipo de numero, cadena o valor booleano ni una matriz u objeto. Este tipo de dato no es 0 como en otros lenguajes como C o C++, declarando una variable de tipo `null` y utilizando el operador typeof interpreta el valor como Object no como tipo `null`

Gracias por leer 💻