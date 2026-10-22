# 📱 DevTest (SamSpec) — v1.0.0

![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=flat&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![One UI](https://img.shields.io/badge/Design-One%20UI%20%2F%20Material%203-0C4DA2?style=flat&logo=samsung&logoColor=white)
![Minimum SDK](https://img.shields.io/badge/Min%20SDK-26%20(Android%208.0)-brightgreen)

> **DevTest** (anteriormente conocido como *SamSpec*) es una herramienta nativa de diagnóstico avanzado para Android desarrollada específicamente para extraer, analizar y visualizar métricas internas de dispositivos Samsung Galaxy bajo entornos **One UI**.

---

## 🌟 Características de la Versión 1.0.0

Esta primera release incluye una interfaz de usuario completamente renovada basada en **Material Design 3** y adaptada al diseño corporativo de One UI, distribuida en **5 secciones principales**:

### 1. 🏠 Inicio (Resumen General)
* Resumen rápido del estado general del dispositivo.
* Acceso a métricas clave del sistema de un solo vistazo.

### 2. 📱 Sistema y Modelo
* **Datos del Dispositivo:** Lectura de fabricante, marca, modelo exacto (`SM-A505G`, etc.), placa base (`Board`) y procesador (`SoC` Exynos / Snapdragon).
* **Software e Interfaz:** Detección de versión de Android, nivel de API, versión específica de la capa de personalización (**One UI**) y parche de seguridad instalado.

### 3. 🌐 Red y CSC (Carrier Sales Code)
* **Información de Operador:** Lectura de tarjeta SIM, código de país (MCC) y código de red móvil (MNC).
* **Identificadores Únicos:** Lectura defensiva de ICCID y estado de la red celular.
* **Base de Datos CSC:** Identificación detallada de los códigos CSC regionales de Samsung (LatAm, EE. UU., Canadá y variantes globales).

### 4. ⚙️ Hardware, Memoria y Batería
* **Especificaciones del Panel:** Resolución de pantalla, densidad de píxeles y métricas de refresco.
* **Diagnóstico de Batería:** Estado de salud del módulo de batería, nivel de carga actual, voltaje y tecnología.
* **Memoria y Almacenamiento:** Análisis del espacio de almacenamiento interno disponible/total y uso de memoria RAM en tiempo real.

### 5. 🛠️ Ajustes y Acerca de
* Panel de configuración de la app e información de versión de compilación.
* Enlaces a la Política de Privacidad y créditos del desarrollador.

---

## 🛠️ Stack Tecnológico y Arquitectura

* **Lenguaje Principal:** Kotlin 100% nativo.
* **UI Framework:** Material Components & Jetpack Compose / XML Layouts optimizados con Material 3.
* **Patrón de Diseño:** Arquitectura modular optimizada para lectura de propiedades del sistema de bajo nivel (`android.os.Build`, `SystemProperties`).
* **Soporte de Compatibilidad:** Diseñado para ejecutarse sin fallos desde Android 8.0 (Oreo / API 26) hasta versiones modernas de Android (API 34+).

---

## 📂 Estructura del Repositorio

```text
DevTest-Android/
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── java/com/.../     # Lógica en Kotlin (Pestañas, CSC Data, System Inspection)
│   │       ├── res/              # Componentes de diseño, iconos de Material 3 y layouts
│   │       └── AndroidManifest.xml
│   └── build.gradle              # Configuración de dependencias y versiones de SDK
├── .gitignore                    # Reglas para excluir archivos locales y firmas de producción (.jks)
├── LICENSE                       # Licencia de código abierto MIT
└── README.md                     # Documentación oficial del proyecto

