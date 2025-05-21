# 🧪 Ejemplo 5: Contexto genérico 5

```jsx
import { createContext, useState, useContext } from "react";

const MiContexto5 = createContext();

function Proveedor5({ children }) {
  const [valor, setValor] = useState("Ejemplo 5");

  return (
    <MiContexto5.Provider value={ valor }>
      {children}
    </MiContexto5.Provider>
  );
}

function MostrarValor5() {
  const valor = useContext(MiContexto5);
  return <p>Contexto dice: {valor}</p>;
}

function AppContext5() {
  return (
    <Proveedor5>
      <MostrarValor5 />
    </Proveedor5>
  );
}
```

✅ ¿Qué hace este componente?

* Declara un contexto independiente para una variable.
* La muestra en un componente consumidor usando `useContext`.

📌 Ejemplo de uso:

```jsx
<AppContext5 />
```
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 16](../Modulo_16.md)
## [🏠 Inicio](../../README.md)
