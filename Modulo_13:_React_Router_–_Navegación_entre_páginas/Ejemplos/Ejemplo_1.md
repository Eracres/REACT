# 🧪 Ejemplo 1: Navegación básica con dos rutas

```jsx
import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom";

function Home() {
  return <h2>Inicio</h2>;
}

function Acerca() {
  return <h2>Acerca de</h2>;
}

function Navegacion() {
  return (
    <nav>
      <Link to="/">Inicio</Link> | <Link to="/acerca">Acerca</Link>
    </nav>
  );
}

function AppRouter() {
  return (
    <Router>
      <Navegacion />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/acerca" element={<Acerca />} />
      </Routes>
    </Router>
  );
}
```

✅ ¿Qué hace este componente?

* Crea una navegación entre dos rutas: `/` e `/acerca`.
* Utiliza `<Link>` para cambiar de vista sin recargar la página.
* Encapsula las rutas dentro de `<Routes>`.

🧠 ¿Qué conceptos aplica?

* Uso de `react-router-dom` para navegación.
* Enrutamiento básico SPA.
* Separación de componentes por vista.

📌 Ejemplo de uso:

```jsx
<AppRouter />
```
---

## [⬅️](../Modulo_12:_Lifting_State_Up_y_comunicación_entre_componentes/Modulo_12.md) Módulo 12 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md) 
## [📄 Modulo 13](../Modulo_13.md)
## [🏠 Inicio](../../README.md)
