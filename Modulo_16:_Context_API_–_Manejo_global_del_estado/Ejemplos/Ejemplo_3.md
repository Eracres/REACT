# 🧪 Ejemplo 3: Contexto genérico 3

```jsx
import { createContext, useState, useContext } from "react";

const MiContexto3 = createContext();

function Proveedor3({ children }) {
  const [valor, setValor] = useState("Ejemplo 3");

  return (
    <MiContexto3.Provider value={ valor }>
      {children}
    </MiContexto3.Provider>
  );
}

function MostrarValor3() {
  const valor = useContext(MiContexto3);
  return <p>Contexto dice: {valor}</p>;
}

function AppContext3() {
  return (
    <Proveedor3>
      <MostrarValor3 />
    </Proveedor3>
  );
}
```

✅ ¿Qué hace este componente?

* Declara un contexto independiente para una variable.
* La muestra en un componente consumidor usando `useContext`.

📌 Ejemplo de uso:

```jsx
<AppContext3 />
```
---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md) 
## [📄 Modulo 16](../Modulo_16.md)
## [🏠 Inicio](../../README.md)
