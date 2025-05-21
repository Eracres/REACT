# 🧪 Ejemplo 3: Lista dinámica 3

```jsx
function Lista3() {
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
<Lista3 />
```
---

## [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - [➡️](../Ejemplos/Ejemplo_4.md) Ejemplo 4
## [📄 Modulo 10](../Modulo_10.md)
## [🏠 Inicio](../../README.md)

