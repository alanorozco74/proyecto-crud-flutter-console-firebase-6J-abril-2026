¡Excelente elección! Integrar Flutter con Firebase es el estándar hoy en día para crear apps escalables. Para que tu entorno quede perfecto, vamos a seguir una ruta lógica: desde preparar tu sistema con Node.js hasta configurar el CLI de Firebase.

---

## 1. Software necesario: Node.js y npm
Para instalar el Firebase CLI (herramienta de línea de comandos) de forma global en Windows, el único requisito fundamental es **Node.js**, el cual incluye automáticamente **npm** (Node Package Manager).

* **Sistema Operativo:** Windows 10 o 11 (64 bits preferiblemente).
* **Instalador:** Archivo `.msi` desde la web oficial.
* **Permisos:** Debes tener permisos de administrador para la instalación global.

---

## 2. Verificar si Node.js y npm están instalados
Antes de descargar nada, comprueba si ya los tienes. Abre tu terminal (**PowerShell** o **CMD**) y escribe:

* Para Node.js: `node -v`
* Para npm: `npm -v`

> **¿Qué versión utilizar?** > Te recomiendo siempre la versión **LTS (Long Term Support)**. A día de hoy, versiones como la **20.x** o superiores son ideales por su estabilidad.

---

## 3. Guía paso a paso para instalar Node.js y npm
Si los comandos anteriores te devolvieron un error de "comando no reconocido", sigue estos pasos:

1.  **Descarga:** Ve a [nodejs.org](https://nodejs.org/) y haz clic en el botón que dice **"LTS"**.
2.  **Ejecución:** Abre el archivo `.msi` descargado.
3.  **Configuración:** * Acepta los términos.
    * **Importante:** En la pantalla "Custom Setup", asegúrate de que la opción **"Add to PATH"** esté seleccionada (viene por defecto).
    * En la ventana de "Tools for Native Modules", puedes marcar la casilla para instalar herramientas de C++ si planeas hacer desarrollo avanzado, aunque para Firebase no es estrictamente obligatorio.
4.  **Finalizar:** Haz clic en *Install* y, al terminar, **reinicia tu terminal** para que reconozca los cambios.

---

## 4. Instalar Firebase CLI de manera global
Una vez que `npm` funciona, instalar las herramientas de Firebase es un solo comando. En tu terminal escribe:

```bash
npm install -g firebase-tools
```
*El parámetro `-g` indica que la instalación es **global**, permitiéndote usar el comando `firebase` en cualquier carpeta de tu PC.*

---

## 5. Cómo usar los comandos de Firebase

### Acceder a Firebase con tu cuenta de Google
Para vincular tu PC con tu consola de Firebase:
1.  En la terminal, escribe:
    ```bash
    firebase login
    ```
2.  Se abrirá automáticamente una ventana en tu navegador.
3.  Selecciona tu cuenta de Google y otorga los permisos necesarios.
4.  Al volver a la terminal, verás un mensaje de éxito: *Success! Logged in as tu-email@gmail.com*.

### Comandos básicos de `firebase-tools`
| Comando | Propósito |
| :--- | :--- |
| `firebase projects:list` | Muestra todos tus proyectos creados en la consola de Firebase. |
| `firebase init` | Inicia la configuración de Firebase en el directorio de tu proyecto. |
| `firebase logout` | Cierra la sesión de tu cuenta en la máquina actual. |

---

## 6. Bonus: Configurar Firebase en Flutter
Para que tu aplicación de Flutter se comunique con Firebase de forma profesional (usando el nuevo flujo de FlutterFire), debes activar el CLI específico de Dart:

1.  **Activa el CLI de FlutterFire:**
    ```bash
    dart pub global activate flutterfire_cli
    ```
2.  **Configura tu App:** Dentro de la carpeta de tu proyecto Flutter, ejecuta:
    ```bash
    flutterfire configure
    ```
    *Este comando te permitirá seleccionar tu proyecto de la lista, elegirá las plataformas (Android, iOS, Web) y creará automáticamente el archivo `firebase_options.dart` en tu carpeta `lib`.*

¿Ya tienes creado el proyecto en la consola web de Firebase o necesitas ayuda para dar ese primer paso allá?
