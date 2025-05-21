# 🧪 Ejemplo 6: Campo controlado #6

```jsx
import { useState } from "react";

function CampoControlado6() {
  const [valor, setValor] = useState("");

  return (
    <div>
      <label>Campo 6: </label>
      <input value={valor} onChange={(e) => setValor(e.target.value)} />
      <p>Valor actual: {valor}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Controla el valor de un input con `useState`.
* Muestra el valor actualizado en tiempo real.

🧠 ¿Qué conceptos aplica?

* Estado controlado en formularios.
* Input reactivo al escribir.

📌 Ejemplo de uso:

```jsx
<CampoControlado6 />
```
---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 11](../Modulo_11.md)
## [🏠 Inicio](../../README.md)
