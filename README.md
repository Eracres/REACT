# 🧑‍🏫 Curso de React – Desarrollo de Aplicaciones Web con React

## 🗂️ Temario General del Curso



1. [Introducción a React ](./Módulo_1:_Introducción_a_React/Modulo_1.md)
2. [Configuración del entorno de desarrollo ](./Modulo_2:_Configuración_del_entorno_de_desarrollo/Modulo_2.md) 
3. [JSX: Sintaxis especial de React](./Modulo_3:_JSX_Sintaxis_especial_de_React/Modulo_3.md)  
4. [Componentes (Funcionales y de Clase)](./Modulo_4:_Componentes_(Funcionales_y_de_Clase)/Modulo_4.md)
5. [Props (Propiedades entre componentes)](./Modulo_5:_Props_(Propiedades_entre_componentes)/Modulo_5.md)
6. [Estado (useState)](./Modulo_6:_Estado_con_useState/Modulo_6.md)
7. [Eventos en React](./Modulo_7:_Eventos_en_React/Modulo_7.md)
8. [Ciclo de vida y useEffect](./Modulo_8:_useEffect_–_Ciclo_de_vida_y_efectos_secundarios/Modulo_8.md) 
9. [Estilos en React](./Modulo_9:_Estilos_en_React/Modulo_9.md)
10. [Listas y claves](./Modulo_10:_Listas_y_Claves/Modulo_10.md)
11. [Formularios en React](./Modulo_11:_Formularios_en_React/Modulo_11.md)
12. [Lifting State Up y comunicación entre componentes](./Modulo_12:_Lifting_State_Up_y_comunicación_entre_componentes/Modulo_12.md)
13. [React Router (Navegación entre páginas)](./Modulo_13:_React_Router_–_Navegación_entre_páginas/Modulo_13.md)
14. [Consumo de APIs con fetch o Axios](./Modulo_14:_Consumo_de_APIs_con_fetch_o_Axios/Modulo_14.md)
15. [Custom Hooks](./Modulo_15:_Custom_Hooks/Modulo_15.md)
16. [Context API (Manejo global del estado)](./Modulo_16:_Context_API_–_Manejo_global_del_estado/Modulo16.md)
17. [Introducción a Redux (opcional, si quieres profundizar)](./Modulo_17:_Introducción_a_Redux/Modulo17.md)
18. [Deploy de la aplicación React](./Modulo_18:_Deploy_de_la_aplicación_React/Modulo_18.md)

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


