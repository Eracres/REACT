# 📘 Módulo 11: Formularios en React

## ❓ ¿Qué es un formulario controlado?

Un formulario controlado en React es aquel donde los campos (`<input>`, `<textarea>`, `<select>`) están **vinculados al estado** del componente mediante `useState`.

Esto significa que:
- El valor visible en el input depende del estado.
- Cada cambio en el input actualiza el estado.
- React tiene el control total del valor en todo momento.

---

## 🔄 ¿Por qué usar formularios controlados?

- ✅ Permite validar en tiempo real mientras el usuario escribe.
- ✅ Puedes limpiar el formulario fácilmente después de enviarlo.
- ✅ Facilita la integración con APIs (enviar datos, guardar en base de datos...).
- ✅ Mejora la trazabilidad y control del flujo de datos.

---

## 🧠 Estructura de un formulario controlado

```jsx
const [valor, setValor] = useState("");

<input
  value={valor}
  onChange={(e) => setValor(e.target.value)}
/>
```

Cada campo necesita:
- Un estado que controle su valor.
- Un `value={estado}` para mantener el vínculo.
- Un `onChange` para actualizar ese estado.

---

## 📌 Reglas clave para formularios en React

- Usa `useState` para controlar cada campo (o un objeto para varios).
- El atributo `value` debe enlazarse al estado.
- `onChange` actualiza el estado con el valor del campo.
- `onSubmit` controla el envío con `e.preventDefault()`.

---

## 💡 Manejo de múltiples campos

Puedes controlar todos los campos con un único estado tipo objeto:

```jsx
const [formulario, setFormulario] = useState({ nombre: "", email: "" });

const manejarCambio = (e) => {
  setFormulario({ ...formulario, [e.target.name]: e.target.value });
};
```

Esto permite escalar a muchos campos con un solo manejador.

---

## 🔐 Validaciones comunes

- Validar si un campo está vacío antes de enviar.
- Validar formato de email con RegEx.
- Validar longitudes mínimas o caracteres prohibidos.

---

## 🛠️ ¿Cuándo usar formularios controlados?

| Caso                        | ¿Controlado? |
|-----------------------------|--------------|
| Formulario simple           | ✅ Sí        |
| Formularios dinámicos       | ✅ Sí        |
| Alto rendimiento (muy largo)| 🔄 A evaluar |
| Terceros no-React           | ❌ No        |

---

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

## [⬅️](../Modulo_10:_Listas_y_Claves/Modulo_10.md) Módulo 10 ... Módulo 12 [➡️](../Modulo_12:_Lifting_State_Up_y_comunicación_entre_componentes/Modulo_12.md)

## [🏠 Inicio](../README.md)
