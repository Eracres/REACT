# 🧪 Ejemplo 4: Campo controlado #4

```jsx
import { useState } from "react";

function CampoControlado4() {
  const [valor, setValor] = useState("");

  return (
    <div>
      <label>Campo 4: </label>
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
<CampoControlado4 />
```
---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md) 
## [📄 Modulo 11](../Modulo_11.md)
## [🏠 Inicio](../../README.md)
