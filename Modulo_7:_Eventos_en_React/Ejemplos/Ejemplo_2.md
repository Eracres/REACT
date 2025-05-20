# 🧪 Ejemplo 2: Captura de texto en un input

Este componente muestra cómo capturar texto con `onChange`.

```jsx
import { useState } from "react";

function InputNombre() {
  const [nombre, setNombre] = useState("");

  const manejarCambio = (e) => {
    setNombre(e.target.value);
  };

  return (
    <div>
      <input type="text" onChange={manejarCambio} />
      <p>Tu nombre es: {nombre}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Captura texto ingresado en tiempo real.
* Muestra el valor actual del input bajo el campo.

🧠 ¿Qué conceptos aplica?

* `useState` para capturar entrada.
* Evento `onChange` en formularios.

📌 Ejemplo de uso:

```jsx
<InputNombre />
```

💡 Variaciones sugeridas:

Agregar validación para que solo acepte letras.

---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md) 
## [📄 Modulo 7](../Modulo_7.md)
## [🏠 Inicio](../../README.md)

