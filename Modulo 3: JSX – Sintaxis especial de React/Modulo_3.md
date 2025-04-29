<a name="modulo-3-jsx-sintaxis-especial-de-react"></a>
## 📘 Módulo 3: JSX – Sintaxis especial de React

### ❓ ¿Qué es JSX?

JSX (JavaScript XML) es una extensión de sintaxis para JavaScript que nos permite escribir código muy similar a HTML dentro de archivos JavaScript.

En lugar de separar la lógica y la interfaz como en otros frameworks, React propone una mezcla controlada: combinamos lógica y estructura de forma declarativa usando JSX.

### 🔎 ¿Por qué es útil JSX?

- Nos permite ver visualmente la estructura del componente.
- Es más legible y cercano al HTML tradicional.
- Aumenta la productividad al unir lógica y presentación en un solo lugar.

### 🚨 Importante:

JSX no es HTML real, aunque lo parezca. Por ejemplo:

* En lugar de class, se usa className.
* Todos los elementos deben cerrarse correctamente (por ejemplo: ![]()).
* Los atributos siguen la convención camelCase (onClick, tabIndex, etc).

### 📌 Diferencias entre HTML y JSX

| En HTML        | En JSX                             |
|---------------|------------------------------------|
| ```class```     | ```className```       |
| ```for```    | ```htmlFor``` |
| ```onclick```    | ```onClick```      |
| Atributos vacíos | Se escriben como booleanos: ```disabled={true}``` |
| Etiquetas deben cerrarse | ```img```, ```input```, etc. se cierran como ```<img />``` |

### 💡 Recordatorio: JSX es solo sintaxis

Dentro del JSX puedes usar JavaScript puro entre llaves {}:

```jsx
const usuario = "Lucía";
return <h2>Bienvenida, {usuario}</h2>;
```
