# 🧪 Ejemplo 5: Toggle de modo claro/oscuro

Este componente alterna entre un fondo claro y uno oscuro.

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

* Cambia el tema visual de claro a oscuro.

🧠 ¿Qué conceptos aplica?

* Estilos condicionales.
* Estado con strings.

📌 Ejemplo de uso:

```jsx
<ModoOscuro />
```

💡 Variaciones sugeridas:

Guardar el modo en localStorage.

---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
