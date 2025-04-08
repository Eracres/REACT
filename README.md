# 🧑‍🏫 Curso de React – Desarrollo de Aplicaciones Web con React

## 🗂️ Temario General del Curso

1. Introducción a React  
2. Configuración del entorno de desarrollo  
3. JSX: Sintaxis especial de React  
4. Componentes (Funcionales y de Clase)  
5. Props (Propiedades entre componentes)  
6. Estado (useState)  
7. Eventos en React  
8. Ciclo de vida y useEffect  
9. Estilos en React  
10. Listas y claves  
11. Formularios en React  
12. Lifting State Up y comunicación entre componentes  
13. React Router (Navegación entre páginas)  
14. Consumo de APIs con fetch o Axios  
15. Custom Hooks  
16. Context API (Manejo global del estado)  
17. Introducción a Redux (opcional, si quieres profundizar)  
18. Deploy de la aplicación React  

---

## 📘 Módulo 1: Introducción a React

### ❓ ¿Qué es React?

React es una biblioteca de JavaScript creada por Facebook para construir interfaces de usuario. Su objetivo principal es crear aplicaciones web reactivas, eficientes y modulares.

### 💡 Ventajas clave:
- Componentes reutilizables
- Virtual DOM (mejora el rendimiento)
- Flujo de datos unidireccional (unidirectional data flow)
- Ideal para SPAs (Single Page Applications)


### 🧪 Ejemplo simple:

```jsx
function HolaMundo() {
 return # ¡Hola, mundo desde React!;
}
```

Esto sería un componente muy básico en React.


### 🎯 Ejercicio para ti:

Crea un componente llamado Saludo que muestre el mensaje, "¡Bienvenido al curso de React!".

---

## 📘 Módulo 2: Configuración del Entorno de Desarrollo

### ❓ ¿Cómo empezar con React?

Para desarrollar con React de forma profesional, lo ideal es tener un entorno que nos permita comenzar rápido, sin perder tiempo en configuraciones innecesarias. Para eso existe una herramienta oficial: Create React App.
Create React App es un scaffolding tool que genera un proyecto React completo, listo para empezar, con todo configurado: Babel, Webpack, React y más.

### 🛠️ Cómo crear tu primer proyecto React:

* Instalar Node.js y npm, para comprobar si estan instalados, usar estos comandos:

 ```bash
node -v
npm -v
``` 

* Abre tu terminal (en VS Code o donde prefieras).

* Ejecuta el siguiente comando:
   
```bash
npx create-react-app mi-app
```

* Entra en el nuevo directorio del proyecto:

```bash
cd mi-app
```

* Inicia el servidor de desarrollo:

```bash
npm start
```

Esto abrirá automáticamente el navegador en http://localhost:3000 con tu aplicación React funcionando. ¡Ya tienes tu primer entorno ⚛️ montado!

### 🗂️ Estructura básica del proyecto

```
mi-app/
├── public/ → contiene el HTML principal (index.html)
├── src/ → aquí irá todo tu código React
│ ├── App.js → componente principal de la aplicación
│ └── index.js → punto de entrada que renderiza App.js
├── package.json → contiene dependencias y scripts
```

### 🧼 Recomendación como desarrollador:

Al empezar un nuevo proyecto, te recomiendo limpiar el código inicial que trae App.js, App.css, y borrar logo.svg. Así puedes construir tu aplicación desde cero con total control.

### 🧪 Ejemplo de inicio:

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

### 🧪 Ejemplo simple:

```jsx
function ComponenteJSX() {
 const nombre = "React";
 return (# Hola desde {nombre} ¡Esto es JSX funcionando!);
}
```

Este componente mezcla código JavaScript (```const nombre = "React"```) con etiquetas JSX (parecidas a HTML). Lo que aparece entre llaves {} dentro del JSX es interpretado como una expresión de JavaScript.

### 🎯 Ejercicio para ti:

Crea un componente llamado BienvenidaJSX que:

1. Declare una variable usuario = "María".
2. Devuelva un div con un saludo que diga: "Hola, María. Bienvenida a React".
3. El texto debe construirse utilizando interpolación con {}.

---

## 📘 Módulo 4: Componentes (Funcionales y de Clase)

### ❓ ¿Qué es un componente en React?

Un componente es una pieza reutilizable de la interfaz de usuario. En React, todo se basa en componentes. Puedes pensar en ellos como bloques de LEGO que se combinan para construir toda tu aplicación.

Cada componente:

* Encapsula su propia lógica y vista.
* Se puede reutilizar múltiples veces.
* Puede recibir datos mediante props y manejar su propio estado.

### 🧱 Tipos de componentes

1. Componentes funcionales (los más comunes actualmente)

Son funciones de JavaScript que devuelven JSX. Se utilizan junto con hooks (useState, useEffect, etc).

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

### 🧪 Ejemplo simple:

```jsx
function Tarjeta() {
 return (### React es genial 😎 Este es un componente funcional);
}
```

Este componente puede usarse dentro de otro componente como si fuera una etiqueta HTML:

### 🎯 Ejercicio para ti:

1. Crea un componente llamado PerfilUsuario.
2. Dentro de él, muestra lo siguiente:
* Un título ##  con el texto “Perfil del usuario”.
* Un párrafo  con el nombre ficticio de un usuario.
* Importa y usa el componente dentro de App.js.

---

## 📘 Módulo 5: Props (Propiedades entre componentes)

### ❓ ¿Qué son las Props?

Las props (abreviatura de “properties”) son la forma de pasar datos entre componentes en React. Son similares a los parámetros de una función, pero aplicados a los componentes.
Las props hacen que los componentes sean reutilizables y dinámicos, ya que permiten cambiar el contenido mostrado sin modificar el propio componente.

### 🧩 ¿Cómo funcionan?

Cuando usas un componente como una etiqueta HTML, puedes pasarle valores como si fueran atributos:

Dentro del componente, accedes a ese valor usando props:

```jsx
function Bienvenida(props) {
 return Hola, {props.nombre};
}
```

### 🔁 Reutilización con props

Los tres mostrarán un mensaje personalizado gracias al valor de props.nombre.

### ⚠️ Importante

Las props son de solo lectura. No debes modificarlas dentro del componente.
Puedes pasar strings, números, funciones, objetos e incluso otros componentes como props.

### 🧪 Ejemplo simple:

```jsx
function Usuario(props) {
 return (

{props.nombre}
Edad: {props.edad}

 );
}
```
Uso del componente:

### 🎯 Ejercicio para ti:

1. Crea un componente llamado Producto.
2. Recibirá por props: nombre, precio y disponible.
3. Mostrará la información dentro de un div con un h3 y dos párrafos.
4. Usa el componente al menos 2 veces con datos diferentes dentro de App.js.

---
<a name="modulo-6-estado-con-usestate"></a>
## 📘 Módulo 6: Estado con useState

### ¿Qué es el estado en React?

El estado es como la "memoria" de un componente. Permite que React guarde y actualice información dinámica que puede cambiar con el tiempo: clics, entradas de usuario, datos traídos de una API, etc.
En componentes funcionales, usamos el hook useState() para gestionar el estado.

#### ❓ ¿Qué es un hook?

Un hook es una función especial de React que permite usar características avanzadas (como estado, ciclo de vida, etc.) en componentes funcionales. useState es el más básico y usado.

**📦 Sintaxis de useState**
```
const [estado, setEstado] = useState(valorInicial);
estado: la variable que contiene el valor actual.
setEstado: función que usamos para actualizar el valor.
useState(valorInicial): le pasamos el valor con el que queremos empezar.
```

#### Ejemplo mío: un contador

import { useState } from "react";

```jsx
function Contador() {
 const [contador, setContador] = useState(0);

 return (

Contador: {contador}
 setContador(contador + 1)}>Sumar
 setContador(0)}>Reiniciar

 );
}
```
Este componente guarda el número actual del contador en su estado, y lo actualiza al hacer clic en los botones.

#### Ejercicio para ti:

Crea un componente llamado Likes.
Usa useState para llevar un conteo de "me gusta".
Agrega un botón con el texto “👍 Me gusta”.
Cada clic debe incrementar el número de likes.
Muestra el texto: “Este post tiene X me gusta”.

---

## 📘 Módulo 7: Eventos en React

### ¿Qué son los eventos en React?

Los eventos en React funcionan de forma muy similar a los eventos en JavaScript puro (como onclick, onchange, etc.), pero con una sintaxis adaptada a JSX y al estilo declarativo de React.
Los eventos nos permiten ejecutar funciones cuando el usuario interactúa con la aplicación: al hacer clic, escribir en un campo, mover el mouse, etc.

#### ¿Cómo se usan los eventos en React?

Se escriben en camelCase: onClick, onChange, onSubmit, etc.
Se pasan funciones como manejadores de eventos.
Puedes usar funciones declaradas o funciones flecha (arrow functions).

#### Ejemplo básico: botón que muestra una alerta

```jsx
function EventoClick() {
 const manejarClick = () => {
 alert("¡Haz hecho clic!");
 };

 return Haz clic aquí;
}
```
Aquí, onClick={manejarClick} está diciendo: “Cuando hagan clic, ejecuta esta función”.

**📋 Otros eventos comunes en React:**

#### Ejemplo avanzado: captura de texto en un input

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
#### Ejercicio para ti:

Crea un componente llamado FormularioCorreo.
Tendrá un input para escribir el correo electrónico.
Muestra el texto debajo en tiempo real: "Tu correo es: [correo]".
Usa el evento onChange para capturar el valor.

---

## 📘 Módulo 8: useEffect – Ciclo de vida y efectos secundarios

### ¿Qué es useEffect?

useEffect es un hook que te permite ejecutar código en momentos específicos del ciclo de vida del componente.
Es útil para realizar efectos secundarios, como:
Llamadas a una API
Interacción con el DOM
Suscripciones, temporizadores, listeners, etc.

**🔁 ¿Cuándo se ejecuta useEffect?**

Por defecto, useEffect se ejecuta después de cada renderizado. Pero puedes controlar cuándo se ejecuta usando un segundo argumento: el array de dependencias.

**📦 Sintaxis básica**

useEffect(() => {
 // Código que se ejecuta después del render
}, []);
Si pasas un array vacío [], el efecto se ejecuta una sola vez al montar el componente (como componentDidMount).
Si incluyes variables dentro del array, se ejecutará cada vez que esas variables cambien.

#### Ejemplo mío: mensaje en consola al montar

import { useEffect } from "react";

```jsx
function Temporizador() {
 useEffect(() => {
 console.log("Componente montado");
 }, []);

 return Observa la consola;
}
```
#### Ejemplo: contador automático

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
#### Ejercicio para ti:

Crea un componente llamado Reloj.
Usa useEffect para actualizar la hora actual cada segundo.
Muestra el resultado en pantalla con formato: HH:MM:SS.

---

## 📘 Módulo 9: Estilos en React

### ¿Cómo se aplican estilos en React?

React no impone un único método para aplicar estilos. Puedes usar:
CSS tradicional (importado)
Estilos en línea (inline styles)
CSS Modules
Frameworks y librerías externas (Tailwind, Bootstrap, styled-components...)

**🎨 Opción 1: CSS tradicional**

Puedes crear un archivo .css y importarlo en el componente.
css
/* archivo: estilos.css */
.titulo {
 color: royalblue;
 font-size: 2rem;
}
import "./estilos.css";

```jsx
function Encabezado() {
 return ¡Hola desde CSS tradicional!;
}
```

🖌️ Opción 2: Estilos en línea (inline)
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


**🧩 Opción 3: CSS Modules**

Permite aplicar estilos aislados por componente (evita conflictos).
// archivo: Titulo.module.css
.tituloEspecial {
 color: green;
 text-transform: uppercase;
}
// componente: Titulo.jsx
import styles from "./Titulo.module.css";

```jsx
function Titulo() {
 return Hola desde CSS Module;
}
```


**💡 ¿Cuál elegir?**

Para proyectos pequeños: CSS tradicional o inline.
Para grandes: CSS Modules o frameworks modernos.


#### Ejemplo mío

```jsx
function MensajeEstilizado() {
 return (

 ¡Este párrafo tiene estilo en línea!

 );
}
```
#### Ejercicio para ti:

Crea un componente llamado Alerta.
Aplica estilos en línea para que se vea como un mensaje de advertencia:
Fondo amarillo
Texto en rojo oscuro
Padding de 1rem
Haz que se muestre en pantalla al renderizar el componente.

---

## 📘 Módulo 10: Listas y Claves

### ¿Qué son las listas en React?

En React puedes mostrar listas de elementos (como productos, tareas, usuarios, etc.) utilizando el método .map() de JavaScript para recorrer un array y crear un componente o elemento por cada dato.

#### ¿Qué son las "claves" o keys?

Cuando renderizas listas, React necesita identificar cada elemento individual. Por eso, se requiere una key única para cada uno, así puede saber cuál ha cambiado, agregado o eliminado.
Si no usas keys, React lanzará una advertencia y tu app puede comportarse de forma inesperada al actualizarse.

#### Ejemplo básico: lista de frutas

const frutas = ["🍎 Manzana", "🍌 Banana", "🍇 Uva", "🍊 Naranja"];

```jsx
function ListaFrutas() {
 return (

 {frutas.map((fruta, index) => (
 * {fruta}

 ))}


 );
}
```
En este ejemplo usamos el índice del array como key (key={index}), aunque lo mejor es usar un id único si lo tienes disponible.

**📦 Ejemplo con objetos**

const productos = [
 { id: 1, nombre: "Camisa", precio: 25 },
 { id: 2, nombre: "Pantalón", precio: 40 },
 { id: 3, nombre: "Zapatos", precio: 60 }
];

```jsx
function ListaProductos() {
 return (

 {productos.map((producto) => (
 * 
 {producto.nombre} - ${producto.precio}

 ))}


 );
}
```

#### Ejercicio para ti:

Crea un componente llamado ListaTareas.
Declara un array de objetos con id y texto.
Muestra las tareas en una lista .
Usa key={tarea.id} en cada * .

---

## 📘 Módulo 11: Formularios en React


### ¿Qué es un formulario controlado?

Un formulario controlado en React es aquel donde los campos (input, textarea, select) están vinculados al estado del componente.
Esto significa que el valor del input depende de useState, y cualquier cambio en el input actualiza ese estado.


**🔄 ¿Por qué usar formularios controlados?**

Permite validar en tiempo real.
Puedes limpiar el formulario fácilmente.
Facilita la lógica al enviar datos a una API.
React controla todo el proceso.


#### Ejemplo básico: formulario de nombre

import { useState } from "react";

```jsx
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

#### Reglas clave para formularios en React

Usa useState para cada campo del formulario.
El atributo value del input debe estar enlazado con el estado.
Usa onChange para actualizar el estado cuando el usuario escriba.
Controla el onSubmit del formulario con una función.


**💡 Mejora: múltiples campos**

const [formulario, setFormulario] = useState({ nombre: "", email: "" });

const manejarCambio = (e) => {
 setFormulario({ ...formulario, [e.target.name]: e.target.value });
};
Esto permite manejar varios campos con una sola función.


#### Ejercicio para ti:

Crea un componente FormularioContacto.
Debe tener campos: nombre, email, mensaje.
Al hacer submit, muestra un alert con los datos.
Usa useState para controlar los valores.
Limpia el formulario después de enviarlo.

---

## 📘 Módulo 12: Lifting State Up y comunicación entre componentes


### ¿Qué es “Lifting State Up”?

En React, el estado se maneja desde el componente que necesita conocer o controlar un dato. Pero cuando varios componentes necesitan acceder o modificar un mismo estado, lo ideal es elevar (lift up) ese estado al ancestro común.
Es decir, el estado se mueve “hacia arriba” en la jerarquía de componentes para que pueda ser compartido por varios hijos.

**📦 ¿Cuándo usar Lifting State Up?**

Cuando un componente hijo necesita enviar información al padre.
Cuando dos componentes hermanos necesitan acceder al mismo estado.


#### Ejemplo: contador controlado desde el padre

import { useState } from "react";

```jsx
function BotonIncrementar({ onClick }) {
 return Incrementar;
}
```

```jsx
function MostrarContador({ valor }) {
 return Valor actual: {valor};
}
```

```jsx
function ContadorConLifting() {
 const [contador, setContador] = useState(0);

 const incrementar = () => setContador(contador + 1);

 return (




 );
}
```


**🔁 Comunicación descendente y ascendente**

Padre → Hijo: usando props
Hijo → Padre: usando una función que el padre pasa como prop


#### Ejercicio para ti:

Crea un componente padre llamado FormularioColor.
Este tendrá un input donde el usuario escriba un color (rojo, blue, etc.).
Pasa ese valor a un componente hijo llamado CajaColor que pinte un div con el color recibido.
Usa useState y props para conectar ambos.

---

## 📘 Módulo 13: React Router – Navegación entre páginas

### ¿Qué es React Router?

React Router es una librería oficial que permite agregar rutas y navegación a aplicaciones hechas con React.
En una SPA (Single Page Application), aunque todo corre en una sola página, podemos simular múltiples “páginas” gracias a React Router.

**📦 ¿Qué podemos hacer con React Router?**

Crear rutas y subrutas (/home, /perfil, /producto/:id)
Cambiar la vista sin recargar la página
Navegar con enlaces
Redirecciones, rutas protegidas, navegación programática...

**🚀 Instalación**

Desde la terminal, en el proyecto React:
npm install react-router-dom

**🔁 Conceptos clave**

: debe envolver toda la app (generalmente en index.js o App.js)
: contenedor de todas las rutas
: define una ruta
: navegación sin recargar
useNavigate(): navegación desde código

#### Ejemplo básico

import {
 BrowserRouter as Router,
 Routes,
 Route,
 Link
} from "react-router-dom";

```jsx
function Home() {
 return Inicio;
}
```

```jsx
function Acerca() {
 return Acerca de;
}
```

```jsx
function Navegacion() {
 return (

Inicio | Acerca

 );
}
```

```jsx
function AppRouter() {
 return (


}
/>
 } />


 );
}
``` 
#### Ejercicio para ti:

Crea tres componentes: Inicio, Servicios y Contacto.
Configura rutas /, /servicios y /contacto.
Crea una barra de navegación con  para cambiar entre ellos.
Bonus: agrega estilos para destacar la página actual.

---

## 📘 Módulo 14: Consumo de APIs con fetch o Axios

### ¿Qué es una API?

Una API (Application Programming Interface) permite que nuestra app React se comunique con servidores externos y obtenga o envíe datos, como usuarios, productos, publicaciones, etc.
En React, solemos usar fetch() o librerías como axios para hacer peticiones HTTP (GET, POST, PUT, DELETE...).

**📦 Opciones populares**

fetch(): viene con JavaScript por defecto.
axios: librería externa más amigable (instalar con npm install axios).

**💡 ¿Dónde usamos la petición?**

Usamos el hook useEffect() para hacer la petición una vez que el componente se monte.

#### Ejemplo con fetch() – Obtener usuarios

import { useState, useEffect } from "react";

```jsx
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

#### Ejercicio para ti:

Crea un componente ListaPosts.
Usa fetch para obtener datos de https://jsonplaceholder.typicode.com/posts.
Muestra los títulos (title) en pantalla.
Agrega un mensaje de "Cargando..." mientras se obtienen los datos.

---

## 📘 Módulo 15: Custom Hooks

### ¿Qué es un Custom Hook?

Un Custom Hook es una función de JavaScript que empieza con use y puede usar otros hooks internos (useState, useEffect, etc.). Nos permite extraer lógica reutilizable y compartirla entre varios componentes.
Si encuentras que estás copiando y pegando useEffect, useState, etc. en varios componentes, ¡es hora de crear un hook personalizado!


#### ¿Cómo se crea?

Un Custom Hook:
Es una función que empieza con use.
Usa hooks dentro (como useState, useEffect).
Devuelve valores o funciones que quieras reutilizar.


#### Ejemplo: Hook para obtener datos de una API

import { useState, useEffect } from "react";

```jsx
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


**📦 Usando el Custom Hook**

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


#### Ejercicio para ti:

Crea un hook llamado useContador que:
Reciba un valor inicial
Devuelva el valor y una función para incrementarlo
Úsalo dentro de un componente llamado ContadorPersonalizado.

---

## 📘 Módulo 16: Context API – Manejo global del estado


### ¿Qué es Context API?

Context API es una herramienta nativa de React que permite crear un estado global al que cualquier componente de tu aplicación puede acceder o modificar, sin importar dónde esté ubicado en el árbol de componentes.
Es ideal para manejar temas globales como: autenticación, idioma, tema oscuro/claro, carrito de compras, usuario actual, etc.


#### ¿Cómo funciona?

Crear el contexto
Proveer el contexto
Consumir el contexto


#### Ejemplo paso a paso: Tema (oscuro/claro)

1. Crear el contexto
import { createContext } from "react";

export const TemaContexto = createContext();
2. Crear el proveedor
import { useState } from "react";
import { TemaContexto } from "./TemaContexto";

export function TemaProvider({ children }) {
 const [tema, setTema] = useState("claro");

 const alternarTema = () => {
 setTema((prev) => (prev === "claro" ? "oscuro" : "claro"));
 };

 return (

 {children}

 );
}
3. Usar el contexto desde un componente
import { useContext } from "react";
import { TemaContexto } from "./TemaContexto";

```jsx
function BotonTema() {
 const { tema, alternarTema } = useContext(TemaContexto);

 return (

 Cambiar a modo {tema === "claro" ? "oscuro" : "claro"}

 );
}
```
4. Envolver la app con el Provider
import { TemaProvider } from "./TemaProvider";

```jsx
function App() {
 return (


 {/* otros componentes */}

 );
}
```


#### Ejercicio para ti:

Crea un contexto llamado UsuarioContexto.
En el proveedor, define un nombre de usuario ("Juan").
Crea un componente PerfilUsuario que muestre: “Bienvenido, Juan”.
Usa useContext para obtener el nombre desde el contexto.

---

## 📘 Módulo 17: Introducción a Redux (opcional)


### ¿Qué es Redux?

Redux es una librería de manejo de estado global. Es más poderosa y estructurada que Context API, ideal cuando:
La aplicación es grande y compleja.
Muchos componentes comparten y modifican el mismo estado.
Necesitas depuración, trazabilidad y control total del flujo de datos.
Se basa en un único estado global inmutable, y para modificarlo usamos acciones y reducers.


**🔁 Principios clave de Redux**

Store: el estado global centralizado.
Actions: objetos que describen qué ocurrió.
Reducers: funciones que actualizan el estado según la acción.
Dispatch: método para lanzar acciones.
useSelector: permite acceder al estado.
useDispatch: permite lanzar acciones.


**🚀 Instalación (con React)**

npm install @reduxjs/toolkit react-redux


#### Ejemplo con Redux Toolkit (recomendado)

1. Crear el slice
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

2. Configurar el store
// store.js
import { configureStore } from '@reduxjs/toolkit';
import contadorReducer from './contadorSlice';

export const store = configureStore({
 reducer: {
 contador: contadorReducer
 }
});

3. Proveer el store a tu app
// index.js
import { Provider } from 'react-redux';
import { store } from './store';
import App from './App';





4. Usar Redux en un componente
import { useSelector, useDispatch } from 'react-redux';
import { incrementar, reiniciar } from './contadorSlice';

```jsx
function ContadorRedux() {
 const contador = useSelector((state) => state.contador);
 const dispatch = useDispatch();

 return (

Contador Redux: {contador}
 dispatch(incrementar())}>Incrementar
 dispatch(reiniciar())}>Reiniciar

 );
}
```


#### Ejercicio para ti:

Crea un contador con Redux Toolkit.
Agrega botones para +1, -1, y reiniciar.
Usa useSelector y useDispatch para manejarlo.

---

## 📘 Módulo 18: Deploy de la aplicación React


### ¿Qué es el Deploy?

Hacer deploy significa subir tu app a internet. Es decir, transformarla desde tu entorno local en una página web accesible desde cualquier lugar.

🌐 Opciones para publicar una app React
Vercel (recomendado)
Netlify
GitHub Pages
Render, Firebase Hosting, AWS, etc.
Nosotros usaremos Vercel porque es fácil, rápido y gratuito.


**🚀 Paso a paso: Deploy con Vercel**

1. Subir tu app a GitHub
Si aún no tienes cuenta en GitHub, créala.
Crea un repositorio nuevo.
Sube tu proyecto (git init, git add ., git commit, git push).
2. Crear cuenta en 
Inicia sesión con tu cuenta de GitHub.
Haz clic en "Add New Project".
Selecciona el repositorio con tu app React.
Vercel detectará que es React y hará la configuración automáticamente.
Haz clic en "Deploy".

### ¡Listo! En unos segundos tendrás un link público como:

https://mi-app-react.vercel.app


**⚙️ Bonus: ¿y si usas create-react-app?**

Cuando usas npm run build, se genera una carpeta build/ con los archivos listos para producción.
npm run build
Puedes subir esos archivos a cualquier servidor o usar herramientas como:
GitHub Pages (requiere configuración)
Netlify Drop (solo arrastras la carpeta build)


#### Ejercicio para ti:

Sube tu proyecto a GitHub.
Haz deploy con Vercel.
Comparte el link de tu app con tus amigos o clientes.
