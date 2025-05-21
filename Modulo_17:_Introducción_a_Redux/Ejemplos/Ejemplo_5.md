# 🧪 Ejemplo 5: Redux funcional 5

```jsx
import { createSlice } from "@reduxjs/toolkit";

const contadorSlice5 = createSlice({
  name: "contador5",
  initialState: 0,
  reducers: {
    incrementar: (state) => state + 1,
  },
});

export const { incrementar } = contadorSlice5.actions;
export default contadorSlice5.reducer;
```

✅ ¿Qué hace este slice?

* Controla un estado simple numérico en Redux Toolkit.
* Expande la lógica a múltiples contadores si se desea.

📌 Uso:

```jsx
dispatch(incrementar());
```
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 17](../Modulo_17.md)
## [🏠 Inicio](../../README.md)
