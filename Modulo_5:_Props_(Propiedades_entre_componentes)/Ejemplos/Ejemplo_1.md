# 🧪 Ejemplo 1: Mostrar datos de usuario con props

Este componente utiliza props para mostrar un nombre y una edad de forma personalizada en pantalla.

```jsx
function Usuario(props) {
  return (
    <div>
      <h2>{props.nombre}</h2>
      <p>Edad: {props.edad}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Recibe `nombre` y `edad` como props desde su componente padre.
* Muestra los valores dentro de un `div`, con encabezado y párrafo.
* Puede reutilizarse para mostrar diferentes personas.

🧠 ¿Qué conceptos aplica?

* Paso de datos entre componentes mediante props.
* Encapsulamiento de lógica visual.
* Interpolación de variables dentro de JSX.

📌 Ejemplo de uso:

```jsx
<Usuario nombre="María" edad={29} />
<Usuario nombre="Lucas" edad={35} />
```

💡 Variaciones sugeridas:

Agregar condicional según la edad:

```jsx
<p>{edad >= 18 ? "Mayor de edad" : "Menor de edad"}</p>
```

---

## Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 
