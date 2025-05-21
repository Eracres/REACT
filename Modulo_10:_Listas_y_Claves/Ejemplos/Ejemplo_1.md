# 🧪 Ejemplo 1: Lista de frutas con index

```jsx
const frutas = ["🍎 Manzana", "🍌 Banana", "🍇 Uva", "🍊 Naranja"];

function ListaFrutas() {
  return (
    <ul>
      {frutas.map((fruta, index) => (
        <li key={index}>{fruta}</li>
      ))}
    </ul>
  );
}
```

✅ ¿Qué hace este componente?

* Muestra una lista de frutas a partir de un array.
* Usa `.map()` para iterar y renderizar.
* Usa `index` como key (válido si la lista no cambia).

🧠 ¿Qué conceptos aplica?

* Renderizado dinámico con `.map()`.
* Uso de `key` para evitar errores en React.
* Componentes de lista en JSX.

📌 Ejemplo de uso:

```jsx
<ListaFrutas />
```

💡 Variaciones sugeridas:

- Probar con más frutas.
- Reemplazar index por un `id` único.
---

## [⬅️](../../Modulo_9:_Estilos_en_React/Modulo_9.md) Módulo 9 - Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md) 
## [📄 Modulo 10](../Modulo_10.md)
## [🏠 Inicio](../../README.md)
