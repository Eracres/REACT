# 🧪 Ejemplo 4: Mouse over para resaltar texto

Este componente cambia el color del texto cuando el mouse pasa por encima.

```jsx
function TextoInteractivo() {
  const [resaltado, setResaltado] = useState(false);

  return (
    <p
      onMouseOver={() => setResaltado(true)}
      onMouseOut={() => setResaltado(false)}
      style={{ color: resaltado ? "red" : "black" }}
    >
      Pasa el mouse por aquí
    </p>
  );
}
```

✅ ¿Qué hace este componente?

* Cambia el color del texto cuando el mouse pasa sobre él.

🧠 ¿Qué conceptos aplica?

* Eventos `onMouseOver` y `onMouseOut`.
* Estado booleano.

📌 Ejemplo de uso:

```jsx
<TextoInteractivo />
```

💡 Variaciones sugeridas:

Usar el mismo patrón para mostrar tooltips o animaciones.

---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md)

## [📄 Modulo 7](../Modulo_7.md) 

## [🏠 Inicio](../../README.md) 
