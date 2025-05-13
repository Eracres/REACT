
# 🧪 Ejemplo 1: Componente funcional básico

Este componente muestra una estructura simple con título y párrafo. Está escrito como una función que devuelve JSX.

```jsx
function Tarjeta() {
  return (
    <div>
      <h3>React es genial 😎</h3>
      <p>Este es un componente funcional</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Define una función `Tarjeta` que retorna una estructura HTML-like con JSX.
* Usa un `div` como elemento padre que contiene un `h3` y un `p`.
* Muestra un título y un texto descriptivo como parte de la interfaz.

🧠 ¿Qué conceptos aplica?

* Componentes funcionales: definidos como funciones estándar de JavaScript.
* JSX: estructura similar a HTML dentro del código JS.
* Reutilización: puede importarse y usarse en otros archivos.

✅ ¿Qué puedes aprender de esto?

* Todo componente debe devolver un solo nodo raíz.
* Es la forma más básica de construir un componente React.

💡 Variaciones sugeridas:

Puedes agregar estilos en línea:

```jsx
<h3 style={{ color: "blue" }}>React es genial 😎</h3>
```

O pasar el título como prop:

```jsx
function Tarjeta({ titulo }) {
  return <h3>{titulo}</h3>;
}
```

---

## Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 



