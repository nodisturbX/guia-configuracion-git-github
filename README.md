# Guía de Configuración: Git y GitHub para Windows (x64)

Bienvenido a esta guía práctica diseñada para estudiantes y profesionales que buscan dominar el control de versiones desde cero utilizando PowerShell en Windows.

---

## 🛠️ Módulo 1: Instalación y Configuración Inicial

Antes de empezar a escribir código o gestionar proyectos, debemos configurar tu identidad en el equipo.

1. **Instalar Git para Windows:**
   * Descarga e instala [Git for Windows](https://git-scm.com/download/win). Deja las opciones predeterminadas recomendadas.
   * Verifica la instalación abriendo PowerShell y ejecutando:
     ```powershell
     git --version
     ```

2. **Configurar tu Identidad Global:**
   * Configura tu nombre de usuario (o apodo de GitHub) y tu correo electrónico ejecutando estos comandos en PowerShell:
     ```powershell
     git config --global user.name "nombreusuario"
     git config --global user.email "tu-correo@ejemplo.com"
     ```

3. **Definir la Rama Principal:**
   * Asegúrate de que tus nuevos repositorios usen `main` por defecto:
     ```powershell
     git config --global init.defaultBranch main
     ```

---

## 🚀 Módulo 2: Conexión con GitHub y Clonación

1. **Crear el Repositorio en GitHub:**
   * En tu cuenta de GitHub, crea un nuevo repositorio público o privado (puedes marcar la opción de inicializar con un archivo `README.md`).

2. **Clonar el Repositorio Localmente:**
   * Copia la URL HTTPS de tu repositorio y ejecútalo en PowerShell en tu carpeta de proyectos:
     ```powershell
     git clone [https://github.com/nombreusuario/guia-configuracion-git-github.git](https://github.com/nombreusuario/guia-configuracion-git-github.git)
     ```

---

## 💻 Módulo 3: El Ciclo Diario (Los 4 Comandos Esenciales)

Cada vez que realices cambios en tus archivos y quieras respaldarlos en la nube, utiliza este flujo en PowerShell:

1. **Verificar el estado:**
   ```powershell
   git status
