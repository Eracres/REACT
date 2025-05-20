# 🧪 Ejemplo 3: Cambio de título con useEffect

Este componente cambia el título del documento según un estado.

```jsx
import { useEffect, useState } from "react";

function TituloDinamico() {
  const [titulo, setTitulo] = useState("React App");

  useEffect(() => {
    document.title = titulo;
  }, [titulo]);

  return (
    <div>
      <input
        type="text"
        value={titulo}
        onChange={(e) => setTitulo(e.target.value)}
      />
      <p>Título actualizado: {titulo}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Actualiza el `document.title` del navegador cuando cambia el input.

🧠 ¿Qué conceptos aplica?

* Acceso al DOM mediante `useEffect`.
* Dependencias específicas para evitar renders innecesarios.

📌 Ejemplo de uso:

```jsx
<TituloDinamico />
```

💡 Variaciones sugeridas:

Agregar un botón para resetear el título.

---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md)

## [📄 Modulo 8](../Modulo_8.md) 

## [🏠 Inicio](../../README.md) 
