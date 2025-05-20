  # 🧪 Ejemplo 2: Contador automático

  Este componente aumenta automáticamente un contador cada segundo.

  ```jsx
  import { useEffect, useState } from "react";

  function ContadorAutomatico() {
    const [contador, setContador] = useState(0);

    useEffect(() => {
      const intervalo = setInterval(() => {
        setContador((prev) => prev + 1);
      }, 1000);

      return () => clearInterval(intervalo);
    }, []);

    return <p>Contador automático: {contador}</p>;
  }
  ```

  ✅ ¿Qué hace este componente?

  * Inicia un temporizador que incrementa un número cada segundo.
  * Limpia el intervalo cuando el componente se desmonta.

  🧠 ¿Qué conceptos aplica?

  * `useEffect` con temporizador (`setInterval`).
  * Función de limpieza.

  📌 Ejemplo de uso:

  ```jsx
  <ContadorAutomatico />
  ```

  💡 Variaciones sugeridas:

  Permitir al usuario iniciar/detener el contador con botones.

  ---

  ## [⬅️](../Ejemplos/Ejemplo_1.md) Ejemplo 1 - Ejercicio 3 [➡️](../Ejemplos/Ejemplo_3.md) 
  ## [📄 Modulo 8](../Modulo_8.md)
  ## [🏠 Inicio](../../README.md)

