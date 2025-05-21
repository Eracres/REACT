# 🧪 Ejemplo 2: Redux funcional 2

```jsx
import { createSlice } from "@reduxjs/toolkit";

const contadorSlice2 = createSlice({
  name: "contador2",
  initialState: 0,
  reducers: {
    incrementar: (state) => state + 1,
  },
});

export const { incrementar } = contadorSlice2.actions;
export default contadorSlice2.reducer;
```

✅ ¿Qué hace este slice?

* Controla un estado simple numérico en Redux Toolkit.
* Expande la lógica a múltiples contadores si se desea.

📌 Uso:

```jsx
dispatch(incrementar());
```
---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md) 
## [📄 Modulo 17](../Modulo_17.md)
## [🏠 Inicio](../../README.md)
