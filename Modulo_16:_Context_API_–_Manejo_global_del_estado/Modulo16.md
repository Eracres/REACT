# 📘 Módulo 16: Context API – Manejo global del estado

## ❓ ¿Qué es Context API?

Context API es una herramienta integrada en React que permite **compartir datos entre componentes sin necesidad de pasar props manualmente a través de múltiples niveles del árbol de componentes**.

Es útil para manejar:
- El tema visual (oscuro o claro)
- Usuario autenticado
- Idioma global
- Configuraciones de la app
- Carrito de compras, etc.

---

## 🔧 ¿Por qué usar Context?

- Evita el "prop drilling" (pasar props manualmente de padre a hijo hasta llegar al destino).
- Mejora la organización de estados compartidos.
- Facilita el mantenimiento en aplicaciones medianas a grandes.

---

## ⚙️ ¿Cómo funciona Context?

1. **Crear el contexto** → define qué información se compartirá.
2. **Proveer el contexto** → usa un `Provider` para que sus hijos accedan al valor.
3. **Consumir el contexto** → usa `useContext` para acceder a los datos dentro de cualquier componente hijo.

---

## 🧠 Buenas prácticas

| Recomendación                        | Explicación                                                |
|-------------------------------------|------------------------------------------------------------|
| Crea un archivo por contexto        | Para mantener la estructura clara y modular                |
| Encapsula lógica en un `Provider`   | Así gestionas el estado dentro del contexto               |
| Usa `useContext` en componentes     | Para consumir los valores fácilmente                      |
| No uses Context como reemplazo de Redux | Solo cuando necesitas compartir estados sencillos       |

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

## [⬅️](../Modulo_15:_Custom_Hooks/Modulo_15.md) Módulo 15 ... Módulo 17 [➡️](../Modulo_17:_Introducción_a_Redux/Modulo17.md)

## [🏠 Inicio](../README.md)
