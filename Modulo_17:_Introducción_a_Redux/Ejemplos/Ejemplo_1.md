# 🧪 Ejemplo 1: Contador con Redux Toolkit

```jsx
// contadorSlice.js
import { createSlice } from "@reduxjs/toolkit";

const contadorSlice = createSlice({
  name: "contador",
  initialState: 0,
  reducers: {
    incrementar: (state) => state + 1,
    reiniciar: () => 0,
  },
});

export const { incrementar, reiniciar } = contadorSlice.actions;
export default contadorSlice.reducer;
```

```jsx
// store.js
import { configureStore } from "@reduxjs/toolkit";
import contadorReducer from "./contadorSlice";

export const store = configureStore({
  reducer: {
    contador: contadorReducer,
  },
});
```

```jsx
// index.js
import React from "react";
import ReactDOM from "react-dom/client";
import { Provider } from "react-redux";
import { store } from "./store";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <Provider store={store}>
    <App />
  </Provider>
);
```

```jsx
// ContadorRedux.js
import { useSelector, useDispatch } from "react-redux";
import { incrementar, reiniciar } from "./contadorSlice";

function ContadorRedux() {
  const contador = useSelector((state) => state.contador);
  const dispatch = useDispatch();

  return (
    <div>
      <p>Contador Redux: {contador}</p>
      <button onClick={() => dispatch(incrementar())}>Incrementar</button>
      <button onClick={() => dispatch(reiniciar())}>Reiniciar</button>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Maneja el estado global de un contador con Redux Toolkit.
* Utiliza `useSelector` para leer el estado y `useDispatch` para modificarlo.

📌 Ejemplo de uso:

```jsx
<ContadorRedux />
```
---

## [⬅️](../../Modulo_16:_Context_API_–_Manejo_global_del_estado/Modulo16.md) Módulo 17 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md) 
## [📄 Modulo 17](../Modulo_17.md)
## [🏠 Inicio](../../README.md)
