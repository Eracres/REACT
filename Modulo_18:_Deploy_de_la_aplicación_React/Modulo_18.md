# 📘 Módulo 18: Deploy de la aplicación React

## ❓ ¿Qué es el Deploy?

El "Deploy" es el proceso de publicar tu aplicación web en internet. Esto transforma tu proyecto local en un sitio accesible desde cualquier parte del mundo mediante una URL pública.

---

## 🌐 Plataformas populares para subir tu app React

| Plataforma       | Características principales                                   |
|------------------|--------------------------------------------------------------|
| **Vercel**       | Integración directa con GitHub, muy rápida y gratuita.       |
| **Netlify**      | Fácil de usar, permite funciones como formularios y funciones serverless. |
| **GitHub Pages** | Gratuito, ideal para proyectos simples.                      |
| **Render**       | Soporta backends y despliegue automático.                    |
| **Firebase**     | Excelente para apps móviles y web.                           |

---

## 🚀 Deploy con Vercel – Guía paso a paso

### 1. Subir tu app a GitHub

- Asegúrate de que tu proyecto funcione correctamente.
- Inicializa Git y sube tu código:

```bash
git init
git add .
git commit -m "Deploy inicial"
git remote add origin https://github.com/tuusuario/tu-repo.git
git push -u origin main
```

---

### 2. Crear cuenta en Vercel

- Ve a 👉 [vercel.com](https://vercel.com)
- Inicia sesión con tu cuenta de GitHub.
- Haz clic en **“Add New Project”** y selecciona tu repositorio.
- Acepta la configuración por defecto y pulsa **“Deploy”**.

✅ En unos segundos tendrás tu aplicación pública en una URL como:
```
https://mi-app-react.vercel.app
```

---

## ⚙️ Bonus: Usar `npm run build` con otras plataformas

Si usas `create-react-app`, puedes compilar tu proyecto con:

```bash
npm run build
```

Esto generará una carpeta `build/` con todos los archivos listos para producción.

Puedes usar esta carpeta con:
- **Netlify Drop** (arrastra y suelta en [netlify.com/drop](https://app.netlify.com/drop))
- **GitHub Pages** (requiere configuración con el package `gh-pages`)
- **FTP/SFTP** si usas tu propio servidor

---

## 📦 Recomendación

Para la mayoría de proyectos de React modernos, **Vercel o Netlify** son las opciones más fáciles y rápidas. Ambos ofrecen certificados SSL gratis, CI/CD, rutas limpias y control de dominio.

¡Hora de compartir tu proyecto con el mundo! 🌍

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

##   [⬅️](../Modulo_17:_Introducción_a_Redux/Modulo17.md) Módulo 17 
## [🏠 Inicio](../README.md)


