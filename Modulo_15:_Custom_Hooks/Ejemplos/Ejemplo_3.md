# 🧪 Ejemplo 3: useContador3

```jsx
import { useState } from "react";

function useContador3(inicial = 0) {
  const [valor, setValor] = useState(inicial);

  const incrementar = () => setValor((prev) => prev + 1);
  const decrementar = () => setValor((prev) => prev - 1);

  return { valor, incrementar, decrementar };
}

function Contador3() {
  const { valor, incrementar, decrementar } = useContador3(5);

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
<Contador3 />
```
---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md) 
## [📄 Modulo 15](../Modulo_15.md)
## [🏠 Inicio](../../README.md)
