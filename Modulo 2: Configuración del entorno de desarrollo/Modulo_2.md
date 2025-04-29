<a name="modulo-2-configuración-del-entorno-de-desarrollo"></a>
## 📘 Módulo 2: Configuración del Entorno de Desarrollo

### ❓ ¿Cómo empezar con React?

Para desarrollar con React de forma profesional, lo ideal es tener un entorno que nos permita comenzar rápido, sin perder tiempo en configuraciones innecesarias. Para eso existe una herramienta oficial: Create React App.
Create React App es un scaffolding tool que genera un proyecto React completo, listo para empezar, con todo configurado: Babel, Webpack, React y más.

### 🛠️ Cómo crear tu primer proyecto React:

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

### 🗂️ Estructura básica del proyecto

```
📦 mi-app
├── 📁 public               → Contiene el HTML principal (`index.html`)
│   └── 📄 index.html
├── 📁 src                  → Aquí va todo tu código React
│   ├── 📄 App.js           → Componente principal de la aplicación
│   └── 📄 index.js         → Punto de entrada que renderiza `App.js`
└── 📄 package.json         → Dependencias y scripts del proyecto
```

### 🧼 Recomendación como desarrollador:

Al empezar un nuevo proyecto, te recomiendo limpiar el código inicial que trae App.js, App.css, y borrar logo.svg. Así puedes construir tu aplicación desde cero con total control.
