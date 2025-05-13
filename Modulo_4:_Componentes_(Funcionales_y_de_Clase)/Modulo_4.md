
# 📘 Módulo 4: Componentes (Funcionales y de Clase)

## ❓ ¿Qué es un componente en React?

Un **componente** es una unidad funcional y visual que representa una **parte de la interfaz de usuario**.  
Todo en React gira en torno a los componentes. Puedes pensarlos como **bloques de LEGO** que se ensamblan para construir toda tu aplicación.

### 📦 ¿Qué hace un componente?

- Encapsula su propia lógica y vista
- Se puede reutilizar en diferentes partes del proyecto
- Puede recibir datos con **props**
- Puede gestionar su propio **estado interno**

---

## 🧱 Tipos de componentes en React

### 1. ✅ Componentes funcionales (actual estándar)

Los componentes funcionales son **funciones JavaScript** que retornan JSX.

```jsx
function Tarjeta() {
  return <p>Componente funcional</p>;
}
```

Son más simples, eficientes y compatibles con **Hooks** (`useState`, `useEffect`, etc.).

---

### 2. 🕰️ Componentes de clase (en desuso pero útiles de conocer)

```jsx
import React, { Component } from 'react';

class TarjetaClase extends Component {
  render() {
    return <p>Componente de clase</p>;
  }
}
```

Usan `render()` para retornar JSX y métodos de ciclo de vida como `componentDidMount`. Se ven cada vez menos, pero aparecen en proyectos antiguos.

---

### 👑 ¿Cuál deberías usar hoy?

✅ **Componentes funcionales + Hooks**  
Son el estándar moderno por su simplicidad, compatibilidad y rendimiento.

---

## 📢 Convenciones clave

- ✅ El nombre del componente debe empezar en mayúscula (`Tarjeta`, no `tarjeta`)
- 📁 Recomendable: un archivo por componente (`PerfilUsuario.js`)
- ⚠️ Un componente debe devolver un único elemento raíz (`<div>` o `<>` fragmentos)

---

## 🧠 Composición de componentes

```jsx
function PerfilCompleto() {
  return (
    <div>
      <FotoPerfil />
      <PerfilUsuario />
    </div>
  );
}
```

Permite reutilizar código y dividir lógica visual.

---

## 🧬 Ciclo de vida de componentes de clase

| Método                  | Cuándo se ejecuta                             |
|------------------------|-----------------------------------------------|
| `constructor()`        | Al instanciar el componente                   |
| `componentDidMount()`  | Tras renderizar por primera vez               |
| `componentDidUpdate()` | Tras actualizar props o estado                |
| `componentWillUnmount()`| Antes de eliminar el componente del DOM      |

🆚 Equivalentes modernos con `useEffect` en componentes funcionales.

---

## 🔄 ¿Cuándo se vuelve a renderizar?

Cuando:

- Cambian las `props`
- Cambia el `estado` (`useState`, `setState`)
- Su componente padre se vuelve a renderizar

---

## 🧠 Composición vs Herencia

React recomienda la **composición** sobre la herencia.

```jsx
function Layout({ children }) {
  return <div className="container">{children}</div>;
}
```

Uso:

```jsx
<Layout>
  <PerfilUsuario />
</Layout>
```

---

## ⚙️ Reglas importantes con Hooks

1. El nombre del componente debe comenzar con mayúscula
2. No usar Hooks dentro de condicionales o bucles
3. Siempre devolver un único nodo raíz

---

## ✅ Buenas prácticas

- Componentes pequeños y reutilizables
- Separación en carpetas individuales
- Props bien definidas
- Evitar duplicación de lógica (usa Hooks)
- Documenta bien tu componente

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

## [⬅️](../Modulo_3:_JSX_Sintaxis_especial_de_React/Modulo_3.md) Módulo 3 ... Módulo 5 [➡️](../Modulo_5:_Props_(Propiedades_entre_componentes)/Modulo_5.md)

## [🏠 Inicio](../README.md)
