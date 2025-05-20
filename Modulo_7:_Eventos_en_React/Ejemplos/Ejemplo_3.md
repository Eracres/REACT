
# 🧪 Ejemplo 3: Validar formulario con onSubmit

Este componente muestra un formulario que se valida antes de enviarse.

```jsx
function ValidarFormulario() {
  const manejarEnvio = (e) => {
    e.preventDefault();
    alert("Formulario enviado correctamente");
  };

  return (
    <form onSubmit={manejarEnvio}>
      <input type="text" placeholder="Escribe algo" />
      <button type="submit">Enviar</button>
    </form>
  );
}
```

✅ ¿Qué hace este componente?

* Previene el comportamiento por defecto del formulario.
* Muestra un mensaje cuando se envía correctamente.

🧠 ¿Qué conceptos aplica?

* Evento `onSubmit`.
* `e.preventDefault()`.

📌 Ejemplo de uso:

```jsx
<ValidarFormulario />
```

💡 Variaciones sugeridas:

Agregar validaciones condicionales.

---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md)

## [📄 Modulo 7](../Modulo_7.md) 

## [🏠 Inicio](../../README.md) 
