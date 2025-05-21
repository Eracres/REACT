# 🧪 Ejemplo 6: Listener de eventos del teclado

Este componente detecta cuando el usuario presiona una tecla globalmente.

```jsx
import { useEffect, useState } from "react";

function EscucharTecla() {
  const [tecla, setTecla] = useState("");

  useEffect(() => {
    const manejarTecla = (e) => setTecla(e.key);

    window.addEventListener("keydown", manejarTecla);
    return () => window.removeEventListener("keydown", manejarTecla);
  }, []);

  return <p>Última tecla presionada: {tecla}</p>;
}
```

✅ ¿Qué hace este componente?

* Escucha teclas presionadas y muestra la última capturada.

🧠 ¿Qué conceptos aplica?

* Escuchadores de eventos en `useEffect`.
* Limpieza al desmontar.

📌 Ejemplo de uso:

```jsx
<EscucharTecla />
```

💡 Variaciones sugeridas:

Mostrar un historial de teclas presionadas.

---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 8](../Modulo_8.md)
## [🏠 Inicio](../../README.md)
