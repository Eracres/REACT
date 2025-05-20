# 🧪 Ejemplo 1: Mensaje en consola al montar

Este componente imprime un mensaje en la consola solo una vez cuando se monta.

```jsx
import { useEffect } from "react";

function Temporizador() {
  useEffect(() => {
    console.log("Componente montado");
  }, []);

  return <p>Observa la consola</p>;
}
```

✅ ¿Qué hace este componente?

* Muestra un mensaje en consola cuando el componente se renderiza por primera vez.

🧠 ¿Qué conceptos aplica?

* `useEffect` con array de dependencias vacío (`[]`).
* Simulación de `componentDidMount`.

📌 Ejemplo de uso:

```jsx
<Temporizador />
```

💡 Variaciones sugeridas:

Mostrar una alerta en vez de un `console.log`.

---

## [⬅️](../Modulo_7.md) Módulo 7 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md)
## [📄 Modulo 8](../Modulo_8.md)
## [🏠 Inicio](../../README.md)
