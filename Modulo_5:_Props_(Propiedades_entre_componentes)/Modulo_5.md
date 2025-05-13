# 📘 Módulo 5: Props (Propiedades entre componentes)

## ❓ ¿Qué son las Props?

Las **props** (abreviatura de “properties”) son la forma en que React permite **pasar datos de un componente padre a un componente hijo**.  
Funcionan de forma muy similar a los **parámetros de una función**.

Las props hacen que los componentes sean:

- ✅ Reutilizables
- ✅ Personalizables
- ✅ Más limpios y fáciles de mantener

---

## 🧩 ¿Cómo funcionan?

Cuando usas un componente como una etiqueta HTML, puedes pasarle datos así:

```jsx
<Bienvenida nombre="Carlos" />
```

Y luego acceder a ese dato dentro del componente:

```jsx
function Bienvenida(props) {
  return <h3>Hola, {props.nombre}</h3>;
}
```

---

## 🔁 Reutilización con props

```jsx
<Bienvenida nombre="Ana" />
<Bienvenida nombre="Luis" />
<Bienvenida nombre="Sofía" />
```

Los tres mostrarán un mensaje personalizado gracias al valor de `props.nombre`.

---

## ⚠️ Importante

- ❗ Las props son **de solo lectura**. No puedes modificarlas dentro del componente hijo.
- ✔️ Puedes pasar:
  - Strings
  - Números
  - Booleanos
  - Objetos
  - Funciones
  - Incluso otros componentes como children

---

# 🧪 Ejemplo 1: Mostrar datos de usuario

Este componente muestra los datos recibidos a través de props y construye una tarjeta personalizada.

```jsx
function Usuario(props) {
  return (
    <div>
      <h2>{props.nombre}</h2>
      <p>Edad: {props.edad}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Recibe `nombre` y `edad` como props.
* Los muestra usando JSX e interpolación (`{}`).
* Es reutilizable para múltiples usuarios.

📌 Ejemplo de uso:

```jsx
<Usuario nombre="María" edad={29} />
<Usuario nombre="Lucas" edad={35} />
```

---

# 🧪 Ejemplo 2: Desestructuración de props

Puedes desestructurar directamente en los parámetros:

```jsx
function Usuario({ nombre, edad }) {
  return (
    <div>
      <h2>{nombre}</h2>
      <p>Edad: {edad}</p>
    </div>
  );
}
```

Esto hace el código más limpio y legible.

---

# 🧠 Bonus: props.children

Todos los componentes tienen acceso especial a `props.children`, que representa cualquier contenido que coloques **entre las etiquetas del componente**:

```jsx
function Contenedor({ children }) {
  return <div className="box">{children}</div>;
}

// Uso:
<Contenedor>
  <p>Hola desde dentro del contenedor</p>
</Contenedor>
```

---

# 🎯 Ejercicio para ti

1. Crea un componente llamado `Producto`.
2. Recibirá por props: `nombre`, `precio` y `disponible`.
3. Mostrará la información dentro de un `<div>` con un `<h3>` y dos párrafos.
4. Si `disponible` es `true`, muestra “Disponible ✅”.
   Si no, muestra “Agotado ❌”.
5. Usa el componente al menos 2 veces con datos diferentes dentro de `App.js`.

---

# 💡 Ejercicio extra opcional:

Crea un componente `BotonAccion` que:

1. Reciba como prop un texto para el botón (`texto`)
2. Reciba una función como prop (`onClick`)
3. Al hacer clic, se ejecute esa función

```jsx
<BotonAccion texto="Borrar" onClick={() => alert("Elemento eliminado")} />
```

## 🧪 Ejemplos básicos:

* [📝Ejemplo 1](./Ejemplos/Ejemplo_1.md)
* [📝Ejemplo 2](./Ejemplos/Ejemplo_2.md)
* [📝Ejemplo 3](./Ejemplos/Ejemplo_3.md)
* [📝Ejemplo 4](./Ejemplos/Ejemplo_4.md)
* [📝Ejemplo 5](./Ejemplos/Ejemplo_5.md)
* [📝Ejemplo 6](./Ejemplos/Ejemplo_6.md)

## 🎯 Ejercicios para ti:

* [📋Ejercicio 1](./Ejercicios/Ejercicio_1.md)
* [📋Ejercicio 2](./Ejercicios/Ejercicio_2.md)
* [📋Ejercicio 3](./Ejercicios/Ejercicio_3.md)
* [📋Ejercicio 4](./Ejercicios/Ejercicio_4.md)

---

## [⬅️](../Modulo_3:_JSX_Sintaxis_especial_de_React/Modulo_3.md) Módulo 3 ... Módulo 5 [➡️](../Modulo_5:_Props_(Propiedades_entre_componentes)/Modulo_5.md)

## [🏠 Inicio](../README.md)
