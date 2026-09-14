Capítulo IV: Product Design

4.1. Style Guidelines.

4.1.1. General Style Guidelines.

4.1.2. Web Style Guidelines.

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

4.6.1. Design-Level Event Storming.

4.6.2. Software Architecture Context Diagram.

4.6.3. Software Architecture Container Diagrams.

4.6.4. Software Architecture Components Diagrams.

4.7. Software Object-Oriented Design.

4.7.1. Class Diagrams.

4.8. Database Design.

4.8.1. Database Diagrams.