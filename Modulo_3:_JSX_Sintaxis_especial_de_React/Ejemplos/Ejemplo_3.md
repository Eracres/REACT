# 🧪 Ejemplo 3: aplicar estilos

```jsx
function Estilizado() {
  const estilo = {
    color: "tomato",
    fontSize: "20px",
    textAlign: "center"
  };

  return <p style={estilo}>¡Este texto tiene estilo JSX!</p>;
}
```
✅ ¿Qué hace este componente?
Este componente:
 1. Declara un objeto ```estilo``` con propiedades CSS (en camelCase)
 2. Usa ese objeto para aplicar estilos en línea al párrafo ```<p>```
El resultado es un texto centrado, en color tomate y con fuente de 20px.

🧠 ¿Qué debes saber sobre estilos en React?
* Los estilos en línea en JSX se pasan como un objeto de JavaScript
* Las propiedades CSS se escriben en camelCase (no ```font-size```, sino ```fontSize```)
* El valor de cada propiedad debe ir entre comillas como string (por ejemplo, ```"tomato"```)

💡 ¿Cuándo usar estilos en línea?
* Para estilos rápidos o condicionales
* Cuando no necesitas un archivo CSS externo
* En componentes muy pequeños o reutilizables

 🧪 Alternativa:
 
Podrías aplicar ese mismo estilo directamente en el elemento así:

```jsx
<p style={{ color: "tomato", fontSize: "20px", textAlign: "center" }}>
  ¡Este texto tiene estilo JSX!
</p>
```
Pero es mejor práctica guardar los estilos en una constante si los vas a reutilizar o si son muchos. 

---


##  [⬅️](../Ejemplos/Ejemplo_2.md) Ejemplo 2 - Ejemplo 4 [➡️](../Ejemplos/Ejemplo_4.md)

## [📄 Modulo 3](../Modulo_3.md) 

## [🏠 Inicio](../../README.md)
