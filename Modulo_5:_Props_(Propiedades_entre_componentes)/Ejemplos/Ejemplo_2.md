# 🧪 Ejemplo 2: Desestructuración de props

Este componente muestra los mismos datos, pero de forma más legible usando desestructuración en los parámetros.

```jsx
function Usuario({ nombre, edad }) {
  return (
    <div>
      <h2>{nombre}</h2>
      <p>Edad: {edad}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Recibe los datos `nombre` y `edad` directamente como variables individuales.
* Mejora la legibilidad y simplicidad del código.

🧠 ¿Qué conceptos aplica?

* Desestructuración ES6 en parámetros de función.
* Uso de props en JSX.

📌 Ejemplo de uso:

```jsx
<Usuario nombre="Sofía" edad={22} />
```

---

##  [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md)

## [📄 Modulo 5](../Modulo_5.md) 

## [🏠 Inicio](../../README.md) 
