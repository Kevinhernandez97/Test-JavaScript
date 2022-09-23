**VARIABLES Y OPERACIONES**

1. ¿Qué es una variable y para qué sirve?

Una variable es un espacio en memoria donde almacenamos informacion de diferentes tipos de datos que sera usada en
codigo, estas variables se pueden crear de 3 formas distintas: var, const, let

2.  ¿Cuál es la diferencia entre declarar e inicializar una variable?

**_Declarar_**:  Darle nombre a la variable

```js
let name;
```

**_Inicializar_**: Indicarle el tipo de dato e informacion que va a almacenar esto se hace con un =

```js
let name = "camilo";
```

3.  ¿Cuál es la diferencia entre sumar números y concatenar strings?

Sumar numeros es la operacion matematica el cual nos arroja el resultado de dicha operacion.

```js
let a = 1;
let b = 2;
let c = a + b;

c = 3
```

concatenar strings la computadora toma el numero creyendo que es texto y los une, no realiza ninguna operacion matematica.

```js
let x = "1";
let y = "2";
let z = x + y;

z = '12'
```

4. ¿Cuál operador me permite sumar o concatenar?

El operador es con el simbolo **+**, el cual hace referncia a suma.

5.  Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

```js
 Nombre
("string");
 Apellido
("string");
 Nombre de usuario en Platzi
("string");
 Edad
("number");
 Correo electrónico
("string");
 Mayor de edad
("boolean");
 Dinero ahorrado
("number");
 Deudas
("number");
```

6. Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```js
let nome = "andres";
let apellido = "rodriguez";
let usuarioPlatzi = "AndresRod1522";
let edad = 25;
let email = "example@hotmail.com";
let mayoriaDeEdad = true;
let dineroAhorrado = 1500;
let deudas = 700;
```

7. Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

```js
Nombre completo (nombre y apellido)
console.log(`${nome} ${apellido}`);

Dinero real (dinero ahorrado menos deudas)
console.log(`${dineroAhorrado - deudas}`);
```


**FUNCIONES**

1. Responde las siguientes preguntas en la sección de comentarios:

. _¿Qué es una función?_
Funcion es un conjunto de instrucciones que realiza una tarea o calcula un valor, esta debe tomar alguna entrada y siempre devuelve un valor

. _¿Cuándo me sirve usar una función en mi código?_
cuando estamos repitiendo codigo la utilidad de las funciones es para evitar esto. Adicional facilita el mantenimiento de los desarroladores y tener una mejor lectura.

. _¿Cuál es la diferencia entre parámetros y argumentos de una función?_
los parametros sirven para pasar valores que serian utilizados en el codigo de la funciion los argumentos son los valores que le envio a los parametros

```js
//siendo a y b los parametros
function myfunction(a, b) {
  return a + b;
}

//siendo 3 y 4 los valores que le envio a los parametros, importa el orden en que se posicionan
myfunction(3, 4);
```

2. Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
const nombre = "Juan David";
const lastname = "Castro Gallego";
const completeName = nombre + " " + lastname;
const nickname = "Juandc";
var anos;

console.log(
  "Mi nombre es " +
    completeName +
    ", pero prefiero que me digas " +
    nickname +
    "."
);

function miNombre(completeName, nickname) {
  return console.log(
    `Mi nombre es ${completeName}, pero prefiero que me digas ${nickname}.`
  );
}

miNombre("KEVIN MAURICIO HERNANDEZ", "DRYPRO97");

console.log(miNombre);
```


**CONDICIONALES**

1. Responde las siguientes preguntas en la sección de comentarios:

. _¿Qué es un condicional?_
es una instruccion o grupos de instrucciones, el cual el codigo se ejecuta si se cumple la condicion.

. _¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?_

**if, esle if, else**
 este operador tiene tres operandos, se pueden generar este operador cuantas veces sea necesario

**switch**
 este operador evalua una expresion, comparando el valor de esa expresion con una instancia case. la diferencia con el if es que este se utiliza para condicionar multiples condiciones, en vez de utilizar multiples if-else

_¿Puedo combinar funciones y condicionales?_
si, las funciones pueden encapsular cualquier bloque de código, incluyendo condicionales.

2. Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
const tipoDeSuscripcion = "free";

if (tipoDeSuscripcion === "free") {
  console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion === "basic") {
  console.log("Puedes tomar casi todos los cursos de platzi durante un mes");
} else if (tipoDeSuscripcion === "expert") {
  console.log("Puedes tomar casi todos los cursos de platzi durante un año");
} else if (tipoDeSuscripcion === "expertPlus") {
  console.log(
    "Tu y alguien mas pueden tomar todos los cursos de platzi durante un año"
  );
} else {
  console.log("No tienes ninguna suscripcion");
}
```

3. Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

```js
let typeSuscription = ["free", "basic", "expert", "expertPlus"];
let infoSuscription = [
  "Solo puedes tomar los cursos gratis",
  "Puedes tomar casi todos los cursos de platzi durante un mes",
  "Puedes tomar casi todos los cursos de platzi durante un año",
  "Tu y alguien mas pueden tomar todos los cursos de platzi durante un año",
];
let userSuscription = "basic";

for (let i = 0; i < typeSuscription.length; i++) {
  if (userSuscription == typeSuscription[i]) {
    console.log(`${infoSuscription[i]}`);
  }
}
if (tipoDeSuscripcion === "free") {
  console;
}
```


**CICLOS**

1. Responde las siguientes preguntas en la sección de comentarios:

_¿Qué es un ciclo?_
Un ciclo son loops(bucles), los cuales son utilizados para realizar tareas repetitivas con base a una condicion. es decir continuara ejecutandose hasta que la condicion devuelva false.

_¿Qué tipos de ciclos existen en JavaScript?_
.for
.while
.do while

_¿Qué es un ciclo infinito y por qué es un problema?_
es cuando la condicion es infinita y este continuara ejecutandose infinitas veces

_¿Puedo mezclar ciclos y condicionales?_
si

2. Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:


```js
for (let i = 0; i < 5; i++) {
  console.log("El valor de i es: " + i)
}

for (let i = 0; i >= 2; i--) {
  console.log("El valor de i es: " + i)

}

let i = 0;

while (i < 5) {
  i++;
  console.log(`El valor de i es: ${i}`);
}

let index = 10;

while (index >= 2) {
  index--;
  console.log("El valor de i es: " + index);
}
```

3. Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

```js
let pregunta = prompt("Cuanto es 2 + 2");

while (pregunta != 4) {
  pregunta = prompt("Cuanto es 2 + 2");
}
```


**LISTAS**

1. Responde las siguientes preguntas en la sección de comentarios:

_¿Qué es un array?_
Es un grupo de elementos asignados a una variable, estos van dentro del simbolo [] y se separan por medio de una ,

_¿Qué es un objeto?_
Es un contenedor de datos, los cuales contienen atributos y metodos

_¿Cuándo es mejor usar objetos o arrays?_
Ocupamos arrays cuando queremos una lista especifica de datos, en cambio cuando tenemos elementos muy grandes y con distintos valores utilizamos objetos

_¿Puedo mezclar arrays con objetos o incluso objetos con arrays?_
si

2.  Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```js
let arrays = ["andres", "camila", "jueves"];

function miArray(arrays) {
  console.log(arrays[0]);
}

miArray(arrays);
```

3. Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo) 

```js
function miArray2(arrays2) {
  for (let index = 0; index < arrays2.length; index++) {
    console.log(arrays2[index]);
  }
}

miArray2(["LUNES", "MARTES", "MIERCOLES"]);
```

4.  Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo)

```js
let auto = {
  marca : 'Ford',
  modelo : 'Fusion',
  annio : 2011
}

function miAuto (object) {
  for(let key in object) {
  console.log(object[key])
 }
}

miAuto(auto)
```