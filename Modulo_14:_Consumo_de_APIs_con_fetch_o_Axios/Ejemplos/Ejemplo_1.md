# 🧪 Ejemplo 1: Obtener usuarios con fetch

```jsx
import { useState, useEffect } from "react";

function ListaUsuarios() {
  const [usuarios, setUsuarios] = useState([]);
  const [cargando, setCargando] = useState(true);

  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/users")
      .then((res) => res.json())
      .then((data) => {
        setUsuarios(data);
        setCargando(false);
      });
  }, []);

  if (cargando) return <p>Cargando usuarios...</p>;

  return (
    <ul>
      {usuarios.map((usuario) => (
        <li key={usuario.id}>{usuario.name}</li>
      ))}
    </ul>
  );
}
```

✅ ¿Qué hace este componente?

* Hace una petición GET al montar el componente.
* Muestra una lista de usuarios de la API pública.
* Controla el estado `cargando` y los datos obtenidos.

🧠 ¿Qué conceptos aplica?

* `useEffect` para efectos secundarios.
* `fetch()` y `.then()` para consumir una API.
* `useState` para guardar y mostrar datos externos.

📌 Ejemplo de uso:

```jsx
<ListaUsuarios />
```
---

## [⬅️](../../Modulo_13:_React_Router_–_Navegación_entre_páginas/Modulo_13.md) Módulo 13 - [➡️](../Ejemplos/Ejemplo_2.md) Ejemplo 2
## [📄 Modulo 14](../Modulo_14.md)
## [🏠 Inicio](../../README.md)
