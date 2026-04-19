# Portafolio de Desarrollo Móvil 

*[Read this in English](README.md)*

Bienvenido a mi catálogo de proyectos destacados. Este repositorio centraliza mis desarrollos más significativos construidos con **Flutter** y **Dart**. Cada aplicación resuelve problemas específicos en distintos sectores: simulación de impacto social, gestión inmobiliaria corporativa y tecnología educativa (EdTech).

---

## 1. UNLUCKY: Un Simulador de Vida Probabilistico.

<img src="assets/unlucky/game_screen.png" width="300" align="right" alt="Vista previa de UNLUCKY">

**UNLUCKY** es una simulación de vida basada en narrativa y estadística. En lugar de un juego de acción tradicional, utiliza una interfaz estilo terminal para simular la "lotería del nacimiento". Cada decisión es ponderada por las circunstancias socioeconómicas y el país asignado al azar, utilizando datos reales para calcular probabilidades y riesgos.

### Tecnologías
* **Gestión de Estado:** Riverpod (enfocado en inmutabilidad absoluta).
* **Arquitectura:** Diseño modular "Feature-first".
* **Lógica Core:** Motor de probabilidad personalizado para cálculos de vectores de riesgo.
* **Localización (i18n):** Internacionalización nativa de Flutter mediante archivos .arb.

<details>
<summary><b>Puntos Técnicos y Arquitectura</b></summary>

* **Inmutabilidad:** Cada cambio de estado en una partida genera una nueva instancia inmutable, garantizando actualizaciones de UI predecibles.
* **Estrategia de UI:** Uso del sistema de widgets nativo de Flutter en lugar de un motor de juegos para mantener un control total sobre la tipografía y layouts complejos.
* **Lógica Determinista:** Sistema `StatDelta` que ajusta las tasas de éxito en tiempo real según el perfil inicial del jugador.
* **Internacionalización Nativa:** Separación total de los textos y la lógica del juego utilizando Application Resource Bundles (.arb), permitiendo el cambio de idioma en tiempo real sin recargar el estado.
</details>

<br clear="all">

**Nota:** Repositorio privado por fines comerciales.
**[Ver Demo en Video](https://youtu.be/0V-P1RplIvc)**

---

## 2. Mex Bridge: Gestión Inmobiliaria

<img src="assets/mex_bridge/main_screen.png" width="500" align="right" alt="Vista previa de Mex Bridge">

**Mex Bridge** es una aplicación corporativa para iPad diseñada para centralizar la gestión de expedientes inmobiliarios en México. Funciona como un centro de control para coordinar equipos de Legal, Remodelación y Ventas, asignando tareas y monitoreando el estatus de las propiedades en tiempo real.

### Tecnologías
* **Framework:** Flutter (Optimizado para iPadOS).
* **Base de Datos:** Cloud Firestore (Sincronización reactiva en tiempo real).
* **Gestión de Estado:** Provider.
* **Autenticación:** Firebase Auth con persistencia de sesión.

<details>
<summary><b>Análisis Técnico y Decisiones de Ingeniería</b></summary>

Debido a que este es un proyecto empresarial propietario, el código fuente no es público. Sin embargo, el desarrollo involucró varios patrones de ingeniería avanzada:

* **Control de Acceso Basado en Roles (RBAC):** Construí una capa de seguridad personalizada donde los niveles de acceso se definen mediante tokens por área. Esto garantiza que, aunque la base de datos es centralizada, la interfaz solo renderiza los módulos pertinentes (Legal, Ventas, etc.) y restringe permisos de escritura según el rol.
* **Orquestación de Estado en Formularios Complejos:** Los expedientes inmobiliarios manejan cientos de puntos de datos. Implementé una estrategia de gestión de estado multi-paso con **Provider** para asegurar la persistencia de datos entre pantallas, permitiendo navegar por formularios extensos sin pérdida de información antes de la sincronización final con Firestore.
* **Estrategia de Datos Relacionales en NoSQL:** Diseñé un esquema no relacional en **Cloud Firestore** que optimiza las consultas para el seguimiento del estatus de la propiedad. Utilicé sub-colecciones para "Tareas" para mantener un vínculo limpio entre el expediente maestro y las actualizaciones de cada departamento.
* **Arquitectura Limpia y Patrón Repository:** El proyecto sigue una estructura modular que desacopla la interfaz de la lógica de negocio. Esto facilita el mantenimiento y permite la escalabilidad del sistema a largo plazo.
</details>

<br clear="all">

**Nota:** Código propietario bajo acuerdo de confidencialidad (NDA).

---

## 3. Intelliafy: EdTech & Reclutamiento

<img src="assets/intelliafy/list_test.png" width="300" align="right" alt="Vista previa de Intelliafy">

**Intelliafy** es una plataforma moderna diseñada para instituciones y reclutadores. Permite la creación dinámica de exámenes de opción múltiple, asignación de fechas límite y ofrece un panel interactivo para que los candidatos resuelvan pruebas y reciban retroalimentación instantánea.

### Tecnologías
* **Backend:** Firebase (Auth, Firestore, Cloud Storage).
* **Gestión de Estado:** Provider.
* **Funcionalidades:** Procesamiento de imágenes (`image_picker` y `image_cropper`).
* **Optimización:** Patrón Barrel personalizado para exportaciones limpias.

<details>
<summary><b>Puntos Técnicos y Arquitectura</b></summary>

* **Sincronización Real-Time:** Motor basado en Firestore que garantiza que puntajes y estados se actualicen al instante en todos los dispositivos.
* **Gestión de Assets:** Integración con Firebase Storage para fotos de perfil y multimedia de exámenes con recorte local.
* **UI Modular:** Encabezados curvos y barras de navegación flotantes construidos como componentes reutilizables.
</details>

<br clear="all">

**[Ver Código Fuente](https://github.com/EdgarLopezMX/Intelliafy)**

---

## Habilidades Core

* **Lenguajes:** Dart, C#.
* **Frameworks:** Flutter (Móvil, Tablet, Escritorio).
* **Backend:** Firebase (Auth, Firestore, Functions, Storage).
* **Herramientas:** Git, GitHub, VS Code, Xcode.

---
*Desarrollado en Puebla, México por Edgar Ismael López Rosas.*