# 🧪 Ejemplo 5: Comunicación padre-hijo 5

```jsx
import { useState } from "react";

function Hijo5(props) {
  return (
    <div>
      <input value={props.valor} onChange={(e) => props.onUpdate(e.target.value)} />
      <p>Valor recibido: {props.valor}</p>
    </div>
  );
}

function Padre5() {
  const [texto, setTexto] = useState("");

  return (
    <div>
      <Hijo5 valor={texto} onUpdate={setTexto} />
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
<Padre5 />
```
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 12](../Modulo_12.md)
## [🏠 Inicio](../../README.md)
