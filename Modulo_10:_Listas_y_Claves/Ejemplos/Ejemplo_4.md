# 🧪 Ejemplo 4: CSS Modules

```jsx
import styles from "./Caja.module.css";

function CajaEstilizada() {
  return (
    <div className={styles.caja}>
      Caja estilizada con CSS Modules
    </div>
  );
}
```

✅ ¿Qué hace este componente?

* Usa un estilo encapsulado que no afecta a otros componentes.

🧠 ¿Qué conceptos aplica?

* Importación con `import styles from`.
* Aplicación de clase desde módulo.

📌 Ejemplo de uso:

```jsx
<CajaEstilizada />
```

💡 Variaciones sugeridas:

* Usar múltiples clases del módulo con `join`.
---

## [⬅️](../Ejemplos/Ejemplo_3.md) Ejemplo 3 - Ejemplo 5 [➡️](../Ejemplos/Ejemplo_5.md) 
## [📄 Modulo 9](../Modulo_9.md)
## [🏠 Inicio](../../README.md)

