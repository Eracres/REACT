# 🧪 Ejemplo 2: condicionales y ternarios

```jsx
function Mensaje(props) {
  return (
    <div>
      <h2>{props.logueado ? "Bienvenido" : "Inicia sesión"}</h2>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

Este componente recibe una propiedad llamada logueado (tipo booleano), y en base a su valor muestra uno de dos mensajes:
* Si ```logueado === true``` → muestra ```"Bienvenido"```
* Si ```logueado === false``` → muestra ```"Inicia sesión"```
Esto se logra usando el operador ternario:
```condición ? valor_si_verdadero : valor_si_falso```

💡 ¿Por qué es útil?

En React muchas veces necesitas mostrar diferentes elementos en función del estado, por ejemplo:
* Un usuario logueado vs. uno anónimo
* Un carrito lleno vs. uno vacío
* Un botón activado vs. desactivado
Esto lo puedes resolver elegantemente con ternarios dentro del JSX.

---
## Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md)
