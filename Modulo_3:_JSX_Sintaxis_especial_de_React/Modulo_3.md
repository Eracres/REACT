## 📘 Módulo 3: JSX – Sintaxis especial de React

### ❓ ¿Qué es JSX?

JSX (JavaScript XML) es una extensión de sintaxis para JavaScript que nos permite escribir código muy similar a HTML dentro de archivos JavaScript.

En lugar de separar la lógica y la interfaz como en otros frameworks, React propone una mezcla controlada: combinamos lógica y estructura de forma declarativa usando JSX.

### 🔎 ¿Por qué es útil JSX?

- Nos permite ver visualmente la estructura del componente.
- Es más legible y cercano al HTML tradicional.
- Aumenta la productividad al unir lógica y presentación en un solo lugar.

### 🚨 Importante:

JSX no es HTML real, aunque lo parezca. Por ejemplo:

* En lugar de class, se usa className.
* Todos los elementos deben cerrarse correctamente (por ejemplo: ![]()).
* Los atributos siguen la convención camelCase (onClick, tabIndex, etc).

### 📌 Diferencias entre HTML y JSX

| En HTML        | En JSX                             |
|---------------|------------------------------------|
| ```class```     | ```className```       |
| ```for```    | ```htmlFor``` |
| ```onclick```    | ```onClick```      |
| Atributos vacíos | Se escriben como booleanos: ```disabled={true}``` |
| Etiquetas deben cerrarse | ```img```, ```input```, etc. se cierran como ```<img />``` |

### 💡 Recordatorio: JSX es solo sintaxis

Dentro del JSX puedes usar JavaScript puro entre llaves {}:

```jsx
const usuario = "Lucía";
return <h2>Bienvenida, {usuario}</h2>;
```

### 🧪 Ejemplos básicos:

#### 📄 Ejemplo 1: básico

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

### 🎯 Ejercicios para ti:

🧩 Ejercicio 1:
Crea un componente llamado BienvenidaJSX que:
* Declare una variable usuario = "María".
* Devuelva un div con un saludo: "Hola, María. Bienvenida a React" (usando interpolación con {}).

🧩 Ejercicio 2:
Crea un componente SumaJSX que:
* Declare dos variables a = 5, b = 7
* Muestra un párrafo que diga:
"El resultado de 5 + 7 es: 12"
(usando la suma dentro del JSX con {a + b})

🧩 Ejercicio 3:
Crea un componente TarjetaUsuario que:
* Declare un objeto usuario = { nombre: "Ana", edad: 25 }
* Devuelva un div con un título y un párrafo mostrando:
	* Nombre del usuario
	* Edad del usuario
* Usa estilos en línea para darle color al texto

🧩 Ejercicio 4 (Bonus):
Crea un componente ComponenteCondicional que:
* Reciba una prop llamada admin
* Si admin es true, muestra: "Tienes acceso total"
* Si false, muestra: "Acceso limitado"
* Usa un operador ternario dentro del JSX
