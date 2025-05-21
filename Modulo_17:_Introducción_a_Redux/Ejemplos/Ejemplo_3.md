# 🧪 Ejemplo 3: Redux funcional 3

```jsx
import { createSlice } from "@reduxjs/toolkit";

const contadorSlice3 = createSlice({
  name: "contador3",
  initialState: 0,
  reducers: {
    incrementar: (state) => state + 1,
  },
});

export const { incrementar } = contadorSlice3.actions;
export default contadorSlice3.reducer;
```

✅ ¿Qué hace este slice?

* Controla un estado simple numérico en Redux Toolkit.
* Expande la lógica a múltiples contadores si se desea.

📌 Uso:

```jsx
dispatch(incrementar());
```
---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md) 
## [📄 Modulo 17](../Modulo_17.md)
## [🏠 Inicio](../../README.md)
