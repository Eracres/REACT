# 📋 Ejercicio 3: Publica en GitHub Pages (avanzado)

## 🎯 Objetivo:
Usar GitHub Pages para publicar tu app React.

## 📝 Instrucciones:
1. Instala el paquete: `npm install gh-pages --save-dev`.
2. Agrega los scripts `predeploy` y `deploy` a `package.json`:
```json
"homepage": "https://tuusuario.github.io/tu-repo",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```
3. Ejecuta `npm run deploy`.
4. Verifica que tu app está disponible en la URL especificada.
---

## [⬅️](../Ejercicios/Ejercicio_2.md) Ejercicio 2
## [📄 Modulo 18](../Modulo_18.md)
## [🏠 Inicio](../../README.md)
