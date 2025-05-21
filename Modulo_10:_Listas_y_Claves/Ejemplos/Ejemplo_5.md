# 🧪 Ejemplo 5: Estilo condicional por props

```jsx
function Etiqueta({ importante }) {
  const estilo = {
    color: importante ? "red" : "black",
    fontWeight: importante ? "bold" : "normal",
  };

  return <span style={estilo}>¡Etiqueta dinámica!</span>;
}
```

✅ ¿Qué hace este componente?

* Aplica estilos diferentes dependiendo del valor de una prop.

🧠 ¿Qué conceptos aplica?

* Props + estilos dinámicos.

📌 Ejemplo de uso:

```jsx
<Etiqueta importante={true} />
```

💡 Variaciones sugeridas:

* Añadir icono si es importante.
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 10](../Modulo_10.md)
## [🏠 Inicio](../../README.md)
