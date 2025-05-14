# 🧪 Ejemplo 1: básico

Este componente mezcla código JavaScript (```const nombre = "React"```) con etiquetas JSX (parecidas a HTML). Lo que aparece entre llaves {} dentro del JSX es interpretado como una expresión de JavaScript.

```jsx
function ComponenteJSX() {
  const nombre = "React";
  return (
    <div>
      <h1>Hola desde {nombre}</h1>
      <p>¡Esto es JSX funcionando!</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

Este componente muestra un saludo dinámico usando una variable declarada en JavaScript (```const nombre = "React"```).
* Dentro del ```return```, usamos JSX para crear una estructura HTML-like.
* Utiliza ```{nombre}``` para insertar dinámicamente el valor ```"React"``` dentro del texto del ```<h1>```.
* Luego, muestra un ```<p>``` con un mensaje fijo.

🧠 ¿Qué conceptos aplica?

* Interpolación de variables: con ```{}``` dentro de JSX puedes mostrar cualquier expresión de JavaScript.
* Encapsulamiento de UI: este componente podría reutilizarse con diferentes textos.
* Elementos anidados en un contenedor (```<div>```): JSX requiere que todo esté envuelto en un solo elemento padre.

✅ ¿Qué puedes aprender de esto?

* JSX no es HTML, pero se le parece mucho.
* Todo lo que escribas dentro del ```return``` tiene que estar envuelto en un solo nodo raíz.
* Las variables dentro del JSX deben ir entre llaves ```{}```.

💡 Variaciones sugeridas:

Puedes transformar el nombre en mayúsculas directamente:

```jsx
<h1>Hola desde {nombre.toUpperCase()}</h1>
```

O usar props para hacerlo reutilizable:

```jsx
function ComponenteJSX(props) {
  return <h1>Hola desde {props.nombre}</h1>;
}
```
---
## Ejemplo 2 [➡️](../Ejemplos/Ejemplo_2.md)

## [📄 Modulo 3](../Modulo_3.md) 

## [🏠 Inicio](../../README.md) 
