# 🧪 Ejemplo 4: Comunicación padre-hijo 4

```jsx
import { useState } from "react";

function Hijo4(props) {
  return (
    <div>
      <input value={props.valor} onChange={(e) => props.onUpdate(e.target.value)} />
      <p>Valor recibido: {props.valor}</p>
    </div>
  );
}

function Padre4() {
  const [texto, setTexto] = useState("");

  return (
    <div>
      <Hijo4 valor={texto} onUpdate={setTexto} />
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
<Padre4 />
```
---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md) 
## [📄 Modulo 12](../Modulo_12.md)
## [🏠 Inicio](../../README.md)
