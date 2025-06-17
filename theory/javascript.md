# JavaScript

## Índice

1. Introducción a JavaScript
2. Sintaxis básica
3. Tipos de datos
4. Variables y constantes
5. Operadores
6. Estructuras de control
7. Funciones
8. Objetos
9. Arrays
10. Métodos útiles de Arrays
11. Bucles (Loops)
12. Funciones de orden superior
13. Manipulación del DOM
14. Eventos
15. Temporizadores (Timers)
16. JSON
17. Fetch API y Promesas
18. Async/Await
19. Módulos
20. Error Handling
21. Programación Orientada a Objetos (POO)
22. Clases
23. Closures
24. Scope y Hoisting
25. Callbacks
26. This, Bind, Call y Apply
27. Storage (localStorage y sessionStorage)
28. Expresiones Regulares
29. Web APIs (intro)
30. Buenas prácticas

---

## 1. Introducción a JavaScript

JavaScript es un lenguaje de programación interpretado, orientado a objetos, dinámico y débilmente tipado. Se ejecuta en el navegador y también en servidores (Node.js).

- Se usa para añadir interactividad a páginas web.
- Es uno de los tres pilares del desarrollo web junto a HTML y CSS.

```html
<script src="script.js"></script>
```

## 2. Sintaxis básica

```js
// Comentario de una línea
/* Comentario de varias líneas */

console.log("Hola Mundo");
```

## 3. Tipos de datos

- Primitivos: `string`, `number`, `boolean`, `undefined`, `null`, `symbol`, `bigint`
- Referencia: `object`, `array`, `function`

```js
let nombre = "Juan"; // string
let edad = 30; // number
let esMayor = true; // boolean
let nada = null; // null
let indefinido; // undefined
```

## 4. Variables y constantes

```js
let nombre = "Paulo"; // puede cambiar
const PI = 3.14; // constante
var edad = 25; // forma antigua, evitar
```

## 5. Operadores

- Aritméticos: `+ - * / % ++ --`
- Comparación: `== === != !== < > <= >=`
- Lógicos: `&& || !`
- Asignación: `= += -= *= /=`
- Ternario: `condición ? valor1 : valor2`

## 6. Estructuras de control

```js
if (edad > 18) {
  console.log("Mayor de edad");
} else {
  console.log("Menor de edad");
}

switch (dia) {
  case 1:
    console.log("Lunes");
    break;
  default:
    console.log("Otro día");
}
```

## 7. Funciones

```js
function saludar(nombre) {
  return "Hola " + nombre;
}

const sumar = (a, b) => a + b;
```

## 8. Objetos

```js
const persona = {
  nombre: "Ana",
  edad: 28,
  saludar() {
    console.log("Hola, soy " + this.nombre);
  },
};
```

## 9. Arrays

```js
let frutas = ["manzana", "banana", "pera"];
```

## 10. Métodos útiles de Arrays

```js
frutas.push("uva");
frutas.pop();
frutas.forEach((f) => console.log(f));
let nueva = frutas.map((f) => f.toUpperCase());
```

## 11. Bucles (Loops)

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}

while (condicion) {
  // código
}
```

## 12. Funciones de orden superior

Funciones que reciben otras funciones o las devuelven.

```js
function operar(a, b, fn) {
  return fn(a, b);
}
```

## 13. Manipulación del DOM

```js
const btn = document.getElementById("boton");
btn.textContent = "Click me";
```

## 14. Eventos

```js
btn.addEventListener("click", () => {
  alert("Click!");
});
```

## 15. Temporizadores

```js
setTimeout(() => console.log("Hola"), 1000);
setInterval(() => console.log("Cada segundo"), 1000);
```

## 16. JSON

```js
const persona = { nombre: "Ana" };
let json = JSON.stringify(persona);
let obj = JSON.parse(json);
```

## 17. Fetch API y Promesas

```js
fetch("https://api.example.com")
  .then((res) => res.json())
  .then((data) => console.log(data))
  .catch((err) => console.error(err));
```

## 18. Async/Await

```js
async function obtenerDatos() {
  try {
    const res = await fetch("https://api.example.com");
    const datos = await res.json();
    console.log(datos);
  } catch (e) {
    console.error(e);
  }
}
```

## 19. Módulos

```js
// archivo.js
export const PI = 3.14;

// main.js
import { PI } from "./archivo.js";
```

## 20. Manejo de errores

```js
try {
  // código que puede fallar
} catch (error) {
  console.error(error);
} finally {
  console.log("Siempre se ejecuta");
}
```

## 21. Programación Orientada a Objetos (POO)

- Encapsulamiento
- Herencia
- Abstracción
- Polimorfismo

## 22. Clases

```js
class Persona {
  constructor(nombre) {
    this.nombre = nombre;
  }
  saludar() {
    console.log("Hola " + this.nombre);
  }
}
```

## 23. Closures

```js
function crearContador() {
  let contador = 0;
  return function () {
    contador++;
    console.log(contador);
  };
}
```

## 24. Scope y Hoisting

- Scope: local, global
- Hoisting: las `var` y funciones se elevan

## 25. Callbacks

```js
function hacerTarea(callback) {
  console.log("Tarea hecha");
  callback();
}
```

## 26. This, Bind, Call, Apply

```js
const obj = {
  nombre: "Ana",
  saludar() {
    console.log(this.nombre);
  },
};

const saludo = obj.saludar.bind(obj);
saludo();
```

## 27. Storage

```js
localStorage.setItem("clave", "valor");
localStorage.getItem("clave");
```

## 28. Expresiones Regulares

```js
const regex = /\d+/;
regex.test("123");
```

## 29. Web APIs (intro)

- Geolocation
- Web Storage
- Fetch
- WebSockets

## 30. Buenas prácticas

- Usar `const` y `let`, no `var`
- Nombres descriptivos
- Separar lógica en funciones pequeñas
- Evitar código repetido
- Usar linter y formateadores (Prettier, ESLint)

---

**Autor**: Apuntes generados por ChatGPT para Paulo Arce
