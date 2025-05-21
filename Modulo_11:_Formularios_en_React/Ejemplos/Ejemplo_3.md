# 🧪 Ejemplo 3: Campo controlado #3

```jsx
import { useState } from "react";

function CampoControlado3() {
  const [valor, setValor] = useState("");

  return (
    <div>
      <label>Campo 3: </label>
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
<CampoControlado3 />
```
---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md) 
## [📄 Modulo 11](../Modulo_11.md)
## [🏠 Inicio](../../README.md)
