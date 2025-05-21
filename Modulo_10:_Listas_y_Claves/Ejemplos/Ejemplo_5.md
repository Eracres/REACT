 🧪 Ejemplo 5: Lista dinámica 5

```jsx
function Lista5() {
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
<Lista5 />
```
---

## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md) 
## [📄 Modulo 10](../Modulo_10.md)
## [🏠 Inicio](../../README.md)
