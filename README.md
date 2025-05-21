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


