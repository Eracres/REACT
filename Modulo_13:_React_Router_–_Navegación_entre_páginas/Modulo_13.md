# 📘 Módulo 13: React Router – Navegación entre páginas

## ❓ ¿Qué es React Router?

React Router es una librería oficial que permite agregar navegación entre diferentes "páginas" dentro de una Single Page Application (SPA) creada con React.

Aunque en una SPA no se recargue la página, **React Router simula múltiples vistas** actualizando la URL y renderizando los componentes correspondientes.

---

## 📦 ¿Qué podemos hacer con React Router?

- Crear rutas como `/inicio`, `/perfil`, `/producto/:id`
- Crear rutas anidadas o dinámicas
- Cambiar de vista sin recargar la página
- Añadir navegación con enlaces (`<Link>`)
- Controlar redirecciones, rutas protegidas y navegación desde código

---

## 🚀 Instalación

Desde la terminal, ejecuta dentro del proyecto React:

```bash
npm install react-router-dom
```

---

## 🔁 Conceptos clave

| Componente / Hook      | Función                                                  |
|------------------------|----------------------------------------------------------|
| `<BrowserRouter>`      | Envoltorio general de la app para activar React Router   |
| `<Routes>`             | Contenedor de rutas definidas con `<Route>`             |
| `<Route>`              | Define una ruta específica (`path` y `element`)         |
| `<Link>`               | Enlace que cambia la vista sin recargar                 |
| `useNavigate()`        | Hook para navegar desde código                          |

---

## 💡 Estructura típica en `App.js`

```jsx
import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom";
```

```jsx
function App() {
  return (
    <Router>
      <nav>
        <Link to="/">Inicio</Link>
        <Link to="/acerca">Acerca</Link>
      </nav>
      <Routes>
        <Route path="/" element={<Inicio />} />
        <Route path="/acerca" element={<Acerca />} />
      </Routes>
    </Router>
  );
}
```

---

## 🧭 Buenas prácticas

- Usa `<Link>` o `useNavigate()` en lugar de `<a href="">`.
- Mantén la estructura de rutas clara y modular.
- Para rutas protegidas, considera el uso de roles o estados autenticados.

---

## 🧪 Ejemplos básicos:

* [📝Ejemplo 1](./Ejemplos/Ejemplo_1.md)
* [📝Ejemplo 2](./Ejemplos/Ejemplo_2.md)
* [📝Ejemplo 3](./Ejemplos/Ejemplo_3.md)
* [📝Ejemplo 4](./Ejemplos/Ejemplo_4.md)
* [📝Ejemplo 5](./Ejemplos/Ejemplo_5.md)
* [📝Ejemplo 6](./Ejemplos/Ejemplo_6.md)

## 🎯 Ejercicios para ti:

* [📋Ejercicio 1](./Ejercicios/Ejercicio_1.md)
* [📋Ejercicio 2](./Ejercicios/Ejercicio_2.md)
* [📋Ejercicio 3](./Ejercicios/Ejercicio_3.md)
* [📋Ejercicio 4](./Ejercicios/Ejercicio_4.md)

---

## [⬅️](../Modulo_12:_Lifting_State_Up_y_comunicación_entre_componentes/Modulo_12.md) Módulo 12 ... Módulo 14 [➡️](../Modulo_14:_Consumo_de_APIs_con_fetch_o_Axios/Modulo_14.md)

## [🏠 Inicio](../README.md)
