# 🧪 Ejemplo 6: Contador con incremento personalizado

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

* Permite al usuario definir en cuánto se incrementa el contador.
* Usa dos estados: uno para el contador y otro para el paso.

🧠 ¿Qué conceptos aplica?

* Múltiples `useState`.
* Inputs de tipo numérico.
* Conversión de tipos (`Number`).

✅ ¿Qué puedes aprender de esto?

* Cómo adaptar el comportamiento de un componente a entradas del usuario.

💡 Variaciones sugeridas:

Agregar un botón para restar o reiniciar el contador.

---

## [⬅️](../Ejemplos/Ejemplo_6.md) Ejemplo 6 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md)

## [📄 Modulo 6](../Modulo_6.md) 

## [🏠 Inicio](../../README.md) 
