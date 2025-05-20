# 🧪 Ejemplo 3: Input controlado

Este componente captura el valor de un input de texto y lo muestra en tiempo real.

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

* Controla un input con estado.
* Muestra el valor escrito por el usuario en tiempo real.

🧠 ¿Qué conceptos aplica?

* Inputs controlados.
* `onChange` para capturar eventos de entrada.

📌 Ejemplo de uso:

```jsx
<FormularioNombre />
```

💡 Variaciones sugeridas:

Validar el input o limpiar el campo después de cierta acción.

---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
