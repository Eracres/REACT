# 🧪 Ejemplo 1: Formulario de nombre

```jsx
import { useState } from "react";

function FormularioNombre() {
  const [nombre, setNombre] = useState("");

  const manejarEnvio = (e) => {
    e.preventDefault();
    alert(`Nombre enviado: ${nombre}`);
    setNombre("");
  };

  return (
    <form onSubmit={manejarEnvio}>
      <input
        type="text"
        value={nombre}
        onChange={(e) => setNombre(e.target.value)}
        placeholder="Tu nombre"
      />
      <button type="submit">Enviar</button>
    </form>
  );
}
```

✅ ¿Qué hace este componente?

* Controla un campo input usando `useState`.
* Muestra un alert con el valor al enviar.
* Limpia el campo después del envío.

🧠 ¿Qué conceptos aplica?

* Formulario controlado con estado.
* `onChange` y `onSubmit` en acción.

📌 Ejemplo de uso:

```jsx
<FormularioNombre />
```
---

## [⬅️](../../Modulo_10:_Listas_y_Claves/Modulo_10.md) Módulo 10 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md) 
## [📄 Modulo 11](../Modulo_11.md)
## [🏠 Inicio](../../README.md)

