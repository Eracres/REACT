### 🧪 Ejemplo básico 2: 

Crea un componente Saludo que:

* Reciba una prop nombre (string)
* Use una prop emoji (opcional, valor por defecto "👋")
* Muestre: ¡{emoji} Hola, {nombre}! Bienvenido/a al curso

```jsx
import PropTypes from 'prop-types';

const Saludo = ({ nombre, emoji = "👋" }) => {
  return (
    <div className="saludo">
      <p>¡{emoji} Hola, {nombre}! Bienvenido/a al curso</p>
    </div>
  );
};

Saludo.propTypes = {
  nombre: PropTypes.string.isRequired,
  emoji: PropTypes.string
};

export default Saludo;
```
---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Módulo 2 [➡️](../../Modulo_2:_Configuración_del_entorno_de_desarrollo/Modulo_2.md)

## [📄 Modulo 1](../Modulo_1.md) 

## [🏠 Inicio](../../README.md) 
