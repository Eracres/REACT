# 📘 Módulo 4: Componentes (Funcionales y de Clase)

## ❓ ¿Qué es un componente en React?

Un componente es una pieza reutilizable de la interfaz de usuario. En React, todo se basa en componentes. Puedes pensar en ellos como bloques de LEGO que se combinan para construir toda tu aplicación.

Cada componente:

* Encapsula su propia lógica y vista.
* Se puede reutilizar múltiples veces.
* Puede recibir datos mediante props y manejar su propio estado.

## 🧱 Tipos de componentes

1. Componentes funcionales (los más comunes actualmente)

Son funciones de JavaScript que devuelven JSX. Se utilizan junto con [hooks](#modulo-6-estado-con-usestate) (useState, useEffect, etc).

```jsx
function Tarjeta() {
  return <p>Componente funcional</p>;
}
```

2. Componentes de clase (en desuso, pero útiles de conocer)
   
Son clases que extienden ```React.Component``` y tienen un método ```render()```.

```import React, { Component } from 'react'```;

```jsx
class TarjetaClase extends React.Component {
  render() {
    return <p>Componente de clase</p>;
  }
}
```

Hoy en día se recomienda usar componentes funcionales con [hooks](#modulo-6-estado-con-usestate) porque son más sencillos y modernos.

## 📢 Convenciones

* Los componentes deben tener su nombre en mayúscula inicial (ej: Saludo, no saludo).
* Un archivo por componente es una buena práctica (por ejemplo, Saludo.js).
* Siempre deben retornar un solo elemento padre (por eso usamos  o React fragments).

## 🧪 Ejemplo básico:

```jsx
function Tarjeta() {
 return (
	### React es genial 😎 Este es un componente funcional
 );
}
```

Este componente puede usarse dentro de otro componente como si fuera una etiqueta HTML

## 🎯 Ejercicio para ti:

1. Crea un componente llamado PerfilUsuario.
2. Dentro de él, muestra lo siguiente:
* Un título ##  con el texto “Perfil del usuario”.
* Un párrafo  con el nombre ficticio de un usuario.
* Importa y usa el componente dentro de App.js.
