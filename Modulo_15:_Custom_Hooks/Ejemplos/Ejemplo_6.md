# 🧪 Ejemplo 6: useContador6

```jsx
import { useState } from "react";

function useContador6(inicial = 0) {
  const [valor, setValor] = useState(inicial);

  const incrementar = () => setValor((prev) => prev + 1);
  const decrementar = () => setValor((prev) => prev - 1);

  return { valor, incrementar, decrementar };
}

function Contador6() {
  const { valor, incrementar, decrementar } = useContador6(5);

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
<Contador6 />
```
---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 15](../Modulo_15.md)
## [🏠 Inicio](../../README.md)
