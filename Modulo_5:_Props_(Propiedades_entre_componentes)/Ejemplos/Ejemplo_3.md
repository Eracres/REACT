# 🧪 Ejemplo 3: Uso de props.children

Este componente recibe contenido dinámico dentro de la etiqueta del componente.

```jsx
function Contenedor({ children }) {
  return <div className="box">{children}</div>;
}
```

✅ ¿Qué hace este componente?

* Renderiza lo que haya entre la apertura y cierre del componente.
* Se puede usar como layout, tarjeta, o contenedor visual.

🧠 ¿Qué conceptos aplica?

* Uso de `props.children`, un mecanismo flexible para contenido anidado.
* Composición de componentes.

📌 Ejemplo de uso:

```jsx
<Contenedor>
  <p>Este es un párrafo dentro del contenedor</p>
</Contenedor>
```

💡 Variaciones sugeridas:

Estilizar con CSS o estilos en línea:

```jsx
<div style={{ border: "1px solid gray", padding: "10px" }}>{children}</div>
```

---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md)

## [📄 Modulo 5](../Modulo_5.md) 

## [🏠 Inicio](../../README.md) 
