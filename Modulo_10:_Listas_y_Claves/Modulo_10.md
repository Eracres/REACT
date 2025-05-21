# 📘 Módulo 10: Listas y Claves

## ❓ ¿Qué son las listas en React?

Las listas en React son una manera de **renderizar múltiples elementos de forma dinámica**. Se usan típicamente cuando quieres mostrar una colección de datos: usuarios, productos, mensajes, etc.

React se apoya en **JavaScript y su método `.map()`** para recorrer arrays y devolver elementos JSX. Esta es una de las herramientas más poderosas para generar contenido desde estructuras de datos.

---

## ❓ ¿Qué son las keys en React?

Cuando renderizas listas, React necesita identificar de forma única cada elemento para **detectar los cambios** entre renders y mejorar el rendimiento.

Por eso es obligatorio usar una **`key` única por elemento** en listas dinámicas. Esto le permite a React saber cuál elemento fue modificado, agregado o eliminado.

### ✅ ¿Por qué son importantes?

- Evitan renderizados innecesarios.
- Mejoran el rendimiento.
- Evitan errores inesperados en la interfaz.

---

## ⚠️ Buenas prácticas con keys

| Situación                 | ¿Usar index como key? |
|--------------------------|------------------------|
| Lista estática           | ✅ Aceptable           |
| Lista que puede cambiar  | ❌ Mejor usar id único |
| Orden puede cambiar      | ❌ Index puede fallar  |

---

## 🧠 ¿Cómo se usan las listas?

A través del método `.map()` de JavaScript. Este método permite transformar un array de elementos en un array de nodos JSX:

```jsx
{miArray.map(item => (
  <li key={item.id}>{item.nombre}</li>
))}
```

---

## 🛠️ Tips adicionales

- Siempre que trabajes con arrays, recuerda el uso del `key`.
- Puedes usar cualquier tipo de estructura (objetos, strings, números).
- Puedes dividir los elementos en componentes individuales si la lógica crece.

---

## 📌 Casos de uso comunes

- Mostrar listas de comentarios, productos, usuarios, mensajes, tareas...
- Generar menús dinámicos.
- Crear componentes que se repiten pero con datos distintos.

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

## [⬅️](../Modulo_9:_Estilos_en_React/Modulo_9.md) Módulo 9 ... Módulo 11 [➡️](../Modulo_11:_Formularios_en_React/Modulo_11.md)

## [🏠 Inicio](../README.md)
