# 🧪 Ejemplo 2: Mostrar/Ocultar texto

Este componente permite mostrar u ocultar un texto haciendo clic en un botón.

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

* Muestra u oculta contenido con base en un valor booleano.

🧠 ¿Qué conceptos aplica?

* `useState` booleano.
* Renderizado condicional.
* Operadores ternarios.

📌 Ejemplo de uso:

```jsx
<MostrarOcultar />
```

💡 Variaciones sugeridas:

Agregar diferentes estilos cuando el contenido está oculto o visible.

---

##  [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejemplo 3 [➡️](../Ejemplos/Ejemplo_3.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
