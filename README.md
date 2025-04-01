# Curso Completo de React – Desarrollo de Aplicaciones Web con React

## 🧑‍🏫 Resumen del Curso

Este curso completo de React ha cubierto todos los fundamentos necesarios para desarrollar aplicaciones web modernas usando React. Desde los conceptos básicos hasta la integración con APIs, gestión de estado global y despliegue profesional. Cada módulo incluye teoría, ejemplos reales y ejercicios prácticos.

---

## 🗂️ Temario General del Curso

1. Introducción a React  
2. Configuración del entorno de desarrollo  
3. JSX  
4. Componentes (Funcionales y de Clase)  
5. Props  
6. Estado con useState  
7. Eventos  
8. useEffect  
9. Estilos en React  
10. Listas y claves  
11. Formularios  
12. Lifting State Up  
13. React Router  
14. Consumo de APIs  
15. Custom Hooks  
16. Context API  
17. Introducción a Redux (opcional)  
18. Deploy de la aplicación React  

---

## 📘 Contenido por Módulo


---

## 📘 Módulo 1: Introducción a React

### ✅ ¿Qué es React?

React es una biblioteca de JavaScript creada por Facebook para construir interfaces de usuario. Su objetivo principal es crear aplicaciones web reactivas, eficientes y modulares.

**Ventajas clave:**
- Componentes reutilizables
- Virtual DOM (mejora el rendimiento)
- Flujo de datos unidireccional (unidirectional data flow)
- Ideal para SPAs (Single Page Applications)

---

### 💻 Ejemplo mío (muy simple)

```jsx
function HolaMundo() {
  return <h1>¡Hola, mundo desde React!</h1>;
}
```

Este sería un componente muy básico en React.

---

### 🧠 Ejercicio para ti:

Crea un componente llamado `Saludo` que muestre el mensaje:
```
¡Bienvenido al curso de React!
```


---

## 📘 Módulo 2: Configuración del entorno de desarrollo

### ✅ ¿Cómo empezar con React?

Para comenzar a trabajar con React de forma sencilla y rápida, usaremos la herramienta oficial Create React App.

### 🛠️ Pasos:
1. Instala Node.js y npm.
2. En la terminal:  
```bash
npx create-react-app mi-app
cd mi-app
npm start
```

### 🧠 Ejercicio:
Crea tu proyecto y reemplaza `App.js` con el componente `HolaMundo`.

---

## 📘 Módulo 3: JSX

JSX es una extensión de JavaScript que permite escribir HTML dentro del código JS.

### 💻 Ejemplo:
```jsx
function ComponenteJSX() {
  const mensaje = "Soy JSX";
  return <h1>{mensaje}</h1>;
}
```

---

## 📘 Módulo 4: Componentes (Funcionales y de Clase)

### 💻 Funcional:
```jsx
function Tarjeta() {
  return <p>Componente funcional</p>;
}
```

### 💻 De Clase:
```jsx
class TarjetaClase extends React.Component {
  render() {
    return <p>Componente de clase</p>;
  }
}
```

---

## 📘 Módulo 5: Props

Permiten pasar información entre componentes.

### 💻 Ejemplo:
```jsx
function Bienvenida(props) {
  return <h3>Hola, {props.nombre}</h3>;
}
```

---

## 📘 Módulo 6: Estado con useState

Permite manejar valores dinámicos.

### 💻 Ejemplo:
```jsx
const [contador, setContador] = useState(0);
```

---

## 📘 Módulo 7: Eventos

Manejan interacciones del usuario.

### 💻 Ejemplo:
```jsx
<button onClick={() => alert('¡Clic!')}>Haz clic</button>
```

---

## 📘 Módulo 8: useEffect – Ciclo de vida

Ejecuta efectos secundarios como peticiones a APIs.

### 💻 Ejemplo:
```jsx
useEffect(() => {
  console.log("Componente montado");
}, []);
```

---

## 📘 Módulo 9: Estilos en React

### 💻 Inline:
```jsx
<p style={{ color: "red" }}>Hola</p>
```

### 💻 CSS Modules:
```jsx
import styles from './archivo.module.css'
```

---

## 📘 Módulo 10: Listas y claves

### 💻 Ejemplo:
```jsx
const frutas = ["Manzana", "Banana"];
frutas.map((fruta, i) => <li key={i}>{fruta}</li>);
```

---

## 📘 Módulo 11: Formularios

### 💻 Ejemplo:
```jsx
const [nombre, setNombre] = useState("");
<input value={nombre} onChange={(e) => setNombre(e.target.value)} />
```

---

## 📘 Módulo 12: Lifting State Up

### 💻 Ejemplo:
```jsx
// Se eleva el estado al padre para compartirlo entre hijos
```

---

## 📘 Módulo 13: React Router

Permite navegación entre vistas.

### 💻 Ejemplo:
```jsx
<Route path="/inicio" element={<Inicio />} />
<Link to="/inicio">Ir a Inicio</Link>
```

---

## 📘 Módulo 14: Consumo de APIs

### 💻 Ejemplo con fetch:
```jsx
useEffect(() => {
  fetch("url").then(res => res.json()).then(data => setDatos(data));
}, []);
```

---

## 📘 Módulo 15: Custom Hooks

Extraen lógica reutilizable.

### 💻 Ejemplo:
```jsx
function useContador(inicial) {
  const [valor, setValor] = useState(inicial);
  return [valor, () => setValor(valor + 1)];
}
```

---

## 📘 Módulo 16: Context API

Manejo global del estado sin props.

### 💻 Ejemplo:
```jsx
const UsuarioContexto = createContext();
const usuario = useContext(UsuarioContexto);
```

---

## 📘 Módulo 17: Redux

Gestión avanzada del estado.

### 💻 Ejemplo básico:
```jsx
dispatch(incrementar());
const contador = useSelector(state => state.contador);
```

---

## 📘 Módulo 18: Deploy

Sube tu app a Vercel:

### 🛠️ Pasos:
1. Sube tu proyecto a GitHub
2. Ve a vercel.com
3. Importa el repositorio
4. ¡Deploy automático!
