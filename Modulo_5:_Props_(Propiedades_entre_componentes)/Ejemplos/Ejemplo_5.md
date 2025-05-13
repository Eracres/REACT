# 🧪 Ejemplo 5: Botón con evento y props

Este componente crea un botón reutilizable que ejecuta una función al hacer clic. Tanto el texto como la acción se pasan como props.

```jsx
function BotonAccion({ texto, onClick }) {
  return <button onClick={onClick}>{texto}</button>;
}
```

✅ ¿Qué hace este componente?

* Muestra un botón con texto definido por la prop `texto`.
* Al hacer clic, ejecuta la función pasada como prop `onClick`.

🧠 ¿Qué conceptos aplica?

* Paso de funciones como props.
* Manejadores de eventos (`onClick`) en componentes reutilizables.

📌 Ejemplo de uso:

```jsx
<BotonAccion texto="Eliminar" onClick={() => alert("Elemento eliminado")} />
<BotonAccion texto="Guardar" onClick={() => console.log("Guardado")} />
```

💡 Variaciones sugeridas:

Agrega estilos, íconos o deshabilita el botón con una prop extra:

```jsx
<button onClick={onClick} disabled={deshabilitado}>
  {texto}
</button>
```

---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md)

## [📄 Modulo 5](../Modulo_5.md) 

## [🏠 Inicio](../../README.md) 

