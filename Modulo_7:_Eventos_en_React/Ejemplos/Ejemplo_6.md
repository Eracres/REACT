# 🧪 Ejemplo 6: Foco en input (onFocus/onBlur)

Este componente detecta si el input está activo (enfocado) o no.

```jsx
function FocoInput() {
  const [activo, setActivo] = useState(false);

  return (
    <div>
      <input
        onFocus={() => setActivo(true)}
        onBlur={() => setActivo(false)}
        placeholder="Escribe algo"
      />
      <p>Estado: {activo ? "Activo" : "Inactivo"}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Muestra si el input tiene el foco o no.

🧠 ¿Qué conceptos aplica?

* Eventos `onFocus` y `onBlur`.

📌 Ejemplo de uso:

```jsx
<FocoInput />
```

💡 Variaciones sugeridas:

Mostrar un borde de color al enfocar.

---

## [⬅️](../Ejemplos/Ejemplo_5.md) Ejemplo 5 - Ejercicio 1 [➡️](../Ejercicios/Ejercicio_1.md) 
## [📄 Modulo 7](../Modulo_7.md)
## [🏠 Inicio](../../README.md)
