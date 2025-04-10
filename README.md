# 🧑‍🏫 Curso de React – Desarrollo de Aplicaciones Web con React

## 🗂️ Temario General del Curso

1. [Introducción a React ](#modulo-1-introducción-a-React) 
2. [Configuración del entorno de desarrollo ](#modulo-2-configuración-del-entorno-de-desarrollo) 
3. [JSX: Sintaxis especial de React](#modulo-3-jsx-sintaxis-especial-de-react)  
4. [Componentes (Funcionales y de Clase)](#modulo-4-componentes-funcionales-y-de-clase)
5. [Props (Propiedades entre componentes)](#modulo-5-props-propiedades-entre-componentes)
6. [Estado (useState)](#modulo-6-estado-con-usestate)
7. [Eventos en React](#modulo-7-Eventos-en-React)
8. [Ciclo de vida y useEffect](#modulo-8-useEffect-ciclo-de-vida-y-efectos-secundarios) 
9. [Estilos en React](#modulo-9-estilos-en-react)
10. [Listas y claves](#modulo-10-listas-y-claves)
11. [Formularios en React](#modulo-11-formularios-en-react)
12. [Lifting State Up y comunicación entre componentes](#modulo-12-lifting-state-up-y-comunicacion-entre-componentes)
13. [React Router (Navegación entre páginas)](#modulo-13-react-router-navegacion-entre-paginas)
14. [Consumo de APIs con fetch o Axios](#modulo-14-consumo-de-apis-con-fetch-o-axios)
15. [Custom Hooks](#modulo-15-custom-hooks)
16. [Context API (Manejo global del estado)](#modulo-16-context-api)
17. [Introducción a Redux (opcional, si quieres profundizar)](#modulo-17-introduccion-a-redux)
18. [Deploy de la aplicación React](#modulo-18-deploy-de-la-aplicacion-react)

---
<a name="modulo-1-introducción-a-React"></a>
## 📘 Módulo 1: Introducción a React

### ❓ ¿Qué es React?

React es una biblioteca de JavaScript creada por Facebook para construir interfaces de usuario. Su objetivo principal es crear aplicaciones web reactivas, eficientes y modulares.

### 💡 Ventajas clave:
- Componentes reutilizables
- Virtual DOM (mejora el rendimiento)
- Flujo de datos unidireccional (unidirectional data flow)
- Ideal para SPAs (Single Page Applications)


### 🧪 Ejemplo básico: crear un componente

Puedes crear HolaMundo directamente dentro del archivo App.js, o mejor aún, en su propio archivo para seguir buenas prácticas.

Tenemos 2 maneras de hacerlo:

🔹 Opción A – Dentro de App.js:

```jsx
// src/App.js
import React from 'react';

function HolaMundo() {
  return <h1>¡Hola, mundo desde React!</h1>;
}

function App() {
  return (
    <div>
      <HolaMundo />
    </div>
  );
}

export default App;
```

🔹 Opción B – En su propio archivo:

1. Crea un archivo nuevo llamado HolaMundo.js dentro de /src

2. Pon esto dentro:

```jsx
// src/HolaMundo.js
import React from 'react';

function HolaMundo() {
  return <h1>¡Hola, mundo desde React!</h1>;
}

export default HolaMundo;
```

3. Ahora importa y usa HolaMundo dentro de App.js:

```jsx
// src/App.js
import React from 'react';
import HolaMundo from './HolaMundo';

function App() {
  return (
    <div>
      <HolaMundo />
    </div>
  );
}

export default App;
```

Esto sería un componente muy básico en React.


### 🎯 Ejercicio para ti:

Crea un componente llamado Saludo que muestre el mensaje, "¡Bienvenido al curso de React!".

---
<a name="modulo-2-configuración-del-entorno-de-desarrollo"></a>
## 📘 Módulo 2: Configuración del Entorno de Desarrollo

### ❓ ¿Cómo empezar con React?

Para desarrollar con React de forma profesional, lo ideal es tener un entorno que nos permita comenzar rápido, sin perder tiempo en configuraciones innecesarias. Para eso existe una herramienta oficial: Create React App.
Create React App es un scaffolding tool que genera un proyecto React completo, listo para empezar, con todo configurado: Babel, Webpack, React y más.

### 🛠️ Cómo crear tu primer proyecto React:

1. Instalar Node.js y npm, para comprobar si estan instalados, usar estos comandos:

 ```bash
node -v
npm -v
``` 

2. Abre tu terminal (en VS Code o donde prefieras).

3. Ejecuta el siguiente comando:
   
```bash
npx create-react-app mi-app
```

4. Entra en el nuevo directorio del proyecto:

```bash
cd mi-app
```

5. Inicia el servidor de desarrollo:

```bash
npm start
```

Esto abrirá automáticamente el navegador en http://localhost:3000 con tu aplicación React funcionando. ¡Ya tienes tu primer entorno ⚛️ montado!

### 🗂️ Estructura básica del proyecto

```
📦 mi-app
├── 📁 public               → Contiene el HTML principal (`index.html`)
│   └── 📄 index.html
├── 📁 src                  → Aquí va todo tu código React
│   ├── 📄 App.js           → Componente principal de la aplicación
│   └── 📄 index.js         → Punto de entrada que renderiza `App.js`
└── 📄 package.json         → Dependencias y scripts del proyecto
```

### 🧼 Recomendación como desarrollador:

Al empezar un nuevo proyecto, te recomiendo limpiar el código inicial que trae App.js, App.css, y borrar logo.svg. Así puedes construir tu aplicación desde cero con total control.

### 🧪 Ejemplo básico:

En index.js deberías tener algo como esto:

```
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render();
```

Eso significa que lo que pongas dentro del componente App se verá en el navegador.

### 🎯 Ejercicio para ti:

1. Crea una nueva aplicación React con npx create-react-app.
2. Limpia el contenido de App.js.
3. Pega el componente HolaMundo del 📘 Módulo 1.
4. Abre tu navegador y verifica que se vea correctamente el mensaje.

---
<a name="modulo-3-jsx-sintaxis-especial-de-react"></a>
## 📘 Módulo 3: JSX – Sintaxis especial de React

### ❓ ¿Qué es JSX?

JSX (JavaScript XML) es una extensión de sintaxis para JavaScript que nos permite escribir código muy similar a HTML dentro de archivos JavaScript.

En lugar de separar la lógica y la interfaz como en otros frameworks, React propone una mezcla controlada: combinamos lógica y estructura de forma declarativa usando JSX.

### 🔎 ¿Por qué es útil JSX?

- Nos permite ver visualmente la estructura del componente.
- Es más legible y cercano al HTML tradicional.
- Aumenta la productividad al unir lógica y presentación en un solo lugar.

### 🚨 Importante:

JSX no es HTML real, aunque lo parezca. Por ejemplo:

* En lugar de class, se usa className.
* Todos los elementos deben cerrarse correctamente (por ejemplo: ![]()).
* Los atributos siguen la convención camelCase (onClick, tabIndex, etc).

### 📌 Diferencias entre HTML y JSX

| En HTML        | En JSX                             |
|---------------|------------------------------------|
| ```class```     | ```className```       |
| ```for```    | ```htmlFor``` |
| ```onclick```    | ```onClick```      |
| Atributos vacíos | Se escriben como booleanos: ```disabled={true}``` |
| Etiquetas deben cerrarse | ```img```, ```input```, etc. se cierran como ```<img />``` |

### 💡 Recordatorio: JSX es solo sintaxis

Dentro del JSX puedes usar JavaScript puro entre llaves {}:

```jsx
const usuario = "Lucía";
return <h2>Bienvenida, {usuario}</h2>;
```

### 🧪 Ejemplos básicos:

#### 📄 Ejemplo 1: básico

Este componente mezcla código JavaScript (```const nombre = "React"```) con etiquetas JSX (parecidas a HTML). Lo que aparece entre llaves {} dentro del JSX es interpretado como una expresión de JavaScript.

```jsx
function ComponenteJSX() {
  const nombre = "React";
  return (
    <div>
      <h1>Hola desde {nombre}</h1>
      <p>¡Esto es JSX funcionando!</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

Este componente muestra un saludo dinámico usando una variable declarada en JavaScript (```const nombre = "React"```).
* Dentro del ```return```, usamos JSX para crear una estructura HTML-like.
* Utiliza ```{nombre}``` para insertar dinámicamente el valor ```"React"``` dentro del texto del ```<h1>```.
* Luego, muestra un ```<p>``` con un mensaje fijo.

🧠 ¿Qué conceptos aplica?

* Interpolación de variables: con ```{}``` dentro de JSX puedes mostrar cualquier expresión de JavaScript.
* Encapsulamiento de UI: este componente podría reutilizarse con diferentes textos.
* Elementos anidados en un contenedor (```<div>```): JSX requiere que todo esté envuelto en un solo elemento padre.

✅ ¿Qué puedes aprender de esto?

* JSX no es HTML, pero se le parece mucho.
* Todo lo que escribas dentro del ```return``` tiene que estar envuelto en un solo nodo raíz.
* Las variables dentro del JSX deben ir entre llaves ```{}```.

💡 Variaciones sugeridas:

Puedes transformar el nombre en mayúsculas directamente:

```jsx
<h1>Hola desde {nombre.toUpperCase()}</h1>
```

O usar props para hacerlo reutilizable:

```jsx
function ComponenteJSX(props) {
  return <h1>Hola desde {props.nombre}</h1>;
}
```

#### 📄 Ejemplo 2: condicionales y ternarios

```jsx
function Mensaje(props) {
  return (
    <div>
      <h2>{props.logueado ? "Bienvenido" : "Inicia sesión"}</h2>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

Este componente recibe una propiedad llamada logueado (tipo booleano), y en base a su valor muestra uno de dos mensajes:
* Si ```logueado === true``` → muestra ```"Bienvenido"```
* Si ```logueado === false``` → muestra ```"Inicia sesión"```
Esto se logra usando el operador ternario:
```condición ? valor_si_verdadero : valor_si_falso```

💡 ¿Por qué es útil?

En React muchas veces necesitas mostrar diferentes elementos en función del estado, por ejemplo:
* Un usuario logueado vs. uno anónimo
* Un carrito lleno vs. uno vacío
* Un botón activado vs. desactivado
Esto lo puedes resolver elegantemente con ternarios dentro del JSX.

#### 📄 Ejemplo 3: aplicar estilos

```jsx
function Estilizado() {
  const estilo = {
    color: "tomato",
    fontSize: "20px",
    textAlign: "center"
  };

  return <p style={estilo}>¡Este texto tiene estilo JSX!</p>;
}
```
✅ ¿Qué hace este componente?
Este componente:
 1. Declara un objeto ```estilo``` con propiedades CSS (en camelCase)
 2. Usa ese objeto para aplicar estilos en línea al párrafo ```<p>```
El resultado es un texto centrado, en color tomate y con fuente de 20px.

🧠 ¿Qué debes saber sobre estilos en React?
* Los estilos en línea en JSX se pasan como un objeto de JavaScript
* Las propiedades CSS se escriben en camelCase (no ```font-size```, sino ```fontSize```)
* El valor de cada propiedad debe ir entre comillas como string (por ejemplo, ```"tomato"```)

💡 ¿Cuándo usar estilos en línea?
* Para estilos rápidos o condicionales
* Cuando no necesitas un archivo CSS externo
* En componentes muy pequeños o reutilizables

 🧪 Alternativa:
 
Podrías aplicar ese mismo estilo directamente en el elemento así:

```jsx
<p style={{ color: "tomato", fontSize: "20px", textAlign: "center" }}>
  ¡Este texto tiene estilo JSX!
</p>
```
Pero es mejor práctica guardar los estilos en una constante si los vas a reutilizar o si son muchos. 

#### 📄 Ejemplo 4: fragmentos y múltiples elementos

JSX solo puede devolver un elemento padre, así que usamos un contenedor (div, section) o un fragmento:

```jsx
function Fragmento() {
  return (
    <>
      <h2>Título</h2>
      <p>Parrafo debajo del título</p>
    </>
  );
}
```

✅ ¿Qué hace este componente?

Este componente devuelve dos elementos HTML consecutivos sin necesidad de envolverlos en un ```div```.
Gracias a los fragmentos (```<> </>```), se puede agrupar múltiples elementos sin añadir nodos extra al DOM.

🧠 ¿Por qué es importante?

JSX solo permite retornar un único nodo raíz.
Eso quiere decir que este código no funcionaría:

```jsx
return (
  <h2>Título</h2>
  <p>Texto</p>
);
```

Tienes dos opciones para solucionarlo:
1. Usar un contenedor como ```<div>```, ```<section>```, etc.
2. Usar un fragmento vacío: ```<> ... </>``` (como en el ejemplo)

💡 ¿Cuándo usar fragmentos?

* Cuando no necesitas un div visualmente, pero React te obliga a agrupar.
* Evitas generar elementos HTML innecesarios que podrían afectar el diseño o el DOM.

✅ Alternativa más explícita:
También puedes usar la forma completa de React.Fragment:

```jsx
return (
  <React.Fragment>
    <h2>Título</h2>
    <p>Texto</p>
  </React.Fragment>
);
```

### 🎯 Ejercicios para ti:

🧩 Ejercicio 1:
Crea un componente llamado BienvenidaJSX que:
* Declare una variable usuario = "María".
* Devuelva un div con un saludo: "Hola, María. Bienvenida a React" (usando interpolación con {}).

🧩 Ejercicio 2:
Crea un componente SumaJSX que:
* Declare dos variables a = 5, b = 7
* Muestra un párrafo que diga:
"El resultado de 5 + 7 es: 12"
(usando la suma dentro del JSX con {a + b})

🧩 Ejercicio 3:
Crea un componente TarjetaUsuario que:
* Declare un objeto usuario = { nombre: "Ana", edad: 25 }
* Devuelva un div con un título y un párrafo mostrando:
	* Nombre del usuario
	* Edad del usuario
* Usa estilos en línea para darle color al texto

🧩 Ejercicio 4 (Bonus):
Crea un componente ComponenteCondicional que:
* Reciba una prop llamada admin
* Si admin es true, muestra: "Tienes acceso total"
* Si false, muestra: "Acceso limitado"
* Usa un operador ternario dentro del JSX

---
<a name="modulo-4-componentes-funcionales-y-de-clase"></a>
## 📘 Módulo 4: Componentes (Funcionales y de Clase)

### ❓ ¿Qué es un componente en React?

Un componente es una pieza reutilizable de la interfaz de usuario. En React, todo se basa en componentes. Puedes pensar en ellos como bloques de LEGO que se combinan para construir toda tu aplicación.

Cada componente:

* Encapsula su propia lógica y vista.
* Se puede reutilizar múltiples veces.
* Puede recibir datos mediante props y manejar su propio estado.

### 🧱 Tipos de componentes

1. Componentes funcionales (los más comunes actualmente)

Son funciones de JavaScript que devuelven JSX. Se utilizan junto con [hooks](#modulo-6-estado-con-usestate) (useState, useEffect, etc).

```jsx
function Tarjeta() {
  return <p>Componente funcional</p>;
}
```

2. Componentes de clase (en desuso, pero útiles de conocer)
   
Son clases que extienden ```React.Component``` y tienen un método ```render()```.

```import React, { Component } from 'react'```;

```jsx
class TarjetaClase extends React.Component {
  render() {
    return <p>Componente de clase</p>;
  }
}
```

Hoy en día se recomienda usar componentes funcionales con [hooks](#modulo-6-estado-con-usestate) porque son más sencillos y modernos.

### 📢 Convenciones

* Los componentes deben tener su nombre en mayúscula inicial (ej: Saludo, no saludo).
* Un archivo por componente es una buena práctica (por ejemplo, Saludo.js).
* Siempre deben retornar un solo elemento padre (por eso usamos  o React fragments).

### 🧪 Ejemplo básico:

```jsx
function Tarjeta() {
 return (
	### React es genial 😎 Este es un componente funcional
 );
}
```

Este componente puede usarse dentro de otro componente como si fuera una etiqueta HTML

### 🎯 Ejercicio para ti:

1. Crea un componente llamado PerfilUsuario.
2. Dentro de él, muestra lo siguiente:
* Un título ##  con el texto “Perfil del usuario”.
* Un párrafo  con el nombre ficticio de un usuario.
* Importa y usa el componente dentro de App.js.

---
<a name="modulo-5-props-propiedades-entre-componentes"></a>
## 📘 Módulo 5: Props (Propiedades entre componentes)

### ❓ ¿Qué son las Props?

Las props (abreviatura de “properties”) son la forma de pasar datos entre componentes en React. Son similares a los parámetros de una función, pero aplicados a los componentes.
Las props hacen que los componentes sean reutilizables y dinámicos, ya que permiten cambiar el contenido mostrado sin modificar el propio componente.

### 🧩 ¿Cómo funcionan?

Cuando usas un componente como una etiqueta HTML, puedes pasarle valores como si fueran atributos:

```jsx
<Bienvenida nombre="Carlos" />
```

Dentro del componente, accedes a ese valor usando props:

```jsx
function Bienvenida(props) {
  return <h3>Hola, {props.nombre}</h3>;
}
```

### 🔁 Reutilización con props

```jsx
<Bienvenida nombre="Ana" />
<Bienvenida nombre="Luis" />
<Bienvenida nombre="Sofía" />
```

Los tres mostrarán un mensaje personalizado gracias al valor de props.nombre.

### ⚠️ Importante

*Las props son de solo lectura. No debes modificarlas dentro del componente.
*Puedes pasar strings, números, funciones, objetos e incluso otros componentes como props.

### 🧪 Ejemplo básico:

```jsx
function Usuario(props) {
  return (
    <div>
      <h2>{props.nombre}</h2>
      <p>Edad: {props.edad}</p>
    </div>
  );
}
```
Uso del componente:

```jsx
<Usuario nombre="María" edad={29} />
```

### 🎯 Ejercicio para ti:

1. Crea un componente llamado ```Producto```.
2. Recibirá por props: ```nombre```, ```precio``` y ```disponible```.
3. Mostrará la información dentro de un ```div``` con un ```h3``` y dos párrafos.
4. Usa el componente al menos 2 veces con datos diferentes dentro de ```App.js```.

---
<a name="modulo-6-estado-con-usestate"></a>
## 📘 Módulo 6: Estado con useState

### ❓ ¿Qué es el estado en React?

El estado es como la "memoria" de un componente. Permite que React guarde y actualice información dinámica que puede cambiar con el tiempo: clics, entradas de usuario, datos traídos de una API, etc.
En componentes funcionales, usamos el hook ```useState()``` para gestionar el estado.

### ❓ ¿Qué es un hook?

Un hook es una función especial de React que permite usar características avanzadas (como estado, ciclo de vida, etc.) en componentes funcionales. ```useState``` es el más básico y usado.

### 📦 Sintaxis de useState

```
const [estado, setEstado] = useState(valorInicial);
```

* ```estado```: la variable que contiene el valor actual.
* ```setEstado```: función que usamos para actualizar el valor.
* ```useState(valorInicial)```: le pasamos el valor con el que queremos empezar.


### 🧪 Ejemplo básico: un contador

```jsx
import { useState } from "react";

function Contador() {
  const [contador, setContador] = useState(0);

  return (
    <div>
      <p>Contador: {contador}</p>
      <button onClick={() => setContador(contador + 1)}>Sumar</button>
      <button onClick={() => setContador(0)}>Reiniciar</button>
    </div>
  );
}

```
Este componente guarda el número actual del contador en su estado, y lo actualiza al hacer clic en los botones.

### 🎯 Ejercicio para ti:

1. Crea un componente llamado Likes.
2. Usa useState para llevar un conteo de "me gusta".
3. Agrega un botón con el texto “👍 Me gusta”.
4. Cada clic debe incrementar el número de likes.
5. Muestra el texto: “Este post tiene X me gusta”.

---
<a name="modulo-7-Eventos-en-React"></a>
## 📘 Módulo 7: Eventos en React

### ❓ ¿Qué son los eventos en React?

Los eventos en React funcionan de forma muy similar a los eventos en JavaScript puro (como ```onclick```, ```onchange```, etc.), pero con una sintaxis adaptada a JSX y al estilo declarativo de React.

Los eventos nos permiten ejecutar funciones cuando el usuario interactúa con la aplicación: al hacer clic, escribir en un campo, mover el mouse, etc.

### 🔁 ¿Cómo se usan los eventos en React?

Se escriben en camelCase: ```onClick```, ```onChange```, ```onSubmit```, etc.
Se pasan funciones como manejadores de eventos.
Puedes usar funciones declaradas o funciones flecha ```(arrow functions)```.

### 🧪 Ejemplo básico: botón que muestra una alerta

```jsx
function EventoClick() {
 const manejarClick = () => {
 alert("¡Haz hecho clic!");
 };

 return Haz clic aquí;
}
```
Aquí, ```onClick={manejarClick}``` está diciendo: “Cuando hagan clic, ejecuta esta función”.

### 📋 Otros eventos comunes en React:

| Evento        | Acción                             |
|---------------|------------------------------------|
| `onClick`     | Cuando el usuario hace clic        |
| `onChange`    | Cuando cambia el valor de un input |
| `onSubmit`    | Cuando se envía un formulario      |
| `onMouseOver` | Cuando el mouse pasa sobre un elemento |

### 🧪 Ejemplo avanzado: captura de texto en un input

import { useState } from "react";

```jsx
function InputNombre() {
 const [nombre, setNombre] = useState("");

 const manejarCambio = (e) => {
 setNombre(e.target.value);
 };

 return (


Tu nombre es: {nombre}

 );
}
```
### 🎯 Ejercicio para ti:

1. Crea un componente llamado ```FormularioCorreo```.
2. Tendrá un ```input``` para escribir el correo electrónico.
3. Muestra el texto debajo en tiempo real: "Tu correo es: [correo]".
4. Usa el evento ```onChange``` para capturar el valor.

---
<a name="modulo-8-useEffect-ciclo-de-vida-y-efectos-secundarios"></a>
## 📘 Módulo 8: useEffect – Ciclo de vida y efectos secundarios

### ❓ ¿Qué es useEffect?

useEffect es un hook que te permite ejecutar código en momentos específicos del ciclo de vida del componente.
Es útil para realizar efectos secundarios, como:
Llamadas a una API
Interacción con el DOM
Suscripciones, temporizadores, listeners, etc.

### 🔁 ¿Cuándo se ejecuta useEffect?

Por defecto, useEffect se ejecuta después de cada renderizado. Pero puedes controlar cuándo se ejecuta usando un segundo argumento: el array de dependencias.

### 📦 Sintaxis básica

```jsx
useEffect(() => {
 // Código que se ejecuta después del render
}, []);
```

* Si pasas un array vacío ```[]```, el efecto se ejecuta una sola vez al montar el componente (como ```componentDidMount```).
* Si incluyes variables dentro del array, se ejecutará cada vez que esas variables cambien.

### 🧪 Ejemplo básico: mensaje en consola al montar

import { useEffect } from "react";

```jsx
function Temporizador() {
 useEffect(() => {
 console.log("Componente montado");
 }, []);

 return Observa la consola;
}
```
### 🧪 Ejemplo básico: contador automático

import { useEffect, useState } from "react";

```jsx
function ContadorAutomatico() {
 const [contador, setContador] = useState(0);

 useEffect(() => {
 const intervalo = setInterval(() => {
 setContador((prev) => prev + 1);
 }, 1000);

 // Limpieza del efecto al desmontar
 return () => clearInterval(intervalo);
 }, []);

 return Contador automático: {contador};
}
```
### 🎯 Ejercicio para ti:

1. Crea un componente llamado ```Reloj```.
2. Usa ```useEffect``` para actualizar la hora actual cada segundo.
3. Muestra el resultado en pantalla con formato: ```HH:MM:SS```.

---
<a name="modulo-9-estilos-en-react"></a>
## 📘 Módulo 9: Estilos en React

### ❓ ¿Cómo se aplican estilos en React?

React no impone un único método para aplicar estilos. Puedes usar:

1. CSS tradicional (importado)
2. Estilos en línea (inline styles)
3. CSS Modules
4. Frameworks y librerías externas (Tailwind, Bootstrap, styled-components...)

#### 🎨 **Opción 1: CSS tradicional**

Puedes crear un archivo ```.css``` y importarlo en el componente.

<img src="https://img.icons8.com/?size=100&id=21278&format=png&color=000000" alt="CSS3 Logo" width="60"/>

```css
/* archivo: estilos.css */
.titulo {
 color: royalblue;
 font-size: 2rem;
}
```

<img src="https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png" alt="JavaScript Logo" width="40"/>

```jsx
import "./estilos.css";

function Encabezado() {
  return <h1 className="titulo">¡Hola desde CSS tradicional!</h1>;
}

```

#### 🖌️ **Opción 2: Estilos en línea (inline)**

Son útiles para estilos rápidos y dinámicos.

```jsx
function Boton() {
 const estilo = {
 backgroundColor: "tomato",
 padding: "10px",
 border: "none",
 color: "white",
 borderRadius: "8px"
 };

 return Haz clic;
}
```
Nota: los nombres de propiedades se escriben en camelCase (por ejemplo, backgroundColor, no background-color).

#### 🧩 **Opción 3: CSS Modules**

Permite aplicar estilos aislados por componente (evita conflictos).

```jsx
// archivo: Titulo.module.css
.tituloEspecial {
 color: green;
 text-transform: uppercase;
}
```

```jsx
// componente: Titulo.jsx
import styles from "./Titulo.module.css";


function Titulo() {
 return Hola desde CSS Module;
}
```

### 💡 ¿Cuál elegir?

* Para proyectos pequeños: CSS tradicional o inline.
* Para grandes: CSS Modules o frameworks modernos.


### 🧪 Ejemplo básico:

```jsx
function MensajeEstilizado() {
 return (

 ¡Este párrafo tiene estilo en línea!

 );
}
```

### 🎯 Ejercicio para ti:

1. Crea un componente llamado ```Alerta```.
2. Aplica estilos en línea para que se vea como un mensaje de advertencia:
* Fondo amarillo
* Texto en rojo oscuro
* Padding de ```1rem```
3. Haz que se muestre en pantalla al renderizar el componente.

---
<a name="modulo-10-listas-y-claves"></a>
## 📘 Módulo 10: Listas y Claves

### ❓ ¿Qué son las listas en React?

En React puedes mostrar listas de elementos (como productos, tareas, usuarios, etc.) utilizando el método ```.map()``` de JavaScript para recorrer un array y crear un componente o elemento por cada dato.

#### ❓ ¿Qué son las "claves" o keys?

Cuando renderizas listas, React necesita identificar cada elemento individual. Por eso, se requiere una key única para cada uno, así puede saber cuál ha cambiado, agregado o eliminado.
Si no usas keys, React lanzará una advertencia y tu app puede comportarse de forma inesperada al actualizarse.

### 🧪 Ejemplo básico: lista de frutas
```jsx
const frutas = ["🍎 Manzana", "🍌 Banana", "🍇 Uva", "🍊 Naranja"];

function ListaFrutas() {
 return (

 {frutas.map((fruta, index) => (
 * {fruta}

 ))}


 );
}
```
En este ejemplo usamos el índice del array como key (```key={index}```), aunque lo mejor es usar un id único si lo tienes disponible.

### 📦 Ejemplo con objetos:

```jsx
const productos = [
 { id: 1, nombre: "Camisa", precio: 25 },
 { id: 2, nombre: "Pantalón", precio: 40 },
 { id: 3, nombre: "Zapatos", precio: 60 }
];


function ListaProductos() {
 return (

 {productos.map((producto) => (
 * 
 {producto.nombre} - ${producto.precio}

 ))}


 );
}
```

### 🎯 Ejercicio para ti:

1. Crea un componente llamado ```ListaTareas```.
2. Declara un array de objetos con ```id``` y ```texto```.
3. Muestra las tareas en una lista ```<ul>```.
4. Usa ```key={tarea.id}``` en cada ```<li>```.
   
---
<a name="modulo-11-formularios-en-react"></a>
## 📘 Módulo 11: Formularios en React


### ❓ ¿Qué es un formulario controlado?

Un formulario controlado en React es aquel donde los campos (```input```, ```textarea```, ```select```) están vinculados al estado del componente.

Esto significa que el valor del input depende de ```useState```, y cualquier cambio en el input actualiza ese estado.


### 🔄 ¿Por qué usar formularios controlados?

* Permite validar en tiempo real.
* Puedes limpiar el formulario fácilmente.
* Facilita la lógica al enviar datos a una API.
* React controla todo el proceso.

### 🧪 Ejemplo básico: formulario de nombre

```jsx
import { useState } from "react";

function FormularioNombre() {
 const [nombre, setNombre] = useState("");

 const manejarEnvio = (e) => {
 e.preventDefault(); // evita recargar la página
 alert(`Nombre enviado: ${nombre}`);
 setNombre(""); // limpiar campo
 };

 return (

 setNombre(e.target.value)}
 />
 Enviar

 );
}
```

### 📌 Reglas clave para formularios en React

* Usa useState para cada campo del formulario.
* El atributo value del input debe estar enlazado con el estado.
* Usa onChange para actualizar el estado cuando el usuario escriba.
* Controla el onSubmit del formulario con una función.

### 💡 Mejora: múltiples campos

```jsx
const [formulario, setFormulario] = useState({ nombre: "", email: "" });

const manejarCambio = (e) => {
 setFormulario({ ...formulario, [e.target.name]: e.target.value });
};
Esto permite manejar varios campos con una sola función.
```

### 🎯 Ejercicio para ti:

1. Crea un componente FormularioContacto.
2. Debe tener campos: nombre, email, mensaje.
3. Al hacer submit, muestra un alert con los datos.
4. Usa useState para controlar los valores.
5. Limpia el formulario después de enviarlo.

---
<a name="modulo-12-lifting-state-up-y-comunicacion-entre-componentes"></a>
## 📘 Módulo 12: Lifting State Up y comunicación entre componentes

### ❓ ¿Qué es “Lifting State Up”?

En React, el estado se maneja desde el componente que necesita conocer o controlar un dato. Pero cuando varios componentes necesitan acceder o modificar un mismo estado, lo ideal es elevar (lift up) ese estado al ancestro común.
Es decir, el estado se mueve “hacia arriba” en la jerarquía de componentes para que pueda ser compartido por varios hijos.

### 🔁 ¿Cuándo usar Lifting State Up?

* Cuando un componente hijo necesita enviar información al padre.
* Cuando dos componentes hermanos necesitan acceder al mismo estado.


### 🧪 Ejemplo básico: contador controlado desde el padre

```jsx
import { useState } from "react";

function BotonIncrementar({ onClick }) {
  return <button onClick={onClick}>Incrementar</button>;
}

function MostrarContador({ valor }) {
  return <p>Valor actual: {valor}</p>;
}

function ContadorConLifting() {
  const [contador, setContador] = useState(0);

  const incrementar = () => setContador(contador + 1);

  return (
    <div>
      <MostrarContador valor={contador} />
      <BotonIncrementar onClick={incrementar} />
    </div>
  );
}
```


### 📡 Comunicación descendente y ascendente

**Padre → Hijo**: usando ```props```
**Hijo → Padre**: usando una función que el padre pasa como prop


### 🎯 Ejercicio para ti:

1. Crea un componente padre llamado FormularioColor.
2. Este tendrá un input donde el usuario escriba un color (rojo, blue, etc.).
3. Pasa ese valor a un componente hijo llamado CajaColor que pinte un div con el color recibido.
4. Usa useState y props para conectar ambos.

---
<a name="modulo-13-react-router-navegacion-entre-paginas"></a>
## 📘 Módulo 13: React Router – Navegación entre páginas

### ❓ ¿Qué es React Router?

React Router es una librería oficial que permite agregar rutas y navegación a aplicaciones hechas con React.
En una SPA (Single Page Application), aunque todo corre en una sola página, podemos simular múltiples “páginas” gracias a React Router.

### 📦 ¿Qué podemos hacer con React Router?

* Crear rutas y subrutas (/home, /perfil, /producto/:id)
* Cambiar la vista sin recargar la página
* Navegar con enlaces
* Redirecciones, rutas protegidas, navegación programática...

### 🚀 Instalación

Desde la terminal, en el proyecto React:

```bash
npm install react-router-dom
```

### 🔁 Conceptos clave

* ```<BrowserRouter>```: debe envolver toda la app (generalmente en ```index.js``` o ```App.js```)
* ```<Routes>```: contenedor de todas las rutas
* ```<Route>```: define una ruta
* ```<Route>```: navegación sin recargar
* ```useNavigate()```: navegación desde código

### 🧪 Ejemplo básico:

import {
 BrowserRouter as Router,
 Routes,
 Route,
 Link
} from "react-router-dom";

```jsx
import {
  BrowserRouter as Router,
  Routes,
  Route,
  Link
} from "react-router-dom";

function Home() {
  return <h2>Inicio</h2>;
}

function Acerca() {
  return <h2>Acerca de</h2>;
}

function Navegacion() {
  return (
    <nav>
      <Link to="/">Inicio</Link> | <Link to="/acerca">Acerca</Link>
    </nav>
  );
}

function AppRouter() {
  return (
    <Router>
      <Navegacion />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/acerca" element={<Acerca />} />
      </Routes>
    </Router>
  );
}

``` 
### 🎯 Ejercicio para ti:

1. Crea tres componentes: ```Inicio```, ```Servicios``` y ```Contacto```.
2. Configura rutas ```/```, ```/servicios``` y ```/contacto```.
3. Crea una barra de navegación con ```<Link>``` para cambiar entre ellos.
4. Bonus: agrega estilos para destacar la página actual.

---
<a name="modulo-14-consumo-de-apis-con-fetch-o-axios"></a>
## 📘 Módulo 14: Consumo de APIs con fetch o Axios

### ❓ ¿Qué es una API?

Una API (Application Programming Interface) permite que nuestra app React se comunique con servidores externos y obtenga o envíe datos, como usuarios, productos, publicaciones, etc.

En React, solemos usar ```fetch()``` o librerías como ```axios``` para hacer peticiones HTTP (GET, POST, PUT, DELETE...).

### 📦 Opciones populares

```fetch()```: viene con JavaScript por defecto.
```axios```: librería externa más amigable (instalar con ```npm install axios```).

### 💡 ¿Dónde usamos la petición?

Usamos el hook ```useEffect()``` para hacer la petición una vez que el componente se monte.

### 🧪 Ejemplo básico con fetch() – Obtener usuarios:

```jsx
import { useState, useEffect } from "react";

function ListaUsuarios() {
 const [usuarios, setUsuarios] = useState([]);
 const [cargando, setCargando] = useState(true);

 useEffect(() => {
 fetch("https://jsonplaceholder.typicode.com/users")
 .then((res) => res.json())
 .then((data) => {
 setUsuarios(data);
 setCargando(false);
 });
 }, []);

 if (cargando) return Cargando usuarios...;

 return (


	 {usuarios.map((usuario) => (
	 + {usuario.name}

	 ))}
 );
}
```

### 🎯 Ejercicio para ti:

1. Crea un componente ```ListaPosts```.
2. Usa ```fetch``` para obtener datos de ```https://jsonplaceholder.typicode.com/posts```.
3. Muestra los títulos (```title```) en pantalla.
4. Agrega un mensaje de "Cargando..." mientras se obtienen los datos.

---
<a name="modulo-15-custom-hooks"></a>
## 📘 Módulo 15: Custom Hooks

### ❓ ¿Qué es un Custom Hook?

Un Custom Hook es una función de JavaScript que empieza con use y puede usar otros hooks internos (useState, useEffect, etc.). Nos permite extraer lógica reutilizable y compartirla entre varios componentes.
Si encuentras que estás copiando y pegando useEffect, useState, etc. en varios componentes, ¡es hora de crear un hook personalizado!


### 🧠 ¿Cómo se crea?

Un Custom Hook:
1. Es una función que empieza con use.
2. Usa hooks dentro (como useState, useEffect).
3. Devuelve valores o funciones que quieras reutilizar.

### 🧪 Ejemplo básico: Hook para obtener datos de una API

```jsx
import { useState, useEffect } from "react";

function useFetch(url) {
 const [datos, setDatos] = useState([]);
 const [cargando, setCargando] = useState(true);

 useEffect(() => {
 fetch(url)
 .then((res) => res.json())
 .then((data) => {
 setDatos(data);
 setCargando(false);
 });
 }, [url]);

 return { datos, cargando };
}
```

### 📦 Ejemplo básico: Usando el Custom Hook

```jsx
function ListaComentarios() {
 const { datos: comentarios, cargando } = useFetch("https://jsonplaceholder.typicode.com/comments");

 if (cargando) return Cargando comentarios...;

 return (


	 {comentarios.slice(0, 5).map((comentario) => (
	 + {comentario.name}

	 ))}
 );
}
```

### 🎯 Ejercicio para ti:

1. Crea un hook llamado useContador que:
2. Reciba un valor inicial
3. Devuelva el valor y una función para incrementarlo
4. Úsalo dentro de un componente llamado ContadorPersonalizado.

---
<a name="modulo-16-context-api"></a>
## 📘 Módulo 16: Context API – Manejo global del estado

### ❓ ¿Qué es Context API?

Context API es una herramienta nativa de React que permite crear un estado global al que cualquier componente de tu aplicación puede acceder o modificar, sin importar dónde esté ubicado en el árbol de componentes.
Es ideal para manejar temas globales como: autenticación, idioma, tema oscuro/claro, carrito de compras, usuario actual, etc.


#### ⚙️ ¿Cómo funciona?

1. Crear el contexto
2. Proveer el contexto
3. Consumir el contexto

### 🧪 Ejemplo básico: paso a paso: Tema (oscuro/claro)

1. Crear el contexto:
   
```jsx
import { createContext } from "react";

export const TemaContexto = createContext();
```

2. Crear el proveedor:
   
```jsx
import { useState } from "react";
import { TemaContexto } from "./TemaContexto";

export function TemaProvider({ children }) {
  const [tema, setTema] = useState("claro");

  const alternarTema = () => {
    setTema((prev) => (prev === "claro" ? "oscuro" : "claro"));
  };

  return (
    <TemaContexto.Provider value={{ tema, alternarTema }}>
      {children}
    </TemaContexto.Provider>
  );
}

```

3. Usar el contexto desde un componente:

```jsx
import { useContext } from "react";
import { TemaContexto } from "./TemaContexto";

function BotonTema() {
  const { tema, alternarTema } = useContext(TemaContexto);

  return (
    <button onClick={alternarTema}>
      Cambiar a modo {tema === "claro" ? "oscuro" : "claro"}
    </button>
  );
}

```

4. Envolver la app con el Provider
   
import { TemaProvider } from "./TemaProvider";

```jsx
import { TemaProvider } from "./TemaProvider";

function App() {
  return (
    <TemaProvider>
      <BotonTema />
      {/* otros componentes */}
    </TemaProvider>
  );
}
```

### 🎯 Ejercicio para ti:

1. Crea un contexto llamado UsuarioContexto.
2. En el proveedor, define un nombre de usuario ("Juan").
3. Crea un componente PerfilUsuario que muestre: “Bienvenido, Juan”.
4. Usa useContext para obtener el nombre desde el contexto.

---
<a name="modulo-17-introduccion-a-redux"></a>
## 📘 Módulo 17: Introducción a Redux (opcional)


### ❓ ¿Qué es Redux?

Redux es una librería de manejo de estado global. Es más poderosa y estructurada que Context API, ideal cuando:

* La aplicación es grande y compleja.
* Muchos componentes comparten y modifican el mismo estado.
* Necesitas depuración, trazabilidad y control total del flujo de datos.

Se basa en un único estado global inmutable, y para modificarlo usamos acciones y reducers.


### 🔁 Principios clave de Redux

1. Store: el estado global centralizado.
2. Actions: objetos que describen qué ocurrió.
3. Reducers: funciones que actualizan el estado según la acción.
4. Dispatch: método para lanzar acciones.
5. useSelector: permite acceder al estado.
6. useDispatch: permite lanzar acciones.

### 🚀 Instalación (con React)

```bash
npm install @reduxjs/toolkit react-redux
```

### 🧪 Ejemplo básico con Redux Toolkit (recomendado)

1. Crear el slice:

```jsx
// contadorSlice.js
import { createSlice } from '@reduxjs/toolkit';

const contadorSlice = createSlice({
  name: 'contador',
  initialState: 0,
  reducers: {
    incrementar: (state) => state + 1,
    reiniciar: () => 0
  }
});

export const { incrementar, reiniciar } = contadorSlice.actions;
export default contadorSlice.reducer;
```

2. Configurar el store:

```jsx
// store.js
import { configureStore } from '@reduxjs/toolkit';
import contadorReducer from './contadorSlice';

export const store = configureStore({
  reducer: {
    contador: contadorReducer
  }
});
```

3. Proveer el store a tu app:
   
```jsx
// index.js
import { Provider } from 'react-redux';
import { store } from './store';
import App from './App';

<Provider store={store}>
  <App />
</Provider>
```

4. Usar Redux en un componente

```jsx
import { useSelector, useDispatch } from 'react-redux';
import { incrementar, reiniciar } from './contadorSlice';

function ContadorRedux() {
  const contador = useSelector((state) => state.contador);
  const dispatch = useDispatch();

  return (
    <div>
      <p>Contador Redux: {contador}</p>
      <button onClick={() => dispatch(incrementar())}>Incrementar</button>
      <button onClick={() => dispatch(reiniciar())}>Reiniciar</button>
    </div>
  );
}

```

### 🎯 Ejercicio para ti:

1. Crea un contador con Redux Toolkit.
2. Agrega botones para ```+1```, ```-1```, y ```reiniciar```.
3. Usa ```useSelector``` y ```useDispatch``` para manejarlo.

---
<a name="modulo-18-deploy-de-la-aplicacion-react"></a>
## 📘 Módulo 18: Deploy de la aplicación React

### ❓ ¿Qué es el Deploy?

Hacer deploy significa subir tu app a internet. Es decir, transformarla desde tu entorno local en una página web accesible desde cualquier lugar.

### 🌐 Opciones para publicar una app React

1. Vercel (recomendado)
2. Netlify
3. GitHub Pages
4. Render, Firebase Hosting, AWS, etc.

Nosotros usaremos Vercel porque es fácil, rápido y gratuito.

### 🚀 Paso a paso: Deploy con Vercel

1. Subir tu app a GitHub

* Si aún no tienes cuenta en GitHub, créala.
* Crea un repositorio nuevo.
* Sube tu proyecto (git init, git add ., git commit, git push).

2. Crear cuenta en vercel.com

* Inicia sesión con tu cuenta de GitHub.
* Haz clic en "Add New Project".
* Selecciona el repositorio con tu app React.
* Vercel detectará que es React y hará la configuración automáticamente.
* Haz clic en "Deploy".

✅ ¡Listo! En unos segundos tendrás un link público como:

```https://mi-app-react.vercel.app```


### ⚙️ Bonus: ¿y si usas create-react-app?

Cuando usas npm run build, se genera una carpeta build/ con los archivos listos para producción.

```bash
npm run build
```

Puedes subir esos archivos a cualquier servidor o usar herramientas como:

* GitHub Pages (requiere configuración)
* Netlify Drop (solo arrastras la carpeta ```build```)


### 🎯 Ejercicio para ti:

1. Sube tu proyecto a GitHub.
2. Haz deploy con Vercel.
3. Comparte el link de tu app con tus amigos o clientes.


