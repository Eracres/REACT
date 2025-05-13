# 🧪 Ejemplo 4: Componente con props

```jsx
function TarjetaUsuario({ nombre, edad }) {
  return (
    <div className="tarjeta">
      <h3>{nombre}</h3>
      <p>Edad: {edad}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Recibe datos por medio de props (`nombre` y `edad`).
* Muestra contenido dinámico en pantalla.

🧠 ¿Qué conceptos aplica?

* Props: permiten hacer componentes dinámicos y reutilizables.
* Desestructuración de props en los parámetros.

✅ ¿Qué puedes aprender de esto?

* Puedes reutilizar este componente con distintos valores sin modificar su lógica.

💡 Variaciones sugeridas:

```jsx
<TarjetaUsuario nombre="Ana" edad={25} />
<TarjetaUsuario nombre="Luis" edad={30} />
```

---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 
