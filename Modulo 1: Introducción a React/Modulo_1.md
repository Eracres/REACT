<a name="modulo-1-introducción-a-React"></a>
## 📘 Módulo 1: Introducción a React

### ❓ ¿Qué es React?

React es una biblioteca de JavaScript creada por Facebook para construir interfaces de usuario. Su objetivo principal es crear aplicaciones web reactivas, eficientes y modulares.

### 💡 Ventajas clave:
- Componentes reutilizables
- Virtual DOM (mejora el rendimiento)
- Flujo de datos unidireccional (unidirectional data flow)
- Ideal para SPAs (Single Page Applications)


### 🧪 Ejemplo básico: crear un componente

Puedes crear HolaMundo directamente dentro del archivo App.js, o mejor aún, en su propio archivo para seguir buenas prácticas.

Tenemos 2 maneras de hacerlo:

🔹 Opción A – Dentro de App.js:

```jsx
// src/App.js
import React from 'react';

function HolaMundo() {
  return <h1>¡Hola, mundo desde React!</h1>;
}

function App() {
  return (
    <div>
      <HolaMundo />
    </div>
  );
}

export default App;
```

🔹 Opción B – En su propio archivo:

1. Crea un archivo nuevo llamado HolaMundo.js dentro de /src

2. Pon esto dentro:

```jsx
// src/HolaMundo.js
import React from 'react';

function HolaMundo() {
  return <h1>¡Hola, mundo desde React!</h1>;
}

export default HolaMundo;
```

3. Ahora importa y usa HolaMundo dentro de App.js:

```jsx
// src/App.js
import React from 'react';
import HolaMundo from './HolaMundo';

function App() {
  return (
    <div>
      <HolaMundo />
    </div>
  );
}

export default App;
```

Esto sería un componente muy básico en React.
