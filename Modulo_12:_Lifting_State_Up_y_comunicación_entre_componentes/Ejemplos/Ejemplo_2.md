# 🧪 Ejemplo 2: Comunicación padre-hijo 2

```jsx
import { useState } from "react";

function Hijo2(props) {
  return (
    <div>
      <input value={props.valor} onChange={(e) => props.onUpdate(e.target.value)} />
      <p>Valor recibido: {props.valor}</p>
    </div>
  );
}

function Padre2() {
  const [texto, setTexto] = useState("");

  return (
    <div>
      <Hijo2 valor={texto} onUpdate={setTexto} />
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Controla el estado `texto` en el componente padre.
* Lo comparte con el hijo que lo modifica a través de `props`.

🧠 ¿Qué conceptos aplica?

* Lifting state: el input está en el hijo, el estado en el padre.
* Funciones que modifican el estado compartidas por `props`.

📌 Ejemplo de uso:

```jsx
<Padre2 />
```
---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md) 
## [📄 Modulo 12](../Modulo_12.md)
## [🏠 Inicio](../../README.md)
