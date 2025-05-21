# 🧪 Ejemplo 4: useContador4

```jsx
import { useState } from "react";

function useContador4(inicial = 0) {
  const [valor, setValor] = useState(inicial);

  const incrementar = () => setValor((prev) => prev + 1);
  const decrementar = () => setValor((prev) => prev - 1);

  return { valor, incrementar, decrementar };
}

function Contador4() {
  const { valor, incrementar, decrementar } = useContador4(5);

  return (
    <div>
      <p>Contador: {valor}</p>
      <button onClick={incrementar}>Sumar</button>
      <button onClick={decrementar}>Restar</button>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Usa un hook personalizado para manejar lógica de contador.
* Puede incrementarse o decrementarse según botones.
* El estado inicial es configurable.

📌 Ejemplo de uso:

```jsx
<Contador4 />
```
---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md) 
## [📄 Modulo 15](../Modulo_15.md)
## [🏠 Inicio](../../README.md)
