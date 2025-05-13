# 🧪 Ejemplo 3: Componente de clase

```jsx
import React, { Component } from 'react';

class TarjetaClase extends Component {
  render() {
    return (
      <div>
        <h3>React desde clase</h3>
        <p>Este es un componente basado en clase</p>
      </div>
    );
  }
}
```

✅ ¿Qué hace este componente?

* Declara un componente como clase usando ES6.
* Usa el método `render()` para devolver JSX.

🧠 ¿Qué conceptos aplica?

* Componentes de clase (anteriores a hooks).
* Estructura basada en POO (Programación Orientada a Objetos).

✅ ¿Qué puedes aprender de esto?

* Aunque están en desuso, los componentes de clase siguen siendo válidos.
* Son útiles para entender proyectos legacy.

💡 Variaciones sugeridas:

Agrega un constructor con estado:

```jsx
constructor(props) {
  super(props);
  this.state = { mensaje: "Hola desde clase" };
}
```

---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 
