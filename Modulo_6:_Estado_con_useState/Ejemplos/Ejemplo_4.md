# 🧪 Ejemplo 4: Lista dinámica de tareas

Este componente permite al usuario agregar tareas a una lista.

```jsx
function ListaTareas() {
  const [tareas, setTareas] = useState([]);
  const [nueva, setNueva] = useState("");

  const agregarTarea = () => {
    setTareas([...tareas, nueva]);
    setNueva("");
  };

  return (
    <div>
      <input
        type="text"
        value={nueva}
        onChange={(e) => setNueva(e.target.value)}
      />
      <button onClick={agregarTarea}>Agregar</button>
      <ul>
        {tareas.map((tarea, index) => (
          <li key={index}>{tarea}</li>
        ))}
      </ul>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Agrega tareas a una lista desde el input.
* Usa dos estados: uno para el input y otro para la lista.

🧠 ¿Qué conceptos aplica?

* Manejo de arrays con `useState`.
* Renderizado con `.map`.

📌 Ejemplo de uso:

```jsx
<ListaTareas />
```

💡 Variaciones sugeridas:

Permitir eliminar o editar tareas.

---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
