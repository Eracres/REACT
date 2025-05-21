# 📘 Módulo 12: Lifting State Up y comunicación entre componentes

## ❓ ¿Qué es “Lifting State Up”?

En React, cada componente puede tener su propio estado. Pero cuando **dos o más componentes necesitan compartir información**, lo ideal es **elevar el estado al componente padre común**.

Este patrón se conoce como **Lifting State Up** (elevar el estado) y es una práctica recomendada para mantener una lógica compartida clara.

---

## 🔁 ¿Cuándo usar Lifting State Up?

- Cuando un hijo necesita enviar datos al padre.
- Cuando dos componentes hermanos necesitan compartir estado.
- Cuando un componente central coordina la interacción de varios elementos hijos.

---

## 🧩 ¿Cómo se aplica?

1. Crea el estado en el componente padre.
2. Pasa el valor del estado como prop al componente hijo que lo necesita.
3. Pasa también una función modificadora (`setEstado`) si el hijo necesita actualizarlo.
4. Los hijos notifican al padre usando la función que reciben.

---

## 📡 Comunicación descendente y ascendente

| Dirección        | Mecanismo                |
|------------------|--------------------------|
| Padre → Hijo     | A través de `props`      |
| Hijo → Padre     | Usando una función pasada por `props` |

---

## 🧠 Ventajas del Lifting State Up

- Permite centralizar la lógica.
- Favorece el flujo de datos unidireccional.
- Mejora el control y sincronización entre componentes.

---

## ⚖️ Alternativas a Lifting State Up

| Situación                    | Alternativa              |
|------------------------------|--------------------------|
| Estado compartido entre muchos | Context API              |
| Aplicaciones grandes         | Redux, Zustand, etc.     |
| Estado que no cambia         | Props simples             |

---

## 💡 Buenas prácticas

- Eleva el estado **solo cuando sea necesario**.
- Si muchos hijos dependen del estado, considera usar **Context**.
- Mantén los componentes lo más independientes posible.

---

## [⬅️](../Modulo_11:_Formularios_en_React/Modulo_11.md) Módulo 11 ... Módulo 13 [➡️](../Modulo_13:_React_Router_–_Navegación_entre_páginas/Modulo_13.md)

## [🏠 Inicio](../README.md)
