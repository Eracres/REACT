# 📋 Ejercicio 2: Tarjeta de producto

## 🎯 Objetivo:
Practicar el uso de props para crear componentes reutilizables que muestren datos dinámicos y condicionados.

Este ejercicio te permitirá crear tarjetas de producto que cambien su contenido en función de las props recibidas, utilizando condicionales y estructura JSX.

## 📝 Instrucciones:
1. Crea un componente llamado `TarjetaProducto`.
2. Este componente debe recibir por props:
   - `nombre`
   - `precio`
   - `disponible` (booleano)
3. Muestra esta información en un `<div>` que contenga:
   - Un `<h3>` con el nombre del producto.
   - Un `<p>` con el precio.
   - Un `<p>` que diga:
     - “Disponible ✅” si `disponible` es `true`.
     - “No disponible ❌” si `disponible` es `false`.
4. Usa el componente al menos dos veces dentro de `App.js` con productos distintos.

## 💡 Ejemplo de uso:

```jsx
<TarjetaProducto nombre="Auriculares" precio={29.99} disponible={true} />
<TarjetaProducto nombre="Teclado" precio={49.99} disponible={false} />
```

---

##  [⬅️](../Ejercicios/Ejercicio_1.md) Ejercicio 1 - Ejercicio 3 [➡️](./Ejercicio_3.md)

## [📄 Modulo 4](../Modulo_4.md) 

## [🏠 Inicio](../../README.md) 
