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

* Usa un booleano para mostrar u ocultar contenido.
* Cambia dinámicamente el texto del botón.

---

##  [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
