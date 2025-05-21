# 🧪 Ejemplo 4: Contexto genérico 4

```jsx
import { createContext, useState, useContext } from "react";

const MiContexto4 = createContext();

function Proveedor4({ children }) {
  const [valor, setValor] = useState("Ejemplo 4");

  return (
    <MiContexto4.Provider value={ valor }>
      {children}
    </MiContexto4.Provider>
  );
}

function MostrarValor4() {
  const valor = useContext(MiContexto4);
  return <p>Contexto dice: {valor}</p>;
}

function AppContext4() {
  return (
    <Proveedor4>
      <MostrarValor4 />
    </Proveedor4>
  );
}
```

✅ ¿Qué hace este componente?

* Declara un contexto independiente para una variable.
* La muestra en un componente consumidor usando `useContext`.

📌 Ejemplo de uso:

```jsx
<AppContext4 />
```
---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md) 
## [📄 Modulo 16](../Modulo_16.md)
## [🏠 Inicio](../../README.md)
