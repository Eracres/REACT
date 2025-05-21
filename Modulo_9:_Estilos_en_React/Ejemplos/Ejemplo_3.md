# 🧪 Ejemplo 3: Estilo dinámico con estado

```jsx
import { useState } from "react";

function BotonInteractivo() {
  const [activo, setActivo] = useState(false);

  return (
    <button
      style={{
        backgroundColor: activo ? "limegreen" : "gray",
        color: "white",
        padding: "10px",
      }}
      onClick={() => setActivo(!activo)}
    >
      {activo ? "Activo" : "Inactivo"}
    </button>
  );
}
```

✅ ¿Qué hace este componente?

* Cambia el estilo del botón al hacer clic.

🧠 ¿Qué conceptos aplica?

* `useState` para controlar estilos condicionales.

📌 Ejemplo de uso:

```jsx
<BotonInteractivo />
```

💡 Variaciones sugeridas:

* Cambiar más propiedades como el borde o agregar iconos.
---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - [➡️](../Ejemplos/Ejemplo_4.md) Ejemplo 4
## [📄 Modulo 9](../Modulo_9.md)
## [🏠 Inicio](../../README.md)

