# 🧪 Ejemplo 5: Componente reutilizable con props

Este componente muestra cómo reutilizar una misma estructura pasando distintos valores mediante **props**. Es muy útil para mostrar información personalizada sin duplicar código.

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

* Recibe los valores `nombre` y `edad` como props y los muestra en pantalla.
* Usa desestructuración directamente en los parámetros (`{ nombre, edad }`).
* Permite mostrar diferentes usuarios con el mismo componente.

🧠 ¿Qué conceptos aplica?

* Props (propiedades): permiten que los componentes sean dinámicos y reutilizables.
* Composición: puedes usar este componente dentro de otro componente padre.
* Buenas prácticas: los nombres de las props son descriptivos y el JSX está bien estructurado.

✅ ¿Qué puedes aprender de esto?

* Un componente puede cambiar completamente su contenido según los datos que reciba.
* Así evitamos repetir código para cada usuario.

💡 Variaciones sugeridas:

Puedes agregar un estilo dinámico basado en la edad:

```jsx
<p style={{ color: edad > 30 ? "red" : "green" }}>
  Edad: {edad}
</p>
```

📌 Ejemplo de uso:

```jsx
<TarjetaUsuario nombre="Ana" edad={25} />
<TarjetaUsuario nombre="Luis" edad={30} />
```

---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 

