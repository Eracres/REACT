# 🧪 Ejemplo 5: useContador5

```jsx
import { useState } from "react";

function useContador5(inicial = 0) {
  const [valor, setValor] = useState(inicial);

  const incrementar = () => setValor((prev) => prev + 1);
  const decrementar = () => setValor((prev) => prev - 1);

  return { valor, incrementar, decrementar };
}

function Contador5() {
  const { valor, incrementar, decrementar } = useContador5(5);

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
<Contador5 />
```
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 15](../Modulo_15.md)
## [🏠 Inicio](../../README.md)

