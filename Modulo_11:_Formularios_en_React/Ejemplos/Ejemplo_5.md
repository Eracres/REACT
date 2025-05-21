# 🧪 Ejemplo 5: Campo controlado #5

```jsx
import { useState } from "react";

function CampoControlado5() {
  const [valor, setValor] = useState("");

  return (
    <div>
      <label>Campo 5: </label>
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
<CampoControlado5 />
```
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 11](../Modulo_11.md)
## [🏠 Inicio](../../README.md)
