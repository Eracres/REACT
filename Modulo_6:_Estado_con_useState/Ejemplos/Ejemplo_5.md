# 🧪 Ejemplo 5: Toggle de modo claro/oscuro

```jsx
function ModoOscuro() {
  const [modo, setModo] = useState("claro");

  const alternarModo = () => {
    setModo(modo === "claro" ? "oscuro" : "claro");
  };

  return (
    <div style={{
      backgroundColor: modo === "claro" ? "#fff" : "#333",
      color: modo === "claro" ? "#000" : "#fff",
      padding: "1rem"
    }}>
      <p>Modo actual: {modo}</p>
      <button onClick={alternarModo}>Cambiar modo</button>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Alterna entre dos temas: claro y oscuro.
* Aplica estilos en línea según el modo.

🧠 ¿Qué conceptos aplica?

* Estado con strings.
* Estilos dinámicos en React.

✅ ¿Qué puedes aprender de esto?

* Cómo cambiar el diseño visual de un componente con estado.

💡 Variaciones sugeridas:

Agregar un ícono según el modo o guardar la preferencia en localStorage.

---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
