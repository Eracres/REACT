# 📘 Módulo 3: JSX – Sintaxis especial de React

## ❓ ¿Qué es JSX?

JSX (JavaScript XML) es una extensión de sintaxis para JavaScript que nos permite escribir código muy similar a HTML dentro de archivos JavaScript.

En lugar de separar la lógica y la interfaz como en otros frameworks, React propone una mezcla controlada: combinamos lógica y estructura de forma declarativa usando JSX.

## 🔎 ¿Por qué es útil JSX?

- Nos permite ver visualmente la estructura del componente.
- Es más legible y cercano al HTML tradicional.
- Aumenta la productividad al unir lógica y presentación en un solo lugar.

## 🚨 Importante:

JSX no es HTML real, aunque lo parezca. Por ejemplo:

* En lugar de class, se usa className.
* Todos los elementos deben cerrarse correctamente (por ejemplo: ![]()).
* Los atributos siguen la convención camelCase (onClick, tabIndex, etc).

## 📌 Diferencias entre HTML y JSX

| En HTML        | En JSX                             |
|---------------|------------------------------------|
| ```class```     | ```className```       |
| ```for```    | ```htmlFor``` |
| ```onclick```    | ```onClick```      |
| Atributos vacíos | Se escriben como booleanos: ```disabled={true}``` |
| Etiquetas deben cerrarse | ```img```, ```input```, etc. se cierran como ```<img />``` |

## 💡 Recordatorio: JSX es solo sintaxis

Dentro del JSX puedes usar JavaScript puro entre llaves {}:

```jsx
const usuario = "Lucía";
return <h2>Bienvenida, {usuario}</h2>;
```

## 🧪 Ejemplos básicos:

#### 📄 Ejemplo 2: condicionales y ternarios

```jsx
function Mensaje(props) {
  return (
    <div>
      <h2>{props.logueado ? "Bienvenido" : "Inicia sesión"}</h2>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

Este componente recibe una propiedad llamada logueado (tipo booleano), y en base a su valor muestra uno de dos mensajes:
* Si ```logueado === true``` → muestra ```"Bienvenido"```
* Si ```logueado === false``` → muestra ```"Inicia sesión"```
Esto se logra usando el operador ternario:
```condición ? valor_si_verdadero : valor_si_falso```

💡 ¿Por qué es útil?

En React muchas veces necesitas mostrar diferentes elementos en función del estado, por ejemplo:
* Un usuario logueado vs. uno anónimo
* Un carrito lleno vs. uno vacío
* Un botón activado vs. desactivado
Esto lo puedes resolver elegantemente con ternarios dentro del JSX.

#### 📄 Ejemplo 3: aplicar estilos

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

#### 📄 Ejemplo 4: fragmentos y múltiples elementos

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

## 🧪 Ejemplos básicos:

* [📝Ejemplo 1](./Ejemplos/Ejemplo_1.md)
* [📝Ejemplo 2](./Ejemplos/Ejemplo_2.md)
* [📝Ejemplo 3](./Ejemplos/Ejemplo_3.md)
* [📝Ejemplo 4](./Ejemplos/Ejemplo_4.md)


## 🎯 Ejercicios para ti:

* [📋Ejercicio 1](./Ejercicios/Ejercicio_1.md)
* [📋Ejercicio 2](./Ejercicios/Ejercicio_2.md)
* [📋Ejercicio 3](./Ejercicios/Ejercicio_3.md)
* [📋Ejercicio 4](./Ejercicios/Ejercicio_4.md)

---

## [⬅️](../Modulo_2:_Configuración_del_entorno_de_desarrollo/Modulo_2.md) Módulo 2 ... Módulo 4 [➡️](../Modulo_4:_Componentes_(Funcionales_y_de_Clase)/Modulo_4.md)

## [🏠 Inicio](../README.md)
