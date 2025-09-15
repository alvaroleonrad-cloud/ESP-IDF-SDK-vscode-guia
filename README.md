# Guía de Instalación del Entorno ESP-IDF SDK en Visual Studio Code y Primer Proyecto
Guía para la instalación de ESP-IDF-SDK con extensión de visual studio.

---

## Requisitos Previos

- Tener instalado **Visual Studio Code**: [Descargar VSCode](https://code.visualstudio.com/)
- Acceso a internet
- Sistema operativo: Windows, macOS o Linux

---

### Por qué usar esp idf sdk
_Si ya sabes usar MicroPython y Arduino para programar placas ESP32, cambiarte a **ESP-IDF SDK** te permite hacer cosas mucho más profesionales. ESP-IDF es el entorno oficial de Espressif y está creado para que puedas aprovechar al máximo cada parte del hardware. Aquí no hay "capas de abstracción" que te limiten, ni funciones automáticas que te oculten lo que realmente sucede en el chip._

_**¿Qué es una capa de abstracción?**  
Es como una especie de traductor que hace que trabajar con la placa sea más fácil, pero también te esconde detalles importantes. Por ejemplo, cuando usas Arduino o MicroPython, no ves cómo el chip se comunica directamente con sus componentes; el entorno te lo simplifica, pero también te quita control y opciones. Con ESP-IDF, tú decides exactamente cómo funciona cada parte._

_Al usar ESP-IDF tienes control total sobre la memoria, los periféricos (como puertos, sensores y comunicaciones), puedes optimizar tu programa para que sea más rápido y estable, y puedes crear aplicaciones que funcionen en proyectos grandes o industriales. Por ejemplo, puedes manejar varias tareas al mismo tiempo (esto se llama multitarea, usando FreeRTOS), actualizar el software de tus placas de forma segura y crear productos pensados para vender o usar en empresas._

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

## 5. Compila y Flashea tu Primer Proyecto

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

## Verificación de requerimientos
1. windows + R
2. Escribir 'cmd' y enter
3. Ver las versiones
   * git --version
   * code --version
   * python --version

---

# Crear un Nuevo Proyecto ESP-IDF en Visual Studio Code

Guía paso a paso para crear, configurar y compilar un proyecto ESP-IDF desde cero usando Visual Studio Code.

---

## 1. Abrir la Extensión ESP-IDF en VS Code

- Abre Visual Studio Code.
- Haz clic en el icono de **ESP-IDF** en la barra lateral izquierda.
- Selecciona **"Create ESP-IDF Project"**.

---

## 2. Configurar el Proyecto Nuevo

1. **Nombre del proyecto:**  
   Escribe el nombre para tu nuevo proyecto (por ejemplo, `mi_primer_espidf`).

2. **Selecciona la plantilla:**  
   Puedes elegir entre varias plantillas (ejemplo: `blink`, `hello_world`, `template`).  
   La plantilla `blink` es ideal para empezar (hace parpadear un LED).

3. **Ubicación del proyecto:**  
   Elige la carpeta donde se guardará el proyecto.  
   Recomendación: crea una carpeta específica para tus proyectos ESP-IDF.

4. **Finaliza la creación:**  
   Haz clic en **"Create project using template"**.

---

## 3. Abrir el Proyecto en VS Code

- Si el proyecto no se abre automáticamente, ve a **File > Open Folder...** y selecciona la carpeta del proyecto que acabas de crear.

---

## 4. Configurar la Conexión y la Placa

- Conecta tu placa ESP a la computadora mediante el cable USB.
- Verifica que VS Code detecta el puerto serial (lo verás en la barra inferior o en la configuración de la extensión ESP-IDF).

---

## 5. Compilar el Proyecto

- En la barra lateral de ESP-IDF, haz clic en **"Build, Flash and Monitor"**.
- Espera a que se complete la compilación.
- Si hay errores, revisa en la terminal los mensajes y verifica dependencias.

---

## 6. Flashear y Monitorear

- Una vez compilado, VS Code cargará el programa en tu placa automáticamente.
- Abre el **Monitor Serial** en VS Code para ver la salida (por ejemplo, mensajes de `hello_world` o el estado del LED).

---

## 7. Modificar el Código y Recompilar

- Abre el archivo principal (normalmente `main/main.c` o `main/main.cpp`).
- Haz cambios, por ejemplo, modifica el intervalo de parpadeo del LED.
- Guarda los cambios y repite el proceso de **"Build, Flash and Monitor"**.

---

## Recursos

- [Video guía en YouTube](https://youtu.be/bMyMhIegFts?list=PL-Hb9zZP9qC65SpXHnTAO0-qV6x5JxCMJ)
- [Documentación oficial de ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/latest/)

---

## Consejos y Solución de Problemas

- Si el puerto serial no aparece, verifica drivers USB y permisos.
- Si la compilación falla, revisa que las dependencias estén instaladas y la configuración del entorno.
- Consulta la documentación oficial para detalles avanzados de configuración.

