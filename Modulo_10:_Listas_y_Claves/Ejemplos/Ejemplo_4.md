# 🧪 Ejemplo 4: Lista dinámica 4

```jsx
function Lista4() {
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
<Lista4 />
```
---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md) 
## [📄 Modulo 10](../Modulo_10.md)
## [🏠 Inicio](../../README.md)


