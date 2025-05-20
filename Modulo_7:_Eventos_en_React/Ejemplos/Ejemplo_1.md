
# 🧪 Ejemplo 1: Botón con alerta

Este componente muestra un botón que ejecuta una alerta al hacer clic.

```jsx
function EventoClick() {
  const manejarClick = () => {
    alert("¡Haz hecho clic!");
  };

  return <button onClick={manejarClick}>Haz clic aquí</button>;
}
```

✅ ¿Qué hace este componente?

* Muestra un botón que al hacer clic lanza una alerta.

🧠 ¿Qué conceptos aplica?

* Evento `onClick`.
* Función manejadora externa.

📌 Ejemplo de uso:

```jsx
<EventoClick />
```

💡 Variaciones sugeridas:

Cambia el texto de la alerta según una prop.

---

## [⬅️](../Modulo_6.md) Modulo 6 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md)
## [📄 Modulo 7](../Modulo_7.md)
## [🏠 Inicio](../../README.md)
