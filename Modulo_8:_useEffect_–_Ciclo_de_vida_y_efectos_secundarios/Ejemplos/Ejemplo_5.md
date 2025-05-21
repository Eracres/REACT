# 🧪 Ejemplo 5: Contador con cleanup

Este componente limpia correctamente el `setInterval` para evitar problemas.

```jsx
import { useEffect, useState } from "react";

function ContadorSeguro() {
  const [cuenta, setCuenta] = useState(0);

  useEffect(() => {
    const id = setInterval(() => {
      setCuenta((prev) => prev + 1);
    }, 1000);

    return () => clearInterval(id);
  }, []);

  return <p>Contador seguro: {cuenta}</p>;
}
```

✅ ¿Qué hace este componente?

* Ejecuta un efecto continuo.
* Lo detiene cuando el componente se desmonta.

🧠 ¿Qué conceptos aplica?

* Limpieza de efectos (`return` en `useEffect`).

📌 Ejemplo de uso:

```jsx
<ContadorSeguro />
```

💡 Variaciones sugeridas:

Agregar botón para detener el contador manualmente.

---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md)

## [📄 Modulo 8](../Modulo_8.md) 

## [🏠 Inicio](../../README.md) 
