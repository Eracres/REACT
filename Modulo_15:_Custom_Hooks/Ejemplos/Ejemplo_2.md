# 🧪 Ejemplo 2: useContador2

```jsx
import { useState } from "react";

function useContador2(inicial = 0) {
  const [valor, setValor] = useState(inicial);

  const incrementar = () => setValor((prev) => prev + 1);
  const decrementar = () => setValor((prev) => prev - 1);

  return { valor, incrementar, decrementar };
}

function Contador2() {
  const { valor, incrementar, decrementar } = useContador2(5);

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
<Contador2 />
```
---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md) 
## [📄 Modulo 15](../Modulo_15.md)
## [🏠 Inicio](../../README.md)
