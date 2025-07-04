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

## [⬅️](../Modulo_3:_JSX_Sintaxis_especial_de_React/Modulo_3.md) Módulo 3 ... Módulo 6 [➡️](../Modulo_6:_Estado_con_useState/Modulo_6.md)

## [🏠 Inicio](../README.md)
