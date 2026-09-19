Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

En esta sección se describen las decisiones, convenciones y principios adoptados por el equipo para garantizar la coherencia, trazabilidad y control de versiones durante el ciclo de vida del desarrollo de la solución EcoRoad. Se establecen los lineamientos para la configuración del entorno de desarrollo, gestión del código fuente, convenciones de estilo y configuración de despliegue.

### 5.1.1. Software Development Environment Configuration

En esta sección se especifican los productos de software utilizados durante el ciclo de vida del proyecto, incluyendo el nombre de cada herramienta, su propósito técnico específico dentro del proyecto EcoRoad, y la ruta de referencia (para software SaaS) o ruta de descarga (para productos de instalación local). Las herramientas se organizan según las siguientes disciplinas:

- Project Management
- Requirements Management
- Product UX/UI Design
- Software Development
- Software Testing
- Software Documentation

---

#### Project Management

Esta disciplina se centra en la planificación, seguimiento y control de las actividades del proyecto, asegurando el cumplimiento de los objetivos dentro del tiempo y recursos establecidos.

* **Jira:** Plataforma de gestión de proyectos ágiles utilizada para la administración del Product Backlog, planificación de Sprints, asignación de User Stories y Tasks a los miembros del equipo, y seguimiento del progreso mediante tableros Scrum con estados To-Do, In-Process, To-Review y Done.
    * **Ruta de referencia:** https://www.atlassian.com/software/jira

---

#### Requirements Management

TRELLO

---

#### Product UX/UI Design

El diseño de la experiencia de usuario y la interfaz de usuario para EcoRoad contempla un modelo de sitio web responsivo, compatible con navegadores de escritorio y dispositivos móviles. Se utilizan las siguientes herramientas:

* **UXPressia:** Plataforma para la elaboración de User Personas, Empathy Maps, Customer Journey Maps e Impact Maps de los segmentos objetivo del proyecto EcoRoad.
    * **Ruta de referencia:** https://uxpressia.com/
* **Miro:** Pizarra digital colaborativa utilizada para sesiones de Big Picture EventStorming y Design-Level EventStorming, facilitando la identificación de Bounded Contexts, Events, Commands y Aggregates del dominio EcoRoad.
    * **Ruta de referencia:** https://miro.com/es/
* **Figma:** Herramienta de diseño colaborativo para la creación de Wireframes, Mock-ups y Prototipos interactivos del Landing Page y Web Applications de EcoRoad, aplicando el Design System basado en Material Design.
    * **Ruta de referencia:** https://www.figma.com/es-es/


---

#### Software Development

El desarrollo de software del proyecto EcoRoad abarca la implementación del Landing Page, Frontend Web Application y Backend Web Services. Se utilizan las siguientes herramientas y tecnologías:

<img src="https://cdn.simpleicons.org/github" width="18" height="18" /> GitHub: Sistema de control de versiones distribuido y plataforma de hosting para repositorios de código fuente. Gestión de la organización del equipo, implementación de GitFlow Workflow, Conventional Commits y Semantic Versioning.
    
  **Ruta de referencia:** https://github.com

  **Organización del proyecto:** https://github.com/Caiman-UPC/EcoRoad_Report.git
  
<img src="https://cdn.simpleicons.org/webstorm" width="18" height="18" /> WebStorm: Entorno de desarrollo integrado (IDE) de JetBrains para la implementación del Frontend utilizando Angular Framework, HTML5, CSS3, JavaScript y TypeScript. Incluye integración con GitHub para control de versiones.
   
  **Ruta de descarga:** https://www.jetbrains.com/webstorm/
  **Licencia de estudiante:** https://www.jetbrains.com/community/education/
  
<img src="https://cdn.simpleicons.org/intellijidea" width="18" height="18" /> IntelliJ IDEA: Entorno de desarrollo integrado (IDE) de JetBrains para la implementación del Backend con Spring Boot Framework y Java. Incluye integración con Azure para despliegue de Web Services.
  
  **Ruta de descarga:** https://www.jetbrains.com/idea/
  **Licencia de estudiante:** https://www.jetbrains.com/community/education/
  
<img src="https://cdn.simpleicons.org/angular" width="18" height="18" /> Angular Framework: Framework de desarrollo para Frontend Web Applications. Construcción de componentes reutilizables, gestión de estado mediante Services y RxJS, enrutamiento entre vistas y consumo de APIs REST.
   
  **Ruta de referencia:** https://angular.io/

<img src="https://cdn.simpleicons.org/angular" width="18" height="18" /> Angular Material: Biblioteca de componentes UI basada en Material Design para Angular. Proporciona componentes pre-construidos (buttons, forms, tables, dialogs) que garantizan consistencia visual en la interfaz de EcoRoad.
  
  **Ruta de referencia:** https://material.angular.io/

<img src="https://cdn.simpleicons.org/springboot" width="18" height="18" /> Spring Boot Framework: Framework para desarrollo de Web Services RESTful del Backend de EcoRoad. Implementación de lógica de negocio, persistencia de datos con JPA/Hibernate, y documentación de API con OpenAPI/Swagger.
  
  **Ruta de referencia:** https://spring.io/projects/spring-boot
  
<img src="https://cdn.simpleicons.org/html5" width="18" height="18" /> <img src="https://cdn.simpleicons.org/css" width="18" height="18" /> <img src="https://cdn.simpleicons.org/javascript" width="18" height="18" /> HTML5, CSS3, JavaScript: Tecnologías fundamentales para la implementación del Landing Page y estructura base de las Web Applications.
   
  **HTML5:** https://html.spec.whatwg.org/
  **CSS3:** https://www.w3.org/Style/CSS/
  **JavaScript:** https://developer.mozilla.org/es/docs/Web/JavaScript

<img src="https://cdn.simpleicons.org/typescript" width="18" height="18" /> TypeScript: Lenguaje de programación tipado para desarrollo de Frontend Web Applications con Angular. Proporciona tipado estático, detección temprana de errores y mejor soporte de IDE.
   
  **Ruta de referencia:** https://www.typescriptlang.org/

<img src="https://img.icons8.com/color/48/java-coffee-cup-logo.png" width="18" height="18" /> Java: Lenguaje de programación para el desarrollo del Backend con Spring Boot. Se utiliza Java 17 para compatibilidad con Azure App Service.
  
  **Ruta de referencia:** https://openjdk.org/

---

#### Software Testing


---

#### Software Documentation

La documentación de software permite explicar el funcionamiento, uso y arquitectura de los productos desarrollados, facilitando su mantenimiento y evolución.

* **Markdown:** Lenguaje de marcado ligero para la elaboración del Project Report en el repositorio GitHub. Permite estructurar documentación con formato consistente y compatible con control de versiones.
    * **Ruta de referencia:** https://www.markdownguide.org/

5.1.2. Source Code Management.

5.1.3. Source Code Style Guide & Conventions.

5.1.4. Software Deployment Configuration.

5.2. Landing Page, Services & Applications Implementation.

5.2.X. Sprint n

5.2.X.1. Sprint Planning n.

5.2.X.2. Aspect Leaders and Collaborators.

5.2.X.3. Sprint Backlog n.

5.2.X.4. Development Evidence for Sprint Review.

5.2.X.5. Execution Evidence for Sprint Review.

5.2.X.6. Services Documentation Evidence for Sprint Review.

5.2.X.7. Software Deployment Evidence for Sprint Review.

5.2.X.8. Team Collaboration Insights during Sprint.

5.3. Validation Interviews.

5.3.1. Diseño de Entrevistas.

5.3.2. Registro de Entrevistas.

5.3.3. Evaluaciones según heurísticas.

5.4. Video About-the-Product.