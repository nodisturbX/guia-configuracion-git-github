# Guía de Configuración: Git y GitHub para Windows (x64)

Bienvenido a esta guía práctica diseñada para estudiantes y profesionales que buscan dominar el control de versiones desde cero utilizando PowerShell en Windows.

---

## 🧐 Conceptos Clave (Explicados sin rodeos)

Antes de tirar comandos, entendamos las 4 piezas del rompecabezas:

1. **¿Qué es un Repositorio (`repository`)?**
   Es la carpeta de tu proyecto (por ejemplo, tus scripts o guías) que ahora tiene superpoderes. No solo guarda archivos, sino que **registra toda su historia de cambios**.

2. **¿Qué es un Commit (La Fotografía)?**
   Cada vez que terminas algo que funciona y quieres guardarlo en la historia, haces un `commit`. Es como hacer una "fotografía" o un punto de control en el tiempo. Si algo se rompe mañana, puedes volver exactamente a esta foto.

3. **¿Qué es una Branch (Una Rama)?**
   Imagina el tronco de un árbol. La rama principal se llama **`main`**. Si quieres experimentar creando un script arriesgado sin romper tu trabajo estable, creas una "rama" secundaria (un camino paralelo), pruebas ahí, y si funciona, lo unes al tronco.

4. **El Flujo Visual del Proceso:**

```text
[ Tu Computadora (Local) ]                   [ La Nube (GitHub) ]
  Archivos en tu PC                            Tu Repositorio Online
        │                                                │
        ├─ 1. Modificas tus archivos                     │
        ├─ 2. `git add .` (Los preparas)                 │
        ├─ 3. `git commit` (Tomas la fotografía)         │
        └─ 4. `git push` ──────────────────────────────> ┘ (Se suben y respaldan)

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
