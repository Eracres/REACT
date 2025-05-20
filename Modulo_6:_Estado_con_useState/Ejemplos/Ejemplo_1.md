# 🧪 Ejemplo 1: Contador simple

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

* Inicializa el contador en 0.
* Muestra el valor en pantalla.
* Aumenta el contador cada vez que haces clic en el botón.

🧠 ¿Qué conceptos aplica?

* useState para manejar valores numéricos.
* Eventos (`onClick`) para modificar el estado.

✅ ¿Qué puedes aprender de esto?

* Cada vez que se llama a `setContador`, React vuelve a renderizar el componente.

💡 Variaciones sugeridas:

Agregar un botón para restar:

```jsx
<button onClick={() => setContador(contador - 1)}>Restar</button>
```

---

## Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
