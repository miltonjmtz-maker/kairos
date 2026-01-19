# Guía para Subir Kairos CRM a GitHub y Publicar en la Red

Este documento detalla los pasos necesarios para subir este proyecto a un repositorio de GitHub y hacerlo accesible para otros usuarios como una aplicación web.

## 1. Requisitos Previos
1. **Instalar Git**: Descárgalo desde [git-scm.com](https://git-scm.com/) e instálalo con las opciones por defecto.
2. **Cuenta de GitHub**: Regístrate en [github.com](https://github.com/).

## 2. Crear el Repositorio en GitHub
1. Entra a [github.com/new](https://github.com/new).
2. **Repository name**: `Kairos-CRM`.
3. **Public**: Asegúrate de que esté seleccionado para que otros puedan verlo.
4. **IMPORTANTE**: No selecciones "Initialize this repository with" (README, gitignore o license).
5. Haz clic en **Create repository**.

## 3. Subir el Proyecto (Línea de Comandos)
Abre una terminal (PowerShell) en esta carpeta y ejecuta los siguientes comandos:

```powershell
# 1. Inicializar el repositorio local
git init

# 2. Agregar todos los archivos del proyecto
git add .

# 3. Guardar los cambios localmente
git commit -m "Initial commit de Kairos CRM"

# 4. Establecer la rama principal
git branch -M main

# 5. Conectar con GitHub (REEMPLAZA TU_USUARIO por tu nombre de usuario de GitHub)
git remote add origin https://github.com/TU_USUARIO/Kairos-CRM.git

# 6. Subir los archivos a la nube
git push -u origin main
```

## 4. Hacerlo Accesible vía Web (GitHub Pages)
Una vez que los archivos estén en GitHub, sigue estos pasos para generar el enlace público:

1. En tu repositorio de GitHub, haz clic en la pestaña **Settings** (Configuración).
2. En el menú de la izquierda, selecciona **Pages**.
3. En la sección **Build and deployment**:
   - Branch: Selecciona `main`.
   - Folder: Selecciona `/(root)`.
4. Haz clic en **Save**.
5. Espera unos minutos y GitHub te mostrará un mensaje arriba: *"Your site is live at..."* con la URL de tu aplicación.

---
**Nota:** El archivo principal del proyecto es `dashboard.html`. Si deseas que se abra automáticamente al entrar a la URL, se recomienda renombrarlo a `index.html`.
