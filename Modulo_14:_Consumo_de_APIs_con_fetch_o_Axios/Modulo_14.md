# 📘 Módulo 14: Consumo de APIs con fetch o Axios

## ❓ ¿Qué es una API?

Una API (Application Programming Interface) permite que una aplicación React obtenga o envíe datos a un servidor externo. Es fundamental para trabajar con bases de datos, servicios de terceros y backends propios.

React no trae herramientas específicas para trabajar con APIs, pero puedes usar JavaScript puro (`fetch`) o librerías especializadas como `axios`.

---

## 📦 Opciones populares

| Método      | Características                            |
|-------------|---------------------------------------------|
| `fetch()`   | Nativo de JavaScript, no requiere instalación |
| `axios`     | Sintaxis más limpia, soporta cancelación, interceptores, etc. |

Para instalar axios:

```bash
npm install axios
```

---

## 💡 ¿Dónde hacer la llamada a la API?

La mejor práctica es hacer peticiones HTTP dentro del hook `useEffect`, para que se realicen una vez que el componente se monte.

```jsx
useEffect(() => {
  // llamada a la API aquí
}, []);
```

---

## 🔄 Métodos HTTP más comunes

| Método | Acción        | Uso                              |
|--------|---------------|-----------------------------------|
| GET    | Obtener datos | Listar usuarios, productos, etc. |
| POST   | Enviar datos  | Crear un nuevo recurso           |
| PUT    | Reemplazar    | Actualizar un recurso completo   |
| PATCH  | Modificar     | Actualizar parcialmente          |
| DELETE | Eliminar      | Borrar un recurso                |

---

## 🧠 Buenas prácticas

- Maneja estados como `loading`, `error`, y `data`.
- Usa `try/catch` con `async/await` para mayor claridad.
- Encapsula llamadas en funciones reutilizables o hooks personalizados (`custom hooks`).

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

## [⬅️](../Modulo_13:_React_Router_–_Navegación_entre_páginas/Modulo_13.md) Módulo 13 ... Módulo 15 [➡️](../Modulo_15:_Custom_Hooks/Modulo_15.md)

## [🏠 Inicio](../README.md)
