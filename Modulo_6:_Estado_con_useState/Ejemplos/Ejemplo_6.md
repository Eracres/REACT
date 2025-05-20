# 🧪 Ejemplo 6: Contador con incremento personalizado

Permite al usuario elegir en cuánto se incrementa el contador.

```jsx
function ContadorPersonalizado() {
  const [contador, setContador] = useState(0);
  const [paso, setPaso] = useState(1);

  return (
    <div>
      <h2>Contador: {contador}</h2>
      <input
        type="number"
        value={paso}
        onChange={(e) => setPaso(Number(e.target.value))}
      />
      <button onClick={() => setContador(contador + paso)}>Sumar</button>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Deja al usuario definir cuánto aumentar el contador.
* Usa dos estados: `contador` y `paso`.

🧠 ¿Qué conceptos aplica?

* `useState` con múltiples valores.
* Conversión de tipos con `Number`.

📌 Ejemplo de uso:

```jsx
<ContadorPersonalizado />
```

💡 Variaciones sugeridas:

Agregar botones para restar y reiniciar.

---

## [⬅️](../Ejemplos/Ejemplo_6.md) Ejemplo 6 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
