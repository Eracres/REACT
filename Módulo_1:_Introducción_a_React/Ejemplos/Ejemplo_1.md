### 🧪 Ejemplo básico 1: 

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

## 🔍 [Ver resultado](https://eracres.github.io/REACT-ejericicios/ejemplo_1.html)

---

##  Ejemplo 2 [➡️](./Ejemplo_2.md)

## [📄 Modulo 1](../Modulo_1.md) 

## [🏠 Inicio](../../README.md) 
