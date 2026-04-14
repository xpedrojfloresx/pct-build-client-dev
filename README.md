# 🚀 Trivia Game - Plaza Cielo Tierra (Modo Developer)

Este repositorio contiene el sistema de trivia interactivo desarrollado para el museo **Plaza Cielo Tierra**. El proyecto está diseñado como una aplicación móvil multiplataforma que utiliza **UI Toolkit** para la interfaz y un backend en **Supabase** para la gestión de datos.

---

## 🛠 Requisitos Previos

Antes de compilar, asegúrate de contar con:

* **Unity Editor**: Versión 2021.3 LTS o superior (requerido para el soporte estable de UI Toolkit y Panel Settings).
* **Módulos de Build**: Soporte para Android/iOS instalado en el Unity Hub.
* **Font Assets**: Asegúrate de tener los archivos SDF de las fuentes en la carpeta `Assets/OG/UI/Fonts/`.

---

## 🔧 Configuración del Entorno

### 1. Integración con Supabase
El sistema registra automáticamente el desempeño de los jugadores en la base de datos.
* Configura las credenciales en el componente `SupabaseService` en la escena.
* Los datos recolectados incluyen: Usuario, Nombre, Apellido, Edad, País y Puntos.

### 2. UI y Estilos Globales (Theme Style Sheet)
Para evitar errores visuales en el despliegue, el proyecto utiliza un sistema de **Theme** global.
* El archivo `SETTING (Panel Settings)` debe tener asignado un **Theme Style Sheet** personalizado para gestionar los estilos de los dropdowns y fuentes dinámicas.
* Verifica que el archivo `.uss` esté vinculado al Theme para que las clases como `.unity-base-dropdown__container-outer` funcionen correctamente.

---

## 📦 Despliegue en Modo Developer

Para realizar una build de prueba con acceso a logs y debugging:

1.  Ve a **File > Build Settings**.
2.  Asegúrate de que la plataforma sea **Android** o **iOS**.
3.  Activa la casilla **Development Build**.
4.  Activa **Script Debugging** para permitir el seguimiento de errores en tiempo real.
5.  Haz clic en **Build and Run**.

---

## 🧪 Pruebas y Debugging

* **Formulario de Datos**: Para probar la validación de campos sin jugar una partida, usa el botón derecho sobre el script `TriviaGameUIController` en el Inspector y selecciona **Debug: Show PanelDatos**.
* **Lógica de Red**: El `QuizGameManager` permite iniciar partidas de prueba con dificultad ajustable (por defecto: `Easy`) y carga de categorías desde la base de datos.
* **Localización**: Puedes alternar entre **Español** e **Inglés** desde el `GameManager`. El sistema actualizará automáticamente etiquetas como "TIME LEFT", "TIEMPO RESTANTE" y el placeholder del selector de nombre.

---

## 📝 Notas Técnicas del Desarrollador

* **Dropdown de Países**: Se incluye una lista predefinida de 28 países. El despliegue de la lista tiene un límite de altura programado (`max-height`) para evitar que cubra toda la pantalla en dispositivos móviles.
* **Gestión de Tareas**: Al reiniciar la UI o cambiar de pantalla, el controlador cancela las tareas programadas (como el `_thanksScreenTask`) para evitar fugas de memoria o llamadas a objetos destruidos.
* **Anclaje de UI**: El dropdown utiliza un cálculo de `worldBound` para posicionarse siempre debajo del campo de selección, independientemente de la resolución del teléfono.

---
*Este proyecto es parte del trabajo final de grado para Colegio Universitario IES 21.*
