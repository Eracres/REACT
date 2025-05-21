# 🧪 Ejemplo 4: Redux funcional 4

```jsx
import { createSlice } from "@reduxjs/toolkit";

const contadorSlice4 = createSlice({
  name: "contador4",
  initialState: 0,
  reducers: {
    incrementar: (state) => state + 1,
  },
});

export const { incrementar } = contadorSlice4.actions;
export default contadorSlice4.reducer;
```

✅ ¿Qué hace este slice?

* Controla un estado simple numérico en Redux Toolkit.
* Expande la lógica a múltiples contadores si se desea.

📌 Uso:

```jsx
dispatch(incrementar());
```
---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md) 
## [📄 Modulo 17](../Modulo_17.md)
## [🏠 Inicio](../../README.md)
