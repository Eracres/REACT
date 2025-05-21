# 🧪 Ejemplo 6: Comunicación padre-hijo 6

```jsx
import { useState } from "react";

function Hijo6(props) {
  return (
    <div>
      <input value={props.valor} onChange={(e) => props.onUpdate(e.target.value)} />
      <p>Valor recibido: {props.valor}</p>
    </div>
  );
}

function Padre6() {
  const [texto, setTexto] = useState("");

  return (
    <div>
      <Hijo6 valor={texto} onUpdate={setTexto} />
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
<Padre6 />
```
---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 12](../Modulo_12.md)
## [🏠 Inicio](../../README.md)
