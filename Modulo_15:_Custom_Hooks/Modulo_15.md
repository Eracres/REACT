# 📘 Módulo 15: Custom Hooks

## ❓ ¿Qué es un Custom Hook?

Un Custom Hook es una función personalizada de JavaScript que **empieza con `use`** y puede utilizar otros hooks como `useState`, `useEffect`, `useContext`, entre otros. Sirven para **extraer lógica reutilizable** de tus componentes y mantener tu código limpio y modular.

---

## 🔁 ¿Por qué usar Custom Hooks?

- Evitas duplicar lógica entre componentes.
- Separas lógica de presentación.
- Haces tus componentes más legibles y fáciles de testear.
- Puedes compartir lógica compleja entre distintos componentes.

---

## 🧠 ¿Cómo se crea un Custom Hook?

Un custom hook:
1. Es una función que **empieza con `use`**.
2. Usa hooks internos (`useState`, `useEffect`, etc.).
3. **Devuelve** datos, funciones o estados útiles para el componente que lo use.

---

## 💡 Convenciones

| Regla                         | Detalles                                                   |
|------------------------------|------------------------------------------------------------|
| Debe empezar por `use`       | Para que React detecte que es un hook válido              |
| Puede recibir parámetros     | Como `url`, `valorInicial`, etc.                          |
| Devuelve un objeto o valores | Para acceder a los resultados de forma sencilla           |

---

## 📌 Ejemplos comunes

- `useContador`: contador personalizado con incremento/decremento
- `useDarkMode`: alternar tema oscuro/claro y guardar en localStorage
- `useFetch`: lógica para obtener datos de una API
- `useForm`: manejo de formularios y validaciones

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

## [⬅️](../Modulo_14:_Consumo_de_APIs_con_fetch_o_Axios/Modulo_14.md) Módulo 14 ... Módulo 16 [➡️](../Modulo_16:_Context_API_–_Manejo_global_del_estado/Modulo16.md)

## [🏠 Inicio](../README.md)
