# 🧪 Ejemplo 2: Lista de productos con objeto

```jsx
const productos = [
  { id: 1, nombre: "Camisa", precio: 25 },
  { id: 2, nombre: "Pantalón", precio: 40 },
  { id: 3, nombre: "Zapatos", precio: 60 }
];

function ListaProductos() {
  return (
    <ul>
      {productos.map((producto) => (
        <li key={producto.id}>
          {producto.nombre} - ${producto.precio}
        </li>
      ))}
    </ul>
  );
}
```

✅ ¿Qué hace este componente?

* Muestra una lista de productos con nombre y precio.
* Usa `key={producto.id}` que es una buena práctica.

🧠 ¿Qué conceptos aplica?

* Iteración sobre arrays de objetos.
* Uso de propiedades internas como key.

📌 Ejemplo de uso:

```jsx
<ListaProductos />
```
---

## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md) 
## [📄 Modulo 10](../Modulo_10.md)
## [🏠 Inicio](../../README.md)
