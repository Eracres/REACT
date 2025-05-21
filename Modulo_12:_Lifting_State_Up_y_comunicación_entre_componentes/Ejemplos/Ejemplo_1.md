# 🧪 Ejemplo 1: Contador con lifting state

```jsx
import { useState } from "react";

function BotonIncrementar({ onClick }) {
  return <button onClick={onClick}>Incrementar</button>;
}

function MostrarContador({ valor }) {
  return <p>Valor actual: {valor}</p>;
}

function ContadorConLifting() {
  const [contador, setContador] = useState(0);

  const incrementar = () => setContador(contador + 1);

  return (
    <div>
      <MostrarContador valor={contador} />
      <BotonIncrementar onClick={incrementar} />
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Eleva el estado `contador` al componente padre `ContadorConLifting`.
* Lo comparte con `MostrarContador` y `BotonIncrementar`.
* La lógica se centraliza en el componente padre.

🧠 ¿Qué conceptos aplica?

* Comunicación entre componentes hermanos mediante lifting state.
* Flujo de datos descendente y funciones ascendentes.

📌 Ejemplo de uso:

```jsx
<ContadorConLifting />
```
---

## [⬅️](../../Modulo_11:_Formularios_en_React/Modulo_11.md) Módulo 11 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md) 
## [📄 Modulo 12](../Modulo_12.md)
## [🏠 Inicio](../../README.md)
