# 🧪 Ejemplo 2: Contexto genérico 2

```jsx
import { createContext, useState, useContext } from "react";

const MiContexto2 = createContext();

function Proveedor2({ children }) {
  const [valor, setValor] = useState("Ejemplo 2");

  return (
    <MiContexto2.Provider value={ valor }>
      {children}
    </MiContexto2.Provider>
  );
}

function MostrarValor2() {
  const valor = useContext(MiContexto2);
  return <p>Contexto dice: {valor}</p>;
}

function AppContext2() {
  return (
    <Proveedor2>
      <MostrarValor2 />
    </Proveedor2>
  );
}
```

✅ ¿Qué hace este componente?

* Declara un contexto independiente para una variable.
* La muestra en un componente consumidor usando `useContext`.

📌 Ejemplo de uso:

```jsx
<AppContext2 />
```
---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md) 
## [📄 Modulo 16](../Modulo_16.md)
## [🏠 Inicio](../../README.md)

