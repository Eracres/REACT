# 🧪 Ejemplo 1: Hook personalizado para fetch (useFetch)

```jsx
import { useState, useEffect } from "react";

function useFetch(url) {
  const [datos, setDatos] = useState([]);
  const [cargando, setCargando] = useState(true);

  useEffect(() => {
    fetch(url)
      .then((res) => res.json())
      .then((data) => {
        setDatos(data);
        setCargando(false);
      });
  }, [url]);

  return { datos, cargando };
}
```

✅ ¿Qué hace este hook?

* Hace una petición HTTP cuando el componente se monta.
* Devuelve los datos y el estado de carga.
* Se puede reutilizar con cualquier URL.

📌 Ejemplo de uso:

```jsx
const { datos, cargando } = useFetch("https://jsonplaceholder.typicode.com/posts");
```
---

## [⬅️](../../Modulo_14:_Consumo_de_APIs_con_fetch_o_Axios/Modulo_14.md) Módulo 14 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md) 
## [📄 Modulo 15](../Modulo_15.md)
## [🏠 Inicio](../../README.md)

