# 🧪 Ejemplo 6: Componente de botón con texto personalizado

Este componente muestra cómo usar props para personalizar el contenido de un botón.

```jsx
function BotonPersonalizado({ texto }) {
  return <button>{texto}</button>;
}
```

✅ ¿Qué hace este componente?

* Recibe una prop `texto` que se usa como contenido del botón.
* El componente se puede usar múltiples veces con distintos textos.
* Muy útil para interfaces con botones genéricos.

🧠 ¿Qué conceptos aplica?

* Props básicas: paso de valores simples (string).
* Reutilización: el mismo componente para múltiples contextos.
* Estructura simple con una sola etiqueta (`<button>`).

✅ ¿Qué puedes aprender de esto?

* Puedes crear un componente altamente reutilizable con una sola línea.
* Los componentes no necesitan ser complejos para ser útiles.

💡 Variaciones sugeridas:

Agrega estilos en línea o eventos al botón:

```jsx
<button onClick={() => alert("¡Click!")}>{texto}</button>
```

📌 Ejemplo de uso:

```jsx
<BotonPersonalizado texto="Enviar" />
<BotonPersonalizado texto="Cancelar" />
```

---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 
