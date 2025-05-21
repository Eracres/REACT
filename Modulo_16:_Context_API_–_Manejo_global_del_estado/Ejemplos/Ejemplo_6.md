# 🧪 Ejemplo 6: Contexto genérico 6

```jsx
import { createContext, useState, useContext } from "react";

const MiContexto6 = createContext();

function Proveedor6({ children }) {
  const [valor, setValor] = useState("Ejemplo 6");

  return (
    <MiContexto6.Provider value={ valor }>
      {children}
    </MiContexto6.Provider>
  );
}

function MostrarValor6() {
  const valor = useContext(MiContexto6);
  return <p>Contexto dice: {valor}</p>;
}

function AppContext6() {
  return (
    <Proveedor6>
      <MostrarValor6 />
    </Proveedor6>
  );
}
```

✅ ¿Qué hace este componente?

* Declara un contexto independiente para una variable.
* La muestra en un componente consumidor usando `useContext`.

📌 Ejemplo de uso:

```jsx
<AppContext6 />
```
---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 16](../Modulo_16.md)
## [🏠 Inicio](../../README.md)
