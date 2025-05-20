# 🧪 Ejemplo 4: Lista dinámica de tareas

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

* Permite ingresar tareas en una lista.
* Usa dos estados: uno para el input y otro para la lista.

🧠 ¿Qué conceptos aplica?

* `useState` con arrays.
* Manipulación de listas con `map`.

✅ ¿Qué puedes aprender de esto?

* Cómo gestionar arrays de datos con React.

💡 Variaciones sugeridas:

Agregar la posibilidad de eliminar tareas o editar.

---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
