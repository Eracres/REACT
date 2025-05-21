# 🧪 Ejemplo 4: Guardar en localStorage

Este componente guarda el nombre en `localStorage` cada vez que se modifica.

```jsx
import { useEffect, useState } from "react";

function NombrePersistente() {
  const [nombre, setNombre] = useState("");

  useEffect(() => {
    localStorage.setItem("nombre", nombre);
  }, [nombre]);

  return (
    <div>
      <input
        type="text"
        placeholder="Tu nombre"
        value={nombre}
        onChange={(e) => setNombre(e.target.value)}
      />
      <p>Nombre guardado: {nombre}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Guarda el valor del input en el almacenamiento local del navegador.

🧠 ¿Qué conceptos aplica?

* Sincronización con APIs del navegador (`localStorage`).
* `useEffect` dependiente de estado.

📌 Ejemplo de uso:

```jsx
<NombrePersistente />
```

💡 Variaciones sugeridas:

Leer el nombre al iniciar con otro `useEffect`.

---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md)

## [📄 Modulo 8](../Modulo_8.md) 

## [🏠 Inicio](../../README.md) 
