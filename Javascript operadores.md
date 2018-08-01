# Javascript diferentes operadores

### Operadores aritméticos

JavaScript posee diferentes tipos de operadores en este caso veremos los aritméticos.

Estos operadores toman los valores numéricos y aplican una operación para devolver un unico resultado, contamos con diferentes tipos de operadores como por ejemplo:

> Suma : 10 + 20

> Resta: 20–30

> Divisiones: 100 / 25

> Multiplicaciones 5 * 5

*Estos operadores funcionan como en la mayoria de los lenguajes de programacion como por ejemplo “Python, Ruby, Java, C”*

El operador de suma tambien puede utilizarse para realizar una acción llamada concatenación de dos o mas Strings como por ejemplo.

`"Hola " + "Mundo"`

Lo cual nos mostrara por consola o pantalla el resultado de

`"Hola Mundo"`

En JavaScript tambien nos encontramos con los operadores de Incremento y decremento, que añaden uno o restan uno a la variable numerica en la que sean aplicados

#### Incremento

```
var x = 3; //VALOR INICIAL DE X
var y = ++x //AQUI SE REALIZA 3 + 1 LO CUAL SE REALIZA CON ++X
```

#### Decremento

```
var x = 5; //VALOR INICIAL DE X
var y = --x //AQUI SE REALIZA 5 - 1 LO CUAL SE REALIZA CON --X
```

#### Operador typeOf

Este operador es especial dado que nos permite a nosotros conocer el tipo(number, boolean, undefined) que tiene la variable sobre la cual vamos a realizar una acción

```
typeof 5; //NUMBER
typeof false; //BOOLEAN
typeof "Mariano"; //String
typeof undefined; //undefined
```

Esto nos va a permitir a nosotros saber los tipos de datos y asì prevenir errores en el desarrollo.

#### Operadores Booleanos

Este tipo de operador solo tiene dos posibles valores:`true`lo cual significa verdadero y `false`lo cual es falso, pero disponemos de ciertos operadores los cuales nos van a permitir transformar estos valores.

#### Negación:

Como su nombre lo dice convierte el valor en el contrario, es representado con el signo `!`

> *“Si utilizamos este valor dos veces !! nos va a devolver el valor original”*

```
!false = true;
!true = false;
!!false = false;
```

Identidad o igualdad

El operador de comparación realiza la acción de comparar sus operandos y devolver un valor lógico (true o false). Estos operadores pueden ser numericos, Strings, logicos o de objetos. En el caso de las cadenas de caracteres(Strings) son comparadas basandose en el orden lexicografico estándar. En los casos que los operandos no sean del mismo tipo JavaScript intenta convertirlos en el tipo apropiado para permitir la comparacion, generalmente esta conversion se realiza de manera numerica. Esta conversion tiene como excepcion la utilizacion de los operadores ===(igualdad) y !==(desigualdad) de manera estricta.

```
true === true // true
true === false // false
true !== false //true
true !== true //false
```

#### Comparacion

Podemos comparar si dos valores son menores, iguales, mayores y mas con los operadores de comparación, representados con los signos `<`, `>`,`<=`, `≥=`. El resultado de la comparación nos devuelve `true` o `false` dependiendo si la comparación es correcta o no

```
15 > 3 //true
15 < 3 //false
3 >= 3 //true
2 <= 1 //false
"a" < "b" //true
```

#### Operadores logicos

#### Operador AND

Es un operador logico que devuelve true siempre que **TODOS** los valores comparados sean verdaderos. Si **UNO** de ellos es falso devuelve false. El operador AND es representado con el simbolo`&&`

```
true && true //true
true && false //false
false && true //false
false && false //false
```

### Operador OR

Es otro de los operadores lógicos funciona a la **inversa** que **AND**, devuelve false si los valores comparados son falsos. En el caso que **UNO** de los valores sea `true` retornara **verdadero**. Es representado con el simbolo `||`.

```
true || true //true
true || false //true
false || true // true
false || false //false
```

Tambien es utilizado para asignar valores por defecto en las funciones, la logica es la siguiente:

> Si el PRIMER valor es VERDADERO devuelvo ese valor

```
var port = process.env.PORT || 5000;
```

En ese ejemplo la variable port contendra el valor de process.env.PORT siempre que esa variable este declarada si no su valor sera 5000

Gracias por leer 💻