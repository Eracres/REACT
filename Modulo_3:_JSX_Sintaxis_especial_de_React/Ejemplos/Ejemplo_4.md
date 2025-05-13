# 🧪 Ejemplo 4: fragmentos y múltiples elementos
 
JSX solo puede devolver un elemento padre, así que usamos un contenedor (div, section) o un fragmento:

```jsx
function Fragmento() {
  return (
    <>
      <h2>Título</h2>
      <p>Parrafo debajo del título</p>
    </>
  );
}
```

✅ ¿Qué hace este componente?

Este componente devuelve dos elementos HTML consecutivos sin necesidad de envolverlos en un ```div```.
Gracias a los fragmentos (```<> </>```), se puede agrupar múltiples elementos sin añadir nodos extra al DOM.

🧠 ¿Por qué es importante?

JSX solo permite retornar un único nodo raíz.
Eso quiere decir que este código no funcionaría:

```jsx
return (
  <h2>Título</h2>
  <p>Texto</p>
);
```

Tienes dos opciones para solucionarlo:
1. Usar un contenedor como ```<div>```, ```<section>```, etc.
2. Usar un fragmento vacío: ```<> ... </>``` (como en el ejemplo)

💡 ¿Cuándo usar fragmentos?

* Cuando no necesitas un div visualmente, pero React te obliga a agrupar.
* Evitas generar elementos HTML innecesarios que podrían afectar el diseño o el DOM.

✅ Alternativa más explícita:
También puedes usar la forma completa de React.Fragment:

```jsx
return (
  <React.Fragment>
    <h2>Título</h2>
    <p>Texto</p>
  </React.Fragment>
);
```

---

##  [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md)

## [📄 Modulo 3](../Modulo_3.md) 

## [🏠 Inicio](../../README.md)
