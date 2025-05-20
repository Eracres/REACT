# 📘 Módulo 6: Estado con useState

## ❓ ¿Qué es el estado en React?

El **estado** es como la "memoria interna" de un componente. Permite que React guarde y actualice información dinámica con el tiempo, como:

- Contadores
- Entradas del usuario (formularios)
- Botones activos/inactivos
- Datos cargados desde una API

Cuando el estado cambia, React vuelve a renderizar el componente automáticamente con el nuevo valor. Esto permite construir interfaces reactivas e interactivas.

## ❓ ¿Qué es un hook?

Un **hook** es una función especial introducida en React 16.8 que te permite “engancharte” a las características de React (como estado, efectos, contexto, etc.) **sin usar componentes de clase**.

`useState()` es el hook más básico y el punto de entrada para añadir estado a componentes funcionales.

## 📦 Sintaxis de useState

```jsx
const [estado, setEstado] = useState(valorInicial);
```

- `estado`: variable que contiene el valor actual.
- `setEstado`: función que se usa para actualizar ese valor.
- `useState(valorInicial)`: inicializa el estado con un valor inicial (puede ser un número, string, booleano, array, objeto...).

## 📘 ¿Cómo funciona en la práctica?

Cada vez que llamas a `setEstado`, React:

1. Actualiza el valor de `estado`.
2. Vuelve a renderizar el componente automáticamente.
3. Muestra el nuevo valor en la interfaz.

Esto permite que tus componentes respondan en tiempo real a las acciones del usuario.

## 💡 Buenas prácticas con useState

- No modifiques directamente el estado (ej: `estado = nuevoValor` está prohibido).
- Usa siempre `setEstado` para hacer cambios.
- Puedes usar múltiples `useState` dentro de un componente si necesitas almacenar varios valores.
- Si el nuevo valor depende del anterior, usa una función:  
  ```jsx
  setContador((prev) => prev + 1);
  ```

## 🧠 ¿Cuándo usar useState?

- Cuando necesitas guardar un valor que cambia con el tiempo.
- Cuando ese valor afecta la visualización del componente.
- Ejemplos comunes:
  - Mostrar u ocultar elementos
  - Contadores
  - Validaciones de formularios
  - Cambiar clases, estilos, etc.

