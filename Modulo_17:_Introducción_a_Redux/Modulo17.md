# 📘 Módulo 17: Introducción a Redux (opcional)

## ❓ ¿Qué es Redux?

Redux es una librería para el manejo de **estado global** en aplicaciones JavaScript, especialmente útil con React. Es una solución más estructurada y poderosa que Context API, recomendada cuando:

- La aplicación es grande o compleja.
- Se necesita compartir estado entre muchos componentes.
- Se quiere trazabilidad y control total del flujo de datos.

---

## 🔁 Principios fundamentales de Redux

| Concepto     | Descripción                                                                 |
|--------------|-----------------------------------------------------------------------------|
| **Store**    | El estado global centralizado de toda la app.                              |
| **Actions**  | Objetos que describen qué ocurrió (tipo y payload).                        |
| **Reducers** | Funciones que actualizan el estado en base a las acciones.                 |
| **Dispatch** | Método para enviar acciones al reducer.                                    |
| **Selector** | Función para obtener datos del estado global.                              |

---

## 🧠 Redux Toolkit

Redux Toolkit es la herramienta oficial para simplificar Redux:
- Menos código repetitivo
- API moderna y optimizada
- Incluye `createSlice`, `configureStore` y middlewares

Instalación:

```bash
npm install @reduxjs/toolkit react-redux
```

---

## 💡 ¿Cuándo usar Redux?

| Situación                                                  | ¿Usar Redux? |
|------------------------------------------------------------|--------------|
| Una app pequeña con pocos componentes                      | ❌ No        |
| Necesitas manejar estado compartido entre muchos niveles   | ✅ Sí        |
| Necesitas control avanzado (logs, undo, debugging profundo)| ✅ Sí        |
| Uso de APIs, listas de productos, autenticación, etc.      | ✅ Sí        |

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

## [⬅️](../Modulo_16:_Context_API_–_Manejo_global_del_estado/Modulo16.md) Módulo 16 ... Módulo 18 [➡️](../Modulo_18:_Deploy_de_la_aplicación_React/Modulo_18.md)

## [🏠 Inicio](../README.md)
