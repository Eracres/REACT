# 🧪 Ejemplo 3: Petición simulada 3 con async/await

```jsx
import { useEffect, useState } from "react";

function Datos3() {
  const [datos, setDatos] = useState([]);
  const [cargando, setCargando] = useState(true);

  useEffect(() => {
    const obtenerDatos = async () => {
      try {
        const respuesta = await fetch("https://jsonplaceholder.typicode.com/posts?_limit=5");
        const resultado = await respuesta.json();
        setDatos(resultado);
      } catch (error) {
        console.error("Error al cargar:", error);
      } finally {
        setCargando(false);
      }
    };
    obtenerDatos();
  }, []);

  if (cargando) return <p>Cargando datos...</p>;

  return (
    <ul>
      {datos.map((item) => (
        <li key={item.id}>{item.title}</li>
      ))}
    </ul>
  );
}
```

✅ ¿Qué hace este componente?

* Simula una petición a una API.
* Usa `async/await` dentro de `useEffect`.
* Muestra títulos de publicaciones limitados a 5.

📌 Ejemplo de uso:

```jsx
<Datos3 />
```
---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md) 
## [📄 Modulo 14](../Modulo_14.md)
## [🏠 Inicio](../../README.md)
