# 📘 Módulo 2: Configuración del Entorno de Desarrollo

## 🎯 Objetivos
- Configurar entorno profesional con herramientas modernas
- Dominar estructura de proyectos React
- Implementar ESLint + Prettier para código limpio
- Optimizar workflow de desarrollo

## ❓ ¿Cómo empezar con React?

Para desarrollar con React de forma profesional, lo ideal es tener un entorno que nos permita comenzar rápido, sin perder tiempo en configuraciones innecesarias. Para eso existe una herramienta oficial: Create React App.
Create React App es un scaffolding tool que genera un proyecto React completo, listo para empezar, con todo configurado: Babel, Webpack, React y más.

## 🛠️ Cómo crear tu primer proyecto React:

1. Instalar Node.js y npm, para comprobar si estan instalados, usar estos comandos:

 ```bash
node -v
npm -v
``` 

2. Abre tu terminal (en VS Code o donde prefieras).

3. Ejecuta el siguiente comando:
   
```bash
npx create-react-app mi-app
```

4. Entra en el nuevo directorio del proyecto:

```bash
cd mi-app
```

5. Inicia el servidor de desarrollo:

```bash
npm start
```

Esto abrirá automáticamente el navegador en http://localhost:3000 con tu aplicación React funcionando. ¡Ya tienes tu primer entorno ⚛️ montado!

## 🗂️ Estructura básica del proyecto

```
📦 mi-app/
├── 📁 public/          → Assets estáticos
├── 📁 src/
│   ├── 📁 assets/      → Imágenes/fuentes
│   ├── 📁 components/  → Componentes reutilizables
│   ├── 📁 hooks/       → Custom hooks
│   ├── 📁 pages/       → Vistas/páginas
│   ├── 📁 styles/      → Estilos globales
│   ├── 📁 utils/       → Funciones helper
│   ├── 📄 App.jsx      → Componente raíz
│   ├── 📄 index.js     → Punto de entrada que renderiza `App.js`
│   └── 📄 main.jsx     → Entry point
├── 📄 .eslintrc.cjs    → Configuración ESLint
├── 📄 .prettierrc      → Configuración Prettier
├── 📄 vite.config.js   → Configuración Vite
└── 📄 package.json     → Dependencias y scripts del proyecto
```

## 🔧 Configuración Esencial:

**ESLint + Prettier**

1. Instalar dependencias:

```bash
npm install -D eslint eslint-plugin-react eslint-config-prettier prettier
```

2. Archivo ```.eslintrc.cjs```:

```js
module.exports = {
  env: { browser: true, es2021: true },
  extends: [
    "eslint:recommended",
    "plugin:react/recommended",
    "eslint-config-prettier"
  ],
  rules: {
    "react/react-in-jsx-scope": "off"
  }
}
```
   
3. Archivo ```.prettierrc```:

```json
{
  "semi": false,
  "singleQuote": true,
  "jsxSingleQuote": true
}
```

## 🧼 Recomendación como desarrollador:

Al empezar un nuevo proyecto, te recomiendo limpiar el código inicial que trae App.js, App.css, y borrar logo.svg. Así puedes construir tu aplicación desde cero con total control.

## 🧪 Ejemplos básicos:

* [📝Ejemplo 1](./Ejemplos/Ejemplo_1.md)


## 🎯 Ejercicios para ti:

* [📋Ejercicio 1](./Ejercicios/Ejercicio_1.md)

---

## [⬅️](../Módulo_1:_Introducción_a_React/Modulo_1.md) Módulo 1 ... Módulo 3 [➡️](../Modulo_3:_JSX_Sintaxis_especial_de_React/Modulo_3.md)

## [🏠 Inicio](../README.md)
