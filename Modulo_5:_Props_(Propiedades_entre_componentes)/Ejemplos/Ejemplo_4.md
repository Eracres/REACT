# 🧪 Ejemplo 4: Mostrar disponibilidad de producto

Este componente muestra la información de un producto, incluyendo si está disponible o no. Se basa en props para personalizar cada tarjeta.

```jsx
function Producto({ nombre, precio, disponible }) {
  return (
    <div>
      <h3>{nombre}</h3>
      <p>Precio: ${precio}</p>
      <p>{disponible ? "Disponible ✅" : "Agotado ❌"}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Recibe 3 props: `nombre`, `precio` y `disponible`.
* Muestra el precio y estado del producto.
* Usa un condicional (`? :`) para mostrar un mensaje dinámico según disponibilidad.

🧠 ¿Qué conceptos aplica?

* Paso de props con distintos tipos: string, number y boolean.
* Uso de operador ternario para condicionales en JSX.

📌 Ejemplo de uso:

```jsx
<Producto nombre="Auriculares" precio={29.99} disponible={true} />
<Producto nombre="Teclado" precio={49.99} disponible={false} />
```

---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 
