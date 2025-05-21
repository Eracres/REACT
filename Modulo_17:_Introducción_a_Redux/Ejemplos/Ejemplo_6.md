# 🧪 Ejemplo 6: Redux funcional 6

```jsx
import { createSlice } from "@reduxjs/toolkit";

const contadorSlice6 = createSlice({
  name: "contador6",
  initialState: 0,
  reducers: {
    incrementar: (state) => state + 1,
  },
});

export const { incrementar } = contadorSlice6.actions;
export default contadorSlice6.reducer;
```

✅ ¿Qué hace este slice?

* Controla un estado simple numérico en Redux Toolkit.
* Expande la lógica a múltiples contadores si se desea.

📌 Uso:

```jsx
dispatch(incrementar());
```
---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 17](../Modulo_17.md)
## [🏠 Inicio](../../README.md)
