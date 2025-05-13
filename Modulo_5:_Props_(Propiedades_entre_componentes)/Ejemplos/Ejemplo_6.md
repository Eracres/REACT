# 🧪 Ejemplo 6: Título personalizado con estilo

Este componente recibe un título como prop y lo muestra en pantalla con un estilo específico.

```jsx
function TituloSeccion({ texto }) {
  return (
    <h2 style={{ color: "royalblue", fontSize: "1.5rem" }}>
      {texto}
    </h2>
  );
}
```

✅ ¿Qué hace este componente?

* Muestra un título (`<h2>`) con el texto recibido desde la prop `texto`.
* Aplica estilos en línea: color y tamaño de fuente.

🧠 ¿Qué conceptos aplica?

* Props de tipo string para contenido dinámico.
* Estilos en línea (`style={{ ... }}`) usando sintaxis de objetos.
* Componentes presentacionales reutilizables.

📌 Ejemplo de uso:

```jsx
<TituloSeccion texto="Últimas noticias" />
<TituloSeccion texto="Artículos recomendados" />
```

💡 Variaciones sugeridas:

Agrega una prop `color` para personalizar el color desde fuera:

```jsx
function TituloSeccion({ texto, color }) {
  return <h2 style={{ color }}>{texto}</h2>;
}
```

Y úsalo así:

```jsx
<TituloSeccion texto="Favoritos" color="crimson" />
```

---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md)

## [📄 Modulo 5](../Modulo_5.md) 

## [🏠 Inicio](../../README.md) 
