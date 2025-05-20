# 🧪 Ejemplo 3: Input controlado

```jsx
function FormularioNombre() {
  const [nombre, setNombre] = useState("");

  return (
    <div>
      <input
        type="text"
        placeholder="Escribe tu nombre"
        value={nombre}
        onChange={(e) => setNombre(e.target.value)}
      />
      <p>Hola, {nombre}!</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Controla un campo de entrada (input) mediante el estado.
* Muestra el valor actualizado del input en tiempo real.

🧠 ¿Qué conceptos aplica?

* Inputs controlados con `useState`.
* Eventos `onChange`.

✅ ¿Qué puedes aprender de esto?

* Cómo capturar y mostrar datos escritos por el usuario.

💡 Variaciones sugeridas:

Agregar una validación o limpiar el campo al enviar.

---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
