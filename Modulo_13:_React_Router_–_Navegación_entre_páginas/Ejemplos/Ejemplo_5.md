# 🧪 Ejemplo 5: Ruta dinámica con parámetro

```jsx
import { BrowserRouter as Router, Routes, Route, Link, useParams } from "react-router-dom";

function Producto() {
  const { id } = useParams();
  return <h3>Detalles del producto con ID: {id}</h3>;
}

function AppRouter() {
  return (
    <Router>
      <nav>
        <Link to="/producto/1">Producto 1</Link> | <Link to="/producto/2">Producto 2</Link>
      </nav>
      <Routes>
        <Route path="/producto/:id" element={<Producto />} />
      </Routes>
    </Router>
  );
}
```

✅ ¿Qué hace este componente?

* Crea una ruta dinámica con el parámetro `:id`.
* Muestra el ID del producto desde la URL.
* Usa `useParams()` para extraer el valor.

🧠 ¿Qué conceptos aplica?

* Rutas dinámicas con parámetros.
* Acceso a datos de la URL.

📌 Ejemplo de uso:

```jsx
<AppRouter />
```
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 13](../Modulo_13.md)
## [🏠 Inicio](../../README.md)
