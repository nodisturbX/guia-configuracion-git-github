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

4. **Esquema Visual del Flujo de Trabajo en GitHub**
 
Para entender cómo se conectan los conceptos que acabamos de revisar, observa la siguiente infografía del flujo de trabajo:

![Diagrama explicativo del flujo de trabajo en GitHub que muestra el Repositorio central, la rama principal main con sus commits C1, C2 y C3, una rama secundaria feature branch con C4 y C5, y un Pull Request](assets/github-workflow.jpg)

### 🔍 Descripción detallada del diagrama:

1. **Repositorio (The Project Hub):** Es la nube central (el contenedor general) que almacena todo el código, los archivos y el historial completo del proyecto[cite: 5].
2. **Main (La línea de producción principal):** Representada por la línea azul horizontal. Es la versión estable y oficial del proyecto donde se van acumulando los commits validados en orden cronológico (C1, C2, C3...)[cite: 5].
3. **Branch (La ruta de desarrollo secundaria):** Representada por la línea naranja inferior (`feature/new-design`). Permite sacar una copia temporal de la línea principal para experimentar, desarrollar nuevas funciones (commits C4 y C5) sin afectar el proyecto estable[cite: 5].
4. **Commit (Punto en el tiempo):** Cada uno de los círculos numerados (`C1`, `C4`, etc.) actúa como una "fotografía" o registro histórico que guarda qué usuario hizo el cambio y qué mensaje dejó (por ejemplo, "Added UI elements")[cite: 5].


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

2. **Preparar los cambios:**
   ```powershell
   git add .

3. **Guardar la fotografía (commit) con un mensaje descriptivo**
   ```powershell
   git commit -m "explica que cambio"

4. **Sincronizar con GitHub (push)**
   ```powershell
   git push origin main

