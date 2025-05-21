# 🧪 Ejemplo 2: Campo controlado #2

```jsx
import { useState } from "react";

function CampoControlado2() {
  const [valor, setValor] = useState("");

  return (
    <div>
      <label>Campo 2: </label>
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
<CampoControlado2 />
```
---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md) 
## [📄 Modulo 11](../Modulo_11.md)
## [🏠 Inicio](../../README.md)
