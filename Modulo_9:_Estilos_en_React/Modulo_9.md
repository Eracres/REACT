# 📘 Módulo 9: Estilos en React

## ❓ ¿Cómo se aplican estilos en React?

En React, existen múltiples maneras de aplicar estilos a los componentes. Esta flexibilidad permite adaptar la forma de trabajar según el tamaño del proyecto, el equipo, y las preferencias personales.

---

## 🎨 Métodos comunes para aplicar estilos

### 1. CSS tradicional

Consiste en usar archivos `.css` externos que se importan en los componentes. Es ideal para quienes vienen de un entorno HTML/CSS clásico.

```css
/* estilos.css */
.titulo {
  color: royalblue;
  font-size: 2rem;
}
```

```jsx
import "./estilos.css";

function Encabezado() {
  return <h1 className="titulo">¡Hola desde CSS tradicional!</h1>;
}
```

✔️ Ventajas:
- Reutilizable
- Familiar
- Se puede usar con preprocessors (SASS, LESS)

---

### 2. Estilos en línea (inline styles)

Los estilos se aplican directamente a los elementos como objetos JavaScript.

```jsx
const estilo = {
  backgroundColor: "tomato",
  color: "white",
  padding: "10px"
};
```

```jsx
<button style={estilo}>Haz clic</button>
```

✔️ Ventajas:
- Dinámico (puede cambiar según estado o props)
- Ideal para pruebas rápidas

⚠️ Consideraciones:
- Menor legibilidad para estilos grandes
- Sintaxis en camelCase

---

### 3. CSS Modules

Permiten usar clases con nombres únicos, evitando conflictos entre estilos de diferentes componentes.

```css
/* Titulo.module.css */
.tituloEspecial {
  color: green;
  text-transform: uppercase;
}
```

```jsx
import styles from './Titulo.module.css';

function Titulo() {
  return <h2 className={styles.tituloEspecial}>Hola desde CSS Module</h2>;
}
```

✔️ Ventajas:
- Encapsulación
- Evita colisiones de clases

---

### 4. Frameworks y librerías externas

React es compatible con herramientas como:

- Bootstrap
- Tailwind CSS
- Material UI
- Styled Components

Ejemplo con Tailwind:

```jsx
<h2 className="text-2xl font-bold text-blue-500">Título Tailwind</h2>
```

---

## 💡 ¿Cuál deberías elegir?

| Método         | Ideal para                  |
|----------------|-----------------------------|
| CSS tradicional| Proyectos pequeños/medianos |
| Inline Styles  | Cambios dinámicos puntuales |
| CSS Modules    | Proyectos medianos/grandes  |
| Frameworks     | Equipos grandes, UI estandarizada |

---

## 🧠 Buenas prácticas

- Usa nombres semánticos y coherentes para clases.
- Evita mezclar muchos métodos de estilos en un solo proyecto.
- Si usas CSS Modules o librerías externas, no es necesario tener estilos globales.
- Centraliza los colores y fuentes para mantener consistencia.

---
