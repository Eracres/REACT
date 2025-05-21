# 🧪 Ejemplo 6: Lista dinámica 6

```jsx
function Lista6() {
  const datos = ["Elemento A", "Elemento B", "Elemento C"];
  return (
    <ul>
      {datos.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
}
```

✅ ¿Qué hace este componente?

* Genera una lista con elementos ficticios.
* Usa `index` como key.

🧠 ¿Qué conceptos aplica?

* Renderizado dinámico con `.map()` y `key`.

📌 Ejemplo de uso:

```jsx
<Lista6 />
```
---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 10](../Modulo_10.md)
## [🏠 Inicio](../../README.md)
