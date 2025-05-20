# 🧪 Ejemplo 1: Contador simple

Este componente muestra un contador que puede incrementarse al hacer clic en un botón.

```jsx
import { useState } from "react";

function Contador() {
  const [contador, setContador] = useState(0);

  return (
    <div>
      <h2>Contador: {contador}</h2>
      <button onClick={() => setContador(contador + 1)}>Sumar</button>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Inicializa el contador en 0 y lo muestra en pantalla.
* Aumenta el contador en 1 cada vez que se hace clic en el botón.

🧠 ¿Qué conceptos aplica?

* `useState` para valores numéricos.
* Eventos con `onClick`.

📌 Ejemplo de uso:

```jsx
<Contador />
```

💡 Variaciones sugeridas:

Agregar botones para restar o reiniciar el contador.

---

## Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
