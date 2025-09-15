# Guía de Instalación del Entorno ESP-IDF SDK en Visual Studio Code
Guía para la instalación de ESP-IDF-SDK con extensión de visual studio.

---

## Requisitos Previos

- Tener instalado **Visual Studio Code**: [Descargar VSCode](https://code.visualstudio.com/)
- Acceso a internet
- Sistema operativo: Windows, macOS o Linux

---

## 1. Instala Python

El ESP-IDF requiere Python.  
- Descarga la versión recomendada (normalmente Python 3.8 o superior): [Descargar Python](https://www.python.org/downloads/)

Asegúrate de marcar la opción **"Add Python to PATH"** durante la instalación.

---

## 2. Instala Git

Vas a necesitar Git para clonar repositorios y gestionar el código.  
- Descárgalo aquí: [Descargar Git](https://git-scm.com/downloads)

---

## 3. Instala la Extensión ESP-IDF en VSCode

1. Abre VSCode.
2. Ve al menú de extensiones (ícono de cuadrito a la izquierda).
3. Busca **"ESP-IDF"**.
4. Haz clic en **"Install"** para instalar la extensión oficial de Espressif.

---

## 4. Instala las Dependencias del ESP-IDF

1. Abre el **Command Palette** en VSCode (`Ctrl+Shift+P`).
2. Escribe **"ESP-IDF: Configure ESP-IDF extension"** y selecciónalo.
3. El asistente te guiará para instalar:
   - ESP-IDF tools (Python, CMake, Ninja, etc.)
   - El SDK de ESP-IDF
   - Añadir variables de entorno

Sigue los pasos recomendados.  
**Tip:** Si tienes problemas, revisa que tu antivirus o conexión a internet (experiencia propia) no bloquee la descarga de herramientas.

---

## 5. Clona un Proyecto de Ejemplo

1. Abre una terminal en VSCode (`Ctrl+``).
2. Ejecuta el siguiente comando (puedes cambiar la ruta si lo necesitas):

   ```
   git clone https://github.com/espressif/esp-idf-template.git
   ```

3. Abre la carpeta clonada en VSCode.

---

## 6. Compila y Flashea tu Primer Proyecto

1. Conecta tu placa ESP a la computadora.
2. En la barra lateral de ESP-IDF, selecciona **"Build, Flash and Monitor"**.
3. Sigue las instrucciones para compilar y cargar el firmware en tu placa.

---

## Recursos Útiles

- [Video guía (YouTube)](https://youtu.be/_1bD-lBdPyI?list=PL-Hb9zZP9qC65SpXHnTAO0-qV6x5JxCMJ)
- [Documentación oficial de ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/latest/)

---

## Solución de Problemas

- Si la extensión no detecta Python o Git, revisa que estén en el PATH del sistema.
- Revisa la consola de VSCode para mensajes de error durante la instalación.
- Consulta el foro de Espressif si tienes problemas con drivers o hardware.
