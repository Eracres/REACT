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
