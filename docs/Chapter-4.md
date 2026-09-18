Capítulo IV: Product Design

## 4.1. Style Guidelines.
<a id="4-1-Style-Guidelines"></a>

En esta sección, el equipo sienta las bases para contar con un repositorio central y organizado de uso común para todo el equipo, que incluye assets, fuentes tipográficas, componentes visuales, entre otros. 
Esto con el fin de mantener una presentación consistente y enfocada de la marca EcoRoad a lo largo de todos los puntos de contacto con el usuario, ya sea en campo, en oficina o en los distintos dispositivos desde los que se accede a la plataforma.

### 4.1.1. General Style Guidelines
<a id="4-1-1-General-Style-Guidelines"></a>

Construimos la identidad de EcoRoad bajo directrices visuales de Branding, Typography, Colors y Spacing, así como las dimensiones adoptadas para el tono de comunicación y lenguaje aplicado por la marca.
Estas decisiones se sustentan en el posicionamiento de EcoRoad como una plataforma que transforma el monitoreo ambiental en un flujo de gestión de detección de riesgos, alerta, incidencia, acción correctiva y evidencia, por lo que la identidad visual busca transmitir confiabilidad, precisión técnica y una ingeniería civil preventiva y sostenible.

**Branding:**

El logotipo de EcoRoad sintetiza los pilares conceptuales de la propuesta: naturaleza, infraestructura vial y monitoreo ambiental en tiempo real mediante IoT.

* **Hoja (naturaleza/sostenibilidad)**: Representa el componente ambiental que la plataforma monitorea (aire, ruido, agua, vibraciones) y la orientación hacia una gestión vial más sostenible. 
* **Carretera (infraestructura vial)**: Representa el sector de aplicación del producto, construcción, mantenimiento y rehabilitación de vías, transmite avance, trazabilidad y dirección, en línea con el seguimiento de acciones correctivas hasta el cierre de cada incidencia. 
* **Montañas y sol (contexto geográfico y monitoreo)**: Hacen referencia a los tramos, frentes de trabajo y puntos de monitoreo que la plataforma visualiza mediante dashboards geolocalizados. 
* **Contenedor circular**: Refuerza la idea de un ciclo completo de gestión ambiental (monitoreo -> alerta -> incidencia -> acción correctiva -> evidencia -> cierre), coherente con el enfoque preventivo y no solo descriptivo de la plataforma.

**Typography:**

Siguiendo la construcción geométrica y redondeada del logotipo, se adopta una familia tipográfica sans-serif geométrica como base del sistema, priorizando legibilidad en pantallas de campo (tablets, móviles con luz solar directa) y coherencia con el tono técnico y confiable de la marca.


| Uso                        | Tipografía                     | Aplicación |
|:---------------------------|:-------------------------------| :--- |
| Encabezados                | Poppins Bold / SemiBold        | Títulos de dashboard, nombres de proyecto |
| Subtítulos                 | Poppins Medium                 | Nombres de módulos, tarjetas de indicadores |
| Cuerpo de texto            | Inter Regular                  |  Tablas, formularios, descripciones |
| Datos numéricos / métricas | Inter Medium (tabular figures) |Valores de sensores, timestamps |

**Colors:**

La paleta se deriva directamente de los colores institucionales definidos para EcoRoad, con un rol funcional asignado a cada uno para su uso en interfaz:

| Color         | Hex | Rol funcional en la plataforma                                                                                          |
|:--------------| :--- |:------------------------------------------------------------------------------------------------------------------------|
| Verde         | `#2E9E7A` | Color principal de la marca; estado óptimo / sin riesgo detectado (semáforo verde)                                       |
| Azul petróleo | `#264653` | Color secundario; tipografía principal, fondos de navegación, elementos estructurales                                   |
| Crema         | `#F5F1E8` | Fondo base de la interfaz; transmite neutralidad y bajo cansancio visual en uso prolongado                              |
| Amarillo      | `#E9B44C` | Condición de advertencia (semáforo ámbar) — indicador que se acerca al umbral establecido y puede derivar en una alerta |
| Rojo          | `#C0392B` | Condición crítica (semáforo rojo) — el indicador supera el umbral y el sistema genera una incidencia                    |


**Spacing**

Se define un sistema de espaciado en base 8px (8, 16, 24, 32, 40), compatible con grillas de 12 columnas para web y facilitando la futura adaptación a interfaces móviles. 
El espaciado busca priorizar la lectura rápida de indicadores en campo, evitando el amontonamiento de datos en tableros con múltiples proyectos simultáneos.

**Lenguaje de comunicación**

Dado que los usuarios principales (responsables del monitoreo, gestión y atención de incidencias ambientales dentro de empresas constructoras y de conservación/rehabilitación vial) 
operan bajo presión de tiempo en campo y necesitan actuar con rapidez ante un riesgo, el tono de EcoRoad se posiciona de la siguiente manera:

| Posicionamiento                | Justificación |
|:-------------------------------| :--- |
| Serio                          | La plataforma respalda decisiones sobre riesgos ambientales reales en obra; el lenguaje debe transmitir precisión técnica. |
| Formal, con cercanía funcional | Se usa terminología técnica correcta (umbrales, incidencias, acciones correctivas), con instrucciones claras y directas para uso rápido en campo. |
| Respetuoso                     | El lenguaje describe condiciones y acciones sin atribuir culpas; una incidencia se comunica como un hecho a resolver, no como un señalamiento. |
| Sereno                         | Las alertas y notificaciones comunican el nivel de riesgo con claridad, priorizando que el usuario entienda qué acción tomar sobre la urgencia emocional del mensaje. |


### 4.1.2. Web Style Guidelines
<a id="4-1-2-Web-Style-Guidelines"></a>

En esta sección se explican e ilustran las decisiones sobre los estándares visuales y de interacción para las interfaces web responsive de EcoRoad, 
aplicables al panel de gestión donde una misma empresa constructora o de conservación/rehabilitación vial, administra sus proyectos, sensores IoT, alertas e incidencias.

* **Grid system:** grilla de 12 columnas con márgenes fluidos, breakpoints en 1280px (desktop), 1024px (tablet/laptop) y 768px (tablet vertical), 
priorizando el desktop como plataforma principal para el análisis multi-proyecto y la vista tablet para el registro de evidencias en campo.
* **Componentes de dashboard:** tarjetas de indicador (KPI cards) con codificación semáforo (verde/amarillo/rojo) según la paleta funcional; 
los dashboards geolocalizados usan el azul petróleo como color base del mapa y marcadores en los tres colores de estado para representar tramos, frentes de trabajo y puntos de monitoreo.
* **Navegación:** barra lateral fija en azul petróleo (
#264653) con el isotipo de EcoRoad, manteniendo contraste alto con el fondo crema (
#F5F1E8) del área de contenido para reducir fatiga visual en sesiones prolongadas de monitoreo.
* **Botones y estados interactivos:** botón primario en verde EcoRoad (
#2E9E7A) para acciones de confirmación (registrar medición, cerrar incidencia); botón de alerta en rojo (
#C0392B) reservado exclusivamente para acciones críticas (crear/escalar una incidencia), evitando el uso decorativo de este color para no diluir su significado funcional.
* **Gestión de incidencias (tipo Kanban):** columnas por estado del flujo de riesgo (Alerta -> Incidencia  -> Acción correctiva -> Evidencia registrada -> Cerrada), 
con tarjetas que muestran responsable asignado, ubicación, fecha/hora y miniatura de evidencia fotográfica, facilitando el seguimiento hasta el cierre.
* **Formularios de registro de campo:** diseñados con campos grandes y espaciado generoso, priorizando el ingreso rápido de mediciones y evidencias 
(foto, descripción, fecha, hora, ubicación) desde dispositivos móviles en obra.
* **Accesibilidad:**  contraste mínimo AA (WCAG 2.1) entre texto y fondo en todas las combinaciones de la paleta, verificado especialmente en el uso del amarillo 
(#E9B44C) sobre crema, que requiere texto oscuro (#264653) para mantener legibilidad.

## 4.2. Information Architecture
<a id="4-2-information-architecture"></a>

La arquitectura de información de EcoRoad está diseñada para garantizar una navegación fluida, intuitiva y eficiente, permitiendo que tanto los ingenieros de campo (constructoras) como los auditores (supervisoras) accedan con rapidez al valor de la plataforma y a sus herramientas de gestión y fiscalización.

### 4.2.1. Organization Systems
<a id="4-2-1-organization-systems"></a>

* **Jerarquía de Contenidos:** La estructura de la información fluye de lo general a lo específico. En la Landing Page pública se prioriza la propuesta de valor HaaS/SaaS y los beneficios de Caiman, mientras que en la Web Application la jerarquía organiza el portafolio global de proyectos viales hasta llegar al detalle micro de cada tramo, punto de monitoreo e incidencia.

* **Secciones Principales de la Aplicación:** La plataforma se divide en módulos funcionales clave:
    * **Dashboard Global:** Vista ejecutiva y multi-proyecto con indicadores de salud ambiental.
    * **Mapa Interactivo:** Visualización geolocalizada de tramos viales y pines semafóricos.
    * **Gestión de Proyectos:** Alta, configuración y administración de frentes de obra viales.
    * **Puntos de Monitoreo:** Registro de telemetría y parámetros físicos (aire, ruido, agua).
    * **Tablero de Incidencias:** Flujo Kanban para el seguimiento y resolución de desvíos normativos con evidencia multimedia.
    * **Reportes y Auditorías:** Generación automatizada de expedientes y exportación en formato PDF.
    * **Configuración y Suscripción:** Gestión de planes (Base, Profesional, Enterprise) y control de accesos basados en roles (RBAC).

* **Agrupación de Contenidos:** Los datos operativos se agrupan lógicamente por severidad y contexto temporal. Las alertas y tickets críticos se destacan mediante códigos de color estandarizados (semáforo), permitiendo un escaneo visual rápido sin saturar al operador de campo.

4.2.2. Labeling Systems.

### 4.2.3. SEO Tags and Meta Tags
<a id="4-2-3-seo-tags-and-meta-tags"></a>

Para asegurar la visibilidad en motores de búsqueda y la correcta compartición en canales digitales B2B, se establecen los siguientes metadatos principales para la experiencia web de EcoRoad:

* **Landing Page (Sitio Web Estático):**
    * **Title:** `EcoRoad by Caiman | Monitoreo y Cumplimiento Ambiental en Infraestructura Vial`
    * **Meta Description:** `Plataforma HaaS/SaaS líder en el Perú para la gestión ambiental vial. Automatiza sensores IoT en comodato, alertas de umbrales y reportes de auditoría para constructoras y supervisoras.`
    * **Meta Keywords:** `monitoreo ambiental vial, cumplimiento normativo OEFA MTC, sensores IoT construcción, gestión ambiental carreteras, auditoría ambiental RPA.`
    * **Meta Author:** `Caiman Tech Startup`

* **Web Application (Plataforma Privada):**
    * **Title:** `EcoRoad App | Gestión y Fiscalización Ambiental en Tiempo Real`
    * **Meta Description:** `Panel de control privado para el seguimiento de indicadores ambientales, mapa geolocalizado de tramos viales y resolución de incidencias operativas.`
    * **Meta Keywords:** `dashboard ambiental, tramos viales, tablero kanban incidencias, reportes PDF auditoría.`
    * **Meta Author:** `Caiman Tech Startup`

### 4.2.4. Searching Systems
<a id="4-2-4-searching-systems"></a>

* **Barra de Búsqueda Global:** Ubicada de forma prominente en el encabezado principal de la Web Application, permitiendo localizar de inmediato proyectos por nombre o código de tramo vial, puntos de control específicos e incidencias registradas.
* **Filtros y Facetas Contextuales:** Herramientas de acotación de datos dentro de los módulos para filtrar la información por tipo de indicador ambiental (*aire, ruido, agua*), rango de fechas y niveles de severidad del riesgo.
* **Historial de Búsqueda:** Registro automatizado de consultas recientes para agilizar el flujo de trabajo de los auditores y residentes de obra que alternan entre múltiples frentes de trabajo.
* **Resultados Relevantes:** Priorización inteligente de resultados basada en los permisos de usuario (RBAC) y la cartera de proyectos activa asignada a su cuenta.

### 4.2.5. Navigation Systems
<a id="4-2-5-navigation-systems"></a>

* **Navegación Global:** La barra superior y el menú lateral (*Sidebar*) permanente aseguran el acceso transversal a las secciones principales de la plataforma desde cualquier pantalla del sistema.
* **Navegación Contextual:** Enlaces integrados dentro de las tarjetas de proyectos y botones de acción rápida (*CTAs*) que guían al usuario desde la vista macro del portafolio hasta el detalle analítico de una incidencia o punto de monitoreo.
* **Migas de Pan (Breadcrumbs):** Elementos de rastreo ubicados en la cabecera interna (ej. *Portafolio > Autopista Norte > Tramo 3 > Punto de Control #02*) que indican la ruta de navegación actual y permiten un retroceso jerárquico inmediato.
* **Navegación Móvil:** Adaptación mediante menús colapsables tipo hamburguesa optimizados para pantallas táctiles, asegurando la usabilidad de campo en dispositivos móviles de los ingenieros residentes.

4.3. Landing Page UI Design.

4.3.1. Landing Page Wireframe.

4.3.2. Landing Page Mock-up.

4.4. Web Applications UX/UI Design.

4.4.1. Web Applications Wireframes.

4.4.2. Web Applications Wireflow Diagrams.

4.4.2. Web Applications Mock-ups.

4.4.3. Web Applications User Flow Diagrams.

4.5. Web Applications Prototyping.

4.6. Domain-Driven Software Architecture.

La arquitectura de software de **EcoRoad** se construye a partir de los resultados obtenidos en el **Big Picture EventStorming**, el cual permitió comprender en profundidad los flujos clave del dominio de monitoreo socioambiental en proyectos de infraestructura vial y las interacciones entre residentes de obra, cuadrillas de campo, auditores regulatorios y dispositivos de telemetría IoT. A partir de este análisis inicial, se desarrolló una visión más estructurada y modular del dominio aplicando los principios del Diseño Guiado por el Dominio (*Domain-Driven Design - DDD*).

4.6.1. Design-Level Event Storming.

Para desglosar la mecánica interna de cada subdominio y profundizar desde la perspectiva de arquitectura de software, el equipo realizó una sesión de **Design-Level EventStorming**. Esta técnica permite modelar tácticamente el flujo detallado de eventos de dominio, comandos, agregados, vistas (*Read Models*) y políticas de negocio dentro del sistema, facilitando la delimitación precisa y la estructuración de los **Bounded Contexts** que conforman la plataforma **EcoRoad**.
Para esto hemos trabajado en la plataforma **Miro** acá esta el enlace del tablero completo: https://miro.com/welcomeonboard/dnVMQ0NtMXJZM28rN2laMGdLd2pwYzYxTjZLYTNRQndxMytzcTNuWisrNzJ6SEZNWEczYlU5aUl5M1hURmdBNCtTNll4V3p4Um5US1hSNjJFRzdNaUlYcUhXWkRyemd1V2VLcHhjdzZobmFwVG5vbkF0Y1FBQWRyUWFzRWI4OFNhWWluRVAxeXRuUUgwWDl3Mk1qRGVRPT0hdjE=?share_link_id=465216757647

**1. Subscriptions & Payments Context**
      
Este bounded context agrupa las actividades relacionadas con la gestión comercial, planes de suscripción y procesamiento de pagos dentro de la plataforma. Aquí se gestionan procesos como la exploración de tarifas, la selección de planes empresariales, la validación de transacciones y la activación automatizada de cuentas, asegurando el control financiero y el acceso comercial de los clientes.
<div style="text-align:center;">
  <img src="assets/chapter-4/Context1.jpg" alt="Tipografía Font">
</div>

**2. Identity & Access Management (IAM) Context**

Este bounded context agrupa las actividades relacionadas con la autenticación, autorización y control de acceso dentro de la plataforma. Aquí se gestionan procesos como el registro de cuentas de compañía, la invitación de miembros, la asignación de roles y la administración de permisos, asegurando que cada usuario acceda solo a la información y funcionalidades que le corresponden.
<div style="text-align:center;">
  <img src="assets/chapter-4/Context2.jpg" alt="Tipografía Font">
</div>

**3. Project & Road Site Management Context**

Este bounded context agrupa las actividades relacionadas con la planeación de proyectos viales, el mapeo de tramos carreteros y el despliegue de infraestructura física. Aquí se gestionan procesos como el registro general de proyectos, la sectorización de vías y la instalación de nodos de sensores, asegurando la organización espacial y operativa de los sitios de monitoreo.
<div style="text-align:center;">
  <img src="assets/chapter-4/Context3.jpg" alt="Tipografía Font">
</div>

**4. Environmental Telemetry & Monitoring Context**

Este bounded context agrupa las actividades relacionadas con la recepción, procesamiento y supervisión de los datos telemétricos capturados por los dispositivos de campo. Aquí se gestionan procesos como la ingesta masiva de lecturas de sensores (partículas en suspensión, ruido, turbidez y vibración) y la ejecución de políticas de monitoreo continuo, asegurando la trazabilidad en tiempo real de las variables ambientales.
<div style="text-align:center;">
  <img src="assets/chapter-4/Context4.jpg" alt="Tipografía Font">
</div>

**5. Threshold Evaluation & Alert Engine Context**

Este bounded context agrupa las actividades relacionadas con la evaluación normativa de datos y la generación automatizada de alertas tempranas. Aquí se gestionan procesos como la comparación de las mediciones telemétricas frente a los límites permitidos, la detección de excesos y el enrutamiento de notificaciones, asegurando una respuesta rápida ante anomalías ambientales.
<div style="text-align:center;">
  <img src="assets/chapter-4/Context5.jpg" alt="Tipografía Font">
</div>

**6. Incident & Remediation Management Context**

Este bounded context agrupa las actividades relacionadas con el ciclo de vida de los incidentes operativos y las acciones de remediación en campo. Aquí se gestionan procesos como la creación de tickets de incidencia, la notificación a cuadrillas de trabajo, la ejecución de medidas correctivas, la carga de evidencias y el cierre de casos, asegurando la mitigación efectiva de los problemas detectados.
<div style="text-align:center;">
  <img src="assets/chapter-4/Context6.jpg" alt="Tipografía Font">
</div>

**7. Compliance & Audit Reporting Context**

Este bounded context agrupa las actividades relacionadas con la trazabilidad regulatoria, la generación de reportes de cumplimiento y las bitácoras de auditoría. Aquí se gestionan procesos como la inicialización de registros históricos inmutables, la consolidación de datos regulatorios y la aplicación de políticas de retención, asegurando que todas las operaciones del sistema cumplan con las normativas legales y ambientales exigidas.
<div style="text-align:center;">
  <img src="assets/chapter-4/Context7.jpg" alt="Tipografía Font">
</div>

4.6.2. Software Architecture Context Diagram.

4.6.3. Software Architecture Container Diagrams.

4.6.4. Software Architecture Components Diagrams.

4.7. Software Object-Oriented Design.

4.7.1. Class Diagrams.

4.8. Database Design.

4.8.1. Database Diagrams.