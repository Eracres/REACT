# 🧪 Ejemplo 5: Tecla presionada (onKeyDown)

Este componente detecta cuando el usuario presiona una tecla y la muestra en pantalla.

```jsx
function TeclaPresionada() {
  const [tecla, setTecla] = useState("");

  const manejarTecla = (e) => {
    setTecla(e.key);
  };

  return (
    <div>
      <input type="text" onKeyDown={manejarTecla} />
      <p>Tecla presionada: {tecla}</p>
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Muestra la última tecla que el usuario presionó en el input.

🧠 ¿Qué conceptos aplica?

* Evento `onKeyDown`.

📌 Ejemplo de uso:

```jsx
<TeclaPresionada />
```

💡 Variaciones sugeridas:

Detectar combinaciones de teclas para atajos de teclado.

---


## [⬅️](../Ejemplos/Ejemplo_4.md) Ejemplo 4 - Ejemplo 6 [➡️](../Ejemplos/Ejemplo_6.md)

## [📄 Modulo 7](../Modulo_7.md) 

## [🏠 Inicio](../../README.md) 
