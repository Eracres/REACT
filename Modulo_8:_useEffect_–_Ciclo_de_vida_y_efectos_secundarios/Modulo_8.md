
# 📘 Módulo 8: useEffect – Ciclo de vida y efectos secundarios

## ❓ ¿Qué es useEffect?

`useEffect` es un **hook de React** que nos permite ejecutar código que tiene efectos secundarios, como llamadas a APIs, temporizadores, acceso al DOM, suscripciones, y más.

En los componentes de clase, el ciclo de vida era manejado con métodos como `componentDidMount`, `componentDidUpdate` y `componentWillUnmount`. En los componentes funcionales, todo eso se logra con `useEffect`.

---

## 🔁 ¿Cuándo se ejecuta useEffect?

`useEffect` se ejecuta **después del renderizado del componente**. Su comportamiento cambia dependiendo del segundo parámetro que recibe:

### 📦 Sintaxis general

```jsx
useEffect(() => {
  // Código del efecto
}, [dependencias]);
```

### 🧠 Casos comunes

| Array de dependencias     | ¿Cuándo se ejecuta el efecto?                      |
|---------------------------|----------------------------------------------------|
| `[]` (vacío)              | Solo una vez al montar el componente               |
| `[estado]`                | Cada vez que `estado` cambie                       |
| (sin segundo parámetro)   | Después de **cada** renderizado                   |

---

## 🧹 Limpieza del efecto

Algunos efectos (como temporizadores o suscripciones) deben ser limpiados cuando el componente se desmonte para evitar fugas de memoria.

Esto se hace retornando una función dentro del `useEffect`:

```jsx
useEffect(() => {
  const timer = setInterval(() => {
    // algo
  }, 1000);

  return () => clearInterval(timer);
}, []);
```

---

## 📌 ¿Para qué se utiliza useEffect?

- Llamar a una API cuando se monta el componente
- Configurar o limpiar un temporizador
- Agregar y quitar event listeners
- Leer del `localStorage` al iniciar
- Realizar animaciones o efectos visuales al cargar

---

## ⚠️ Buenas prácticas

- Siempre limpia efectos que pueden dejar procesos abiertos (`setInterval`, `setTimeout`, suscripciones...).
- Si el efecto depende de valores, decláralos en el array de dependencias.
- Evita side-effects dentro del return del componente.
- Divide los efectos en múltiples `useEffect` si hacen tareas distintas.

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

## [⬅️](../Modulo_7:_Eventos_en_React/Modulo_7.md) Módulo 7 ... Módulo 9 [➡️](../Modulo_9:_Estilos_en_React/Modulo_9.md)

## [🏠 Inicio](../README.md)
