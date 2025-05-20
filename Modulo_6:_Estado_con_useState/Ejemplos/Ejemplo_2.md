
# 🧪 Ejemplo 2: Mostrar/Ocultar texto

```jsx
function MostrarOcultar() {
  const [visible, setVisible] = useState(true);

  return (
    <div>
      <button onClick={() => setVisible(!visible)}>
        {visible ? "Ocultar" : "Mostrar"}
      </button>
      {visible && <p>Este texto se puede ocultar</p>}
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Controla la visibilidad de un texto con un booleano.
* Cambia el texto del botón de forma dinámica.

🧠 ¿Qué conceptos aplica?

* `useState` con valores booleanos.
* Renderizado condicional.
* Operador ternario para mostrar el texto del botón.

✅ ¿Qué puedes aprender de esto?

* Cómo usar una variable booleana en estado para controlar la interfaz.

💡 Variaciones sugeridas:

Podrías mostrar diferentes bloques de contenido según el estado del booleano.

---

##  [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
