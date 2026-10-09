# Capítulo V: Product Implementation, Validation & Deployment

# Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management
<a id="5-1-software-configuration-management"></a>
En esta sección se describen las decisiones, convenciones y principios adoptados por el equipo Caimán para garantizar la coherencia, trazabilidad y control de versiones durante el ciclo de vida del desarrollo de la solución EcoRoad. Se establecen los lineamientos para la configuración del entorno de desarrollo, gestión del código fuente, convenciones de estilo y configuración de despliegue.

### 5.1.1. Software Development Environment Configuration
<a id="5-1-1-software-development-environment-configuration"></a>
#### Gestión del Proyecto
Para la coordinación del proyecto y el seguimiento del trabajo colaborativo se utilizaron plataformas de comunicación, almacenamiento y gestión ágil. El código fuente de la Landing Page y del informe se centralizó en una organización de GitHub. Las reuniones virtuales del equipo y coordinaciones diarias se realizaron mediante Discord y WhatsApp, mientras que la planificación y asignación de tareas se gestionó a través de Zoho Sprints.

* **Coordinación de código y repositorios:** GitHub
* **Reuniones virtuales y syncs:** Discord
* **Comunicación diaria:** WhatsApp
* **Organización y seguimiento de tareas (Agile):** Zoho Sprints

#### Gestión de Requerimientos
Durante la fase de análisis y estructuración de requerimientos, se empleó UXPressia para diseñar las User Personas, Mapas de Empatía e Impact Maps. Se utilizó Miro para la construcción de escenarios As-Is / To-Be y los tableros de Event Storming.

* **Diseño UX y Mapas de Impacto:** UXPressia
* **Event Storming y Escenarios:** Miro
* **Gestión de User Stories:** Zoho Sprints / GitHub Projects

#### Diseño de Experiencia e Interfaz del Producto
Para la concepción visual de la Landing Page y la maquetación preliminar de las interfaces de la plataforma, el equipo empleó Figma. Se elaboraron wireframes y maquetas de alta fidelidad para validar la estructura visual, paleta de colores y la disposición de las secciones informativas antes de su codificación.

* **Diseño de Interfaz y Prototipado:** Figma

#### Desarrollo de Software
El desarrollo de la Landing Page responsiva se realizó utilizando tecnologías web estándar (HTML5, CSS3 y JavaScript). El informe del proyecto se redactó en formato Markdown (.md). Para el desarrollo del código y del informe se emplearon editores e IDEs como Visual Studio Code, WebStorm e IntelliJ IDEA, administrados mediante JetBrains Toolbox para mantener la homogeneidad del entorno.

* **IDEs y Editores:** Visual Studio Code, WebStorm, IntelliJ IDEA
* **Gestor de IDEs:** JetBrains Toolbox

#### Documentación de Software
La documentación técnica del informe se gestionó en archivos Markdown (.md) sincronizados con el repositorio central del grupo en GitHub mediante la metodología Git Flow, asegurando un trabajo colaborativo ordenado.

#### Despliegue de Software
Para la publicación de la Landing Page como primer entregable accesible al público, se utilizó GitHub Pages (o Vercel), plataforma que permite el alojamiento continuo desde la rama correspondiente del repositorio.

* **Hosting y Despliegue Continuo:** GitHub Pages / Vercel

<div style="text-align: left; max-width: 900px; margin: 0 auto;"></div>

### 5.1.2. Source Code Management
<a id="5-1-2-source-code-management"></a>

---

El equipo gestiona el código fuente mediante **GitHub** como plataforma de control de versiones, organizado bajo una organización pública que agrupa los repositorios de cada producto digital del proyecto.


**Landing Page — GitHub Pages**


Enlace de despliegue: https://caiman-upc.github.io/Landing-Page/

**Landing Page — Repositorio GitHub**

Enlace del repositorio: https://github.com/Caiman-UPC/Landing-Page.git


#### GitFlow Workflow

El equipo implementa **GitFlow** como estrategia de ramificación para gestionar el ciclo de vida del código. Las ramas definidas son:

- **`main`**: Rama principal que contiene el código de producción estable. Solo recibe merges desde `release` o `hotfix`.
- **`develop`**: Rama de integración continua donde se consolidan los features completados antes de pasar a producción.
- **`feature/<nombre-feature>`**: Rama individual para el desarrollo de cada funcionalidad. Se crea desde `develop` y se integra de vuelta a `develop` al completarse. Ejemplo: `feature/hero-section`, `feature/navbar`, `feature/contact-form`.
- **`release/<versión>`**: Rama de preparación de una nueva versión de producción. Se crea desde `develop` cuando el Sprint está completo. Ejemplo: `release/1.0.0`.
- **`hotfix/<descripción>`**: Rama para correcciones críticas en producción. Se crea desde `main`. Ejemplo: `hotfix/fix-cta-redirect`.

#### Semantic Versioning

Para el nombramiento de versiones se aplica **Semantic Versioning 2.0.0** con el formato `MAJOR.MINOR.PATCH`:
- `MAJOR`: cambios incompatibles con versiones anteriores.
- `MINOR`: nuevas funcionalidades compatibles con versiones anteriores.
- `PATCH`: correcciones de errores compatibles con versiones anteriores.

La primera versión del Landing Page se etiqueta como `v1.0.0`.

#### Conventional Commits

Para los mensajes de commit, el equipo aplica la especificación **Conventional Commits**, usando el formato:

```
<type>(<scope>): <description>
```

Los tipos permitidos son:
- `feat`: nueva funcionalidad.
- `fix`: corrección de error.
- `docs`: cambios en documentación.
- `style`: cambios de formato que no afectan la lógica.
- `refactor`: reestructuración de código sin cambio funcional.
- `chore`: tareas de mantenimiento (dependencias, configuración).
- `test`: adición o modificación de pruebas.

Ejemplos aplicados al proyecto:
```
docs(chapter2): add user empathy map
docs(chapter3): update user stories
fix(landing): correct mobile layout for plans section
docs(readme): update cover
style(landing): apply Material Design color tokens
```

### 5.1.3. Source Code Style Guide & Conventions

El equipo adopta las siguientes guías de estilo y convenciones de codificación para garantizar uniformidad y legibilidad en todos los productos. Toda nomenclatura se redacta en **inglés**.

#### HTML5 & CSS3 (Landing Page)
- Se aplica la guía **W3Schools HTML Style Guide** para estructura semántica, indentación con 2 espacios, atributos en minúsculas y uso de comillas dobles.
- Se aplica la guía **Google HTML/CSS Style Guide** para nomenclatura de clases en `kebab-case`, evitar el uso de selectores de ID en CSS y priorizar propiedades abreviadas.
- El diseño visual se basa en **Material Design** como sistema de diseño de referencia.

#### TypeScript & Angular (Frontend Web Application)
- Se aplica la **Angular Coding Style Guide** oficial: componentes con sufijo `Component`, servicios con sufijo `Service`, módulos con sufijo `Module`.
- Nombres de archivos en `kebab-case`: `project-list.component.ts`.
- Se aplica la **Google TypeScript Style Guide** para tipado estricto y gestión de imports.

#### Gherkin (Acceptance Criteria)
- Se aplican las **Gherkin Conventions for Readable Specifications**: un solo nivel de indentación para `Given/When/Then`, escenarios en inglés, descripciones en tercera persona.

---

### 5.1.4. Software Deployment Configuration

En esta sección se describe la configuración de despliegue para el Landing Page, único producto desplegado en el Sprint 1.

#### Landing Page — GitHub Pages

El Landing Page de EcoRoad se despliega como sitio web estático mediante **GitHub Pages**, directamente desde el repositorio:

**Pasos para el despliegue:**

1. Asegurarse de que la rama `main` contiene los archivos del Landing Page (`index.html`, carpetas `css/`, `js/`, `assets/`).
2. Ingresar al repositorio en GitHub y navegar a **Settings > Pages**.
3. En la sección **Source**, seleccionar la rama `main` y la carpeta `/ (root)`.
4. Hacer clic en **Save**. GitHub Pages genera automáticamente la URL de despliegue.
5. Verificar el sitio desplegado en la URL generada por GitHub Pages.

Cualquier push a la rama `main` actualiza automáticamente el sitio desplegado.

## 5.2. Landing Page, Services & Applications Implementation.

### 5.2.1. Sprint 1

<p>
  Durante el Sprint 1, el equipo se enfocó en el desarrollo e implementación del Landing Page de EcoRoad, incluyendo todas las secciones de presentación del negocio con soporte bilingüe (español/inglés) y despliegue mediante GitHub Pages.
</p>

<p>
  <strong>Repositorio:</strong> <a href="https://github.com/Caiman-UPC/Landing-Page.git">https://github.com/Caiman-UPC/Landing-Page.git</a>
</p>

<p>
  <strong>Landing Page Desplegada:</strong> <a href="https://caiman-upc.github.io/Landing-Page/">https://caiman-upc.github.io/Landing-Page/</a>
</p>

#### 5.2.1.1. Sprint Planning.

<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <th colspan="2" style="text-align: center;">Sprint Planning Sprint 1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint Planning Background</strong></td>
    </tr>
    <tr>
      <td>Date</td>
      <td>14/09/2026</td>
    </tr>
    <tr>
      <td>Time</td>
      <td>10:00 p.m.</td>
    </tr>
    <tr>
      <td>Location</td>
      <td>Discord</td>
    </tr>
    <tr>
      <td>Prepared By</td>
      <td>Miguel Ángel Junior Román López</td>
    </tr>
    <tr>
      <td>Attendees (to planning meeting)</td>
      <td>
        Román López, Miguel Ángel Junior<br>
        Salcedo Muñoz, Andy Alfredo Hipolito<br>
        Guillen Chavez, Eduardo Martín<br>
        Yarleque Ruiz, Cristina Marcela<br>
        Torres Júarez, Alisee Muriel
      </td>
    </tr>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint 0 Review Summary</strong></td>
    </tr>
    <tr>
      <td colspan="2">N/A (Este es el primer sprint del proyecto)</td>
    </tr>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint 0 Retrospective Summary</strong></td>
    </tr>
    <tr>
      <td colspan="2">N/A (Este es el primer sprint del proyecto)</td>
    </tr>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint Goal & User Stories</strong></td>
    </tr>
    <tr>
      <td colspan="2"><strong>Sprint 1 Goal (Outcome–Impact–Customer–Confirmation):</strong><br><br>
<em>Our focus is on delivering the first bilingual marketing Landing Page of EcoRoad that clearly communicates the value proposition and service offering to first-time visitors.</em><br><br>
<em>We believe it conveys a clear and trustworthy first impression to road construction, maintenance, and rehabilitation companies, helping them quickly understand what EcoRoad does and how to contact the team.</em><br><br>
<em>This will be confirmed when users from both segments can navigate through all core sections (Hero, Services, Pricing, About Us, Team, Contact) in Spanish and English and can reach the Contact section in no more than three clicks from the home view.</em>
      </td>
    </tr>
    <tr>
      <td>Sprint 1 Velocity</td>
      <td>13 Story Points</td>
    </tr>
    <tr>
      <td>Sum of Story Points</td>
      <td>13 SP (≈ 53 horas estimadas)</td>
    </tr>
  </tbody>
</table>

#### 5.2.1.2. Aspect Leaders and Collaborators.

<p>
En esta sección se presenta la matriz <strong>Leadership-and-Collaboration Matrix (LACX)</strong> correspondiente al Sprint 1. 
Su propósito es identificar claramente los aspectos principales del sprint y asignar responsabilidades de liderazgo (<strong>L</strong>) y colaboración (<strong>C</strong>) para fortalecer la comunicación, coordinación y trazabilidad del trabajo dentro del equipo.
</p>

<p>
Estos aspectos se derivan directamente de los objetivos definidos en el Sprint 1 Goal, asegurando cobertura total de los entregables planificados.
</p>

<ul>
  <li><strong>Landing Page Development & Deployment:</strong> Diseño, estructura, contenido y funcionalidad de la página principal del proyecto, incluyendo su despliegue.</li>
  <li><strong>Report Module Implementation:</strong> Desarrollo y presentación del módulo que permitirá crear, visualizar y exportar el reporte requerido.</li>
</ul>

<table border="1" cellpadding="4" cellspacing="0" align="center">
  <thead>
    <tr>
      <th>Team Member (Last Name, First Name)</th>
      <th>Aspect: Landing Page</th>
      <th>Aspect: Report Module</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Román López, Miguel Ángel Junior</td><td>L</td><td>C</td></tr>
    <tr><td>Guillen Chavez Eduardo Martín</td><td>C</td><td>L</td></tr>
    <tr><td>Salcedo Muñoz Andy Alfredo Hipolito/td><td>C</td><td>C</td></tr>
    <tr><td>Torres Júarez Alisee Muriel</td><td>C</td><td>C</td></tr>
    <tr><td>Yarleque Ruiz Cristina Marcela</td><td>C</td><td>C</td></tr>
  </tbody>
</table>

<ul>
  <li><strong>L</strong> = Líder del aspecto</li>
  <li><strong>C</strong> = Colaborador en el aspecto</li>
</ul>

<p>
Esta organización de roles está alineada con la posterior asignación de tareas del Sprint Backlog, permitiendo que cada líder supervise la ejecución de su aspecto con apoyo de sus colaboradores. 
Con ello, se garantiza una gestión más eficiente del progreso y una mejor sincronización entre los miembros del equipo.
</p>


### 5.2.1.3. Sprint Backlog 1.

El Sprint Backlog 1 reúne las historias de usuario y tareas necesarias para implementar la primera versión de la landing page, incluyendo el menú de navegación, la visualización de planes, la sección de creadores, redes sociales, el formulario de contacto y el cambio de idioma.

Todas las tareas son monitoreadas y actualizadas mediante **Jira Software**.

A continuación, la estructura de la tabla de control de estado para el Sprint:

| Story Id | Title | Task Id | Task Title | Assigned To | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| US01 | Propuesta de valor | T01 | Implementar sección Hero y Header | Román López | Done |
| US05 | Soluciones monitoreo | T02 | Implementar grilla de Soluciones Ambientales | Yarleque Ruiz | Done |
| US06 | Beneficios plataforma| T03 | Maquetar tarjetas de beneficios (Cero multas) | Torres Juárez | Done |
| US10 | Selección de planes | T04 | Implementar sección Pricing (SaaS/HaaS) | Guillen Chavez | Done |
| US12 | Formulario contacto | T05 | Integrar validaciones en Formulario Contact | Salcedo Muñoz | Done |
| US15 | Cambio de idioma | T06 | Implementar i18n (Inglés/Español) | Yarleque Ruiz | Done |
| US03 | Responsive Design | T07 | Ajustar media queries para Mobile Web | Román López | Done |

El seguimiento y la actualización del Sprint Backlog se realizan en **Jira Software** mediante el tablero Scrum del proyecto, donde se registran los estados de cada tarea (To-do, In-Process, To-Review, Done). Durante las reuniones diarias (**Daily Scrum**), el equipo revisa el avance, actualiza el estado de las tareas y gestiona posibles bloques.

#### 5.2.1.4. Development Evidence for Sprint Review.

En el Sprint 1 se construyó la primera versión navegable del Landing Page con las secciones Home (Hero), Solutions, Benefits, Features, Testimonials, Pricing, Our Team y Contact, además del footer, los estilos responsivos y el cambio de idioma. La implementación consta de `index.html`, `assets/styles.css` y `assets/script.js`.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
|---|---|---|---|---|---|
| Caiman-UPC/Landing-Page | main | 8a4c8ca | first commit | — | 20/09/2026 |
| Caiman-UPC/Landing-Page | main | 41eebd8 | Agregando todos los archivos del proyecto | — | 20/09/2026 |
| Caiman-UPC/Landing-Page | main | a0587f1 | Organizando archivos en la raiz para GitHub Pages | — | 20/09/2026 |

#### 5.2.1.5. Execution Evidence for Sprint Review.

En el Sprint 1 se alcanzó la publicación del Landing Page con ocho secciones navegables desde el header, diseño adaptable a escritorio y móvil, y cambio de idioma entre inglés (por defecto) y español.

Video de navegación del Landing Page: `[POR COMPLETAR: URL en Microsoft Stream]` — Duración: `[POR COMPLETAR]`

| Vista | Captura |
|---|---|
| Header y navegación | `[POR COMPLETAR: captura]` |
| Hero | `[POR COMPLETAR: captura]` |
| Solutions | `[POR COMPLETAR: captura]` |
| Benefits | `[POR COMPLETAR: captura]` |
| Features | `[POR COMPLETAR: captura]` |
| Testimonials | `[POR COMPLETAR: captura]` |
| Pricing | `[POR COMPLETAR: captura]` |
| Our Team | `[POR COMPLETAR: captura]` |
| Contact | `[POR COMPLETAR: captura]` |
| Footer | `[POR COMPLETAR: captura]` |
| Vista móvil (600 px) | `[POR COMPLETAR: captura]` |
| Versión en español | `[POR COMPLETAR: captura]` |

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

El alcance del Sprint 1 es el Landing Page, un sitio web estático; por lo tanto, no se implementaron ni documentaron Web Services en este Sprint.

| Endpoint | Acciones implementadas | Documentación |
|---|---|---|
| No aplica | No hay Web Services en el alcance del Sprint 1. | No aplica |

#### 5.2.1.7. Software Deployment Evidence for Sprint Review
El sitio fue desplegado exitosamente en GitHub Pages.
* **URL:** https://caiman-upc.github.io/Landing-Page/

#### 5.2.1.8. Team Collaboration Insights during Sprint.

<p>
Durante el Sprint 1, los analíticos de colaboración de GitHub muestran una participación activa y continua de todos los miembros del equipo sobre el repositorio de la Landing Page. En el panel de Overview se observa un flujo constante de commits distribuidos a lo largo de los días del sprint, lo que evidencia que las tareas de implementación de las distintas secciones (hero, servicios, planes, equipo, testimonios, contacto y footer) se desarrollaron de manera incremental y coordinada. Cada integrante realizó aportes directos al código, ya sea mediante la creación de nuevas secciones, ajustes de estilos responsivos o correcciones derivadas de las revisiones entre pares, asegurando así que el entregable del sprint se construyera de forma colaborativa y no centralizada en una sola persona.
</p>

![overview-spring1.png](../assets/img/chapter-V/overview-spring1.png)
<p>
El Network Graph refleja esta dinámica mediante la presencia de ramas que nacen desde main y regresan a ella una vez integradas, siguiendo el flujo definido por GitFlow. Esta visualización confirma que las contribuciones individuales se alinearon con el marco de trabajo acordado: se desarrollaron cambios en ramas aisladas, se realizaron pruebas locales y posteriormente se integraron al tronco principal, lo que redujo conflictos y facilitó el seguimiento de la trazabilidad de cada cambio. De este modo, la colaboración no solo se dio a nivel de cantidad de commits, sino también en la forma de trabajo estructurada y compatible con las prácticas ágiles del equipo.
</p>

![network-graph-sprint1.png](../assets/img/chapter-V/network-graph-sprint1.png)

<p>
Finalmente, el gráfico de Visitors evidencia que, conforme avanzaba el desarrollo y se consolidaban las funcionalidades del Landing Page, el repositorio comenzó a recibir visitas y visualizaciones, lo que sugiere interés progresivo en el producto por parte de stakeholders y del propio equipo durante las actividades de revisión y validación. En conjunto, estos analíticos de colaboración y actividad en GitHub demuestran que todos los integrantes tuvieron participación efectiva en la implementación del producto del Sprint (Landing Page) y sientan la base para replicar este mismo patrón de trabajo en los siguientes sprints, donde se abordarán la Web Application y los Web Services.
</p>

![visitors-sprint1.png](../assets/img/chapter-V/visitors-sprint1.png)

### 5.2.2. Sprint 2

<p>
  Durante el Sprint 2, el equipo se enfocó en el desarrollo del módulo frontend de gestión de tareas, 
  miembros y grupos de la aplicación web EcoRoad. Este sprint se centró en integrar componentes con el 
  backend mediante servicios REST, crear flujos de navegación funcionales entre vistas y aplicar mejoras 
  en la interfaz visual con Angular y Angular Material.
</p>

<p>
  <strong>Repositorio Frontend:</strong> <a href=""></a>
</p>

<p>
  <strong>Backend API (Local):</strong> <a href=""></a>
</p>

#### 5.2.2.1. Sprint Planning 2

<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <th colspan="2" style="text-align: center;">Sprint Planning Sprint 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint Planning Background</strong></td>
    </tr>
    <tr>
      <td>Date</td>
      <td>09/10/2026</td>
    </tr>
    <tr>
      <td>Time</td>
      <td>09:30 p.m.</td>
    </tr>
    <tr>
      <td>Location</td>
      <td>Discord</td>
    </tr>
    <tr>
      <td>Prepared By</td>
      <td>Miguel Ángel Junior Román López</td>
    </tr>
    <tr>
      <td>Attendees (to planning meeting)</td>
      <td>
        Román López, Miguel Ángel Junior
        Salcedo Muñoz, Andy Alfredo Hipolito
        Guillen Chavez, Eduardo Martín
        Yarleque Ruiz, Cristina Marcela
        Torres Júarez, Alisee Muriel
      </td>
    </tr>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint 1 Review Summary</strong></td>
    </tr>
    <tr>
      <td colspan="2">
        Se completó el desarrollo y despliegue de la Landing Page, incluyendo todas las secciones planificadas 
        y la funcionalidad de cambio de idioma.
      </td>
    </tr>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint 1 Retrospective Summary</strong></td>
    </tr>
    <tr>
      <td colspan="2">
        El equipo identificó la necesidad de mejorar la comunicación diaria y la asignación de sub-tareas 
        en Jira para evitar solapamientos. Se acordó utilizar etiquetas más claras por responsable y realizar 
        revisiones de código colaborativas al cierre de cada día.
      </td>
    </tr>
    <tr>
      <td colspan="2" style="text-align: center;"><strong>Sprint Goal & User Stories</strong></td>
    </tr>
    <tr>
      <td colspan="2"><strong>Sprint 2 Goal (Outcome–Impact–Customer–Confirmation):</strong><br><br>
<em>Our goal is to enable project managers and environmental engineers to manage road projects, work fronts, and field crews via a unified web interface connected to EcoRoad's backend services.</em><br><br>
<em>We believe this provides site residents, environmental supervisors, and operations staff with better visibility and coordination of mitigation activities by centralizing telemetry alerts and compliance records in a single location.</em><br><br>
<em>This will be confirmed when an engineer or site resident can create, update, and view environmental incidents linked to road sections and assigned personnel—as well as filter them by risk level and status—using the web application, with data stored and retrieved via the backend API.</em>
      </td>
    </tr>
    <tr>
      <td>Sprint 2 Velocity</td>
      <td>16 Story Points</td>
    </tr>
    <tr>
      <td>Sum of Story Points</td>
      <td>16 SP (≈ 64 horas estimadas)</td>
    </tr>
  </tbody>
</table>

#### 5.2.2.2. Aspect Leaders and Collaborators

<p>
Para el Sprint 2 se presenta la matriz <strong>Leadership-and-Collaboration Matrix (LACX)</strong>, donde se definen los roles de liderazgo (<strong>L</strong>) y colaboración (<strong>C</strong>) por aspecto técnico y funcional del desarrollo frontend basado en Angular.
</p>

<p>
Estos aspectos se derivan directamente de los objetivos establecidos en el <em>Sprint 2 Goal</em>, garantizando que cada componente clave del módulo frontend cuente con un responsable principal y con el apoyo colaborativo necesario para su implementación efectiva.
</p>

<ul>
  <li><strong>Integración Frontend–Backend:</strong> Consumo de endpoints, configuración de servicios HTTP y validación de la conexión con la API local.</li>
  <li><strong>Gestión de Tareas (UI):</strong> Desarrollo de componentes Angular para la visualización, filtrado y navegación entre tareas.</li>
  <li><strong>Gestión de Miembros y Grupos:</strong> Creación de componentes de detalle y listado de miembros y grupos asociados al proyecto.</li>
</ul>

<table border="1" cellpadding="4" cellspacing="0" align="center">
  <thead>
    <tr>
      <th>Team Member (Last Name, First Name)</th>
      <th>Aspect: API Integration</th>
      <th>Aspect: Task UI</th>
      <th>Aspect: Members &amp; Groups</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Yarleque Ruiz, Cristina Marcela</td><td>L</td><td>C</td><td>C</td></tr>
    <tr><td>Román López, Miguel Ángel Junior</td><td>C</td><td>L</td><td>C</td></tr>
    <tr><td>Salcedo Muñoz, Andy Alfredo Hipolito</td><td>C</td><td>C</td><td>L</td></tr>
    <tr><td>Guillen Chavez, Eduardo Martín</td><td>C</td><td>C</td><td>C</td></tr>
    <tr><td>Torres Júarez, Alisee Muriel</td><td>C</td><td>C</td><td>C</td></tr>
  </tbody>
</table>

<ul>
  <li><strong>L</strong> = Líder del aspecto</li>
  <li><strong>C</strong> = Colaborador en el aspecto</li>
</ul>

<p>
La asignación de roles busca optimizar la ejecución del sprint, favoreciendo la especialización técnica y la cooperación entre los miembros. 
Cada líder coordina las tareas relacionadas con su aspecto a través de <strong>Jira Software</strong>, supervisando avances, revisiones de código y validaciones funcionales con sus colaboradores.
</p>

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

<p>
  <a href="">Frontend EcoRoad</a> — 
  <a href=""></a>
</p>

#### 5.2.2.8. Team Collaboration Insights during Sprint

<p>
Durante el Sprint 2, los analíticos de colaboración del repositorio EcoRoad-Frontend evidencian una participación constante de todos los integrantes del equipo sobre el código de la aplicación web EcoRoad. A lo largo del sprint se registran commits frecuentes asociados a la implementación de los módulos de proyectos viales, tramos de carreteras, tablero Kanban de incidencias y visualización de telemetría IoT sobre mapas geolocalizados, así como a las mejoras visuales implementadas con Angular y Angular Material. Esta actividad distribuida confirma que la construcción de la Web Application se realizó de forma incremental, respetando las responsabilidades definidas en el Sprint 2 Goal y la matriz LACX (Project & GIS Dashboard, Alerts & Incident Kanban, Landing Page v1.1 & Deploy), y evitando la concentración del desarrollo en un solo miembro.
</p>

<img src="../images/overview-sprint2.jpg" alt="overview-sprint2">

<p>
El Network Graph correspondiente al Sprint 2 muestra un uso activo del flujo de trabajo basado en GitFlow, con ramas de características (features) creadas para la gestión de proyectos viales, el visor GIS de telemetría y el tablero interactivo de incidencias, que luego fueron fusionadas a la rama principal tras las respectivas revisiones de código entre pares. Este patrón de ramas y merges refleja que los líderes de cada aspecto coordinaron el trabajo con sus colaboradores, alineados con las prácticas definidas para el proyecto (feature branches, conventional commits y consolidación en develop/main), reforzando la trazabilidad y la calidad del código entregado durante el sprint.
</p>

<img src="../images/network-graph-sprint2.jpg" alt="network-graph-sprint2">

<p>
Finalmente, el gráfico de Visitors del repositorio frontend muestra un incremento sostenido de visitas y vistas de página conforme se acercaban las fechas de integración de vistas y despliegue en Vercel, lo que demuestra que el equipo utilizó activamente el repositorio como punto central para revisar avances, validar flujos interactivos y preparar la Sprint Review. En conjunto, estos analíticos de overview, network graph y visitors confirman que, durante el Sprint 2, todos los miembros del equipo participaron efectivamente en la implementación de la Web Application y en su preparación para la futura integración con los Web Services, cumpliendo con el principio de que cada integrante contribuya a los distintos productos definidos en el proyecto (Landing Page, Web Applications, Web Services) según el alcance de cada sprint.
</p>

<img src="../images/visitors-sprint2.jpg" alt="visitors-sprint2">

5.3. Validation Interviews.

5.3.1. Diseño de Entrevistas.

5.3.2. Registro de Entrevistas.

5.3.3. Evaluaciones según heurísticas.

## 5.4. Video About-the-Product

<p>
  El video "About the Product" presenta de manera clara y atractiva la propuesta de valor de EcoRoad, 
  los problemas que resuelve y cómo funciona la solución para ambos segmentos objetivo.
</p>

<h4>Información General del Video</h4>

<table border="1" cellpadding="4" cellspacing="0">
  <tbody>
    <tr>
      <td><strong>Título del Video</strong></td>
      <td>EcoRoad: </td>
    </tr>
    <tr>
      <td><strong>Duración</strong></td>
      <td>0 minutos 0 segundos</td>
    </tr>
    <tr>
      <td><strong>Fecha de Grabación</strong></td>
      <td>//2026</td>
    </tr>
    <tr>
      <td><strong>URL YouTube</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>URL Microsoft Stream</strong></td>
      <td><a href=""></a></td>
    </tr>
  </tbody>
</table>

<p><strong>Screenshot del video:</strong></p>
<img src="../images/AboutTheProduct-image.png" alt="About the Product Video">

<h4>Contenido del Video</h4>

<p>
  El video está estructurado en las siguientes secciones:
</p>

<ol>
  <li>
    <strong>Introducción (0:00 - 0:00):</strong> Presentación del problema - .
  </li>
  <li>
    <strong>Propuesta de Solución (0:00 - 0:00):</strong> Presentación de EcoRoad como la solución integral 
    para.
  </li>
  <li>
    <strong>Funcionalidades Principales (0:00 - 0:00):</strong> Demostración de las características clave:
    <ul>
      <li>Gestión de </li>
      <li>Control de</li>
      <li>Portal </li>
      <li>Generación de reportes</li>
    </ul>
  </li>
  <li>
    <strong>Beneficios (0:00 - 0:00):</strong> Énfasis en beneficios para ambos segmentos - .
  </li>
  <li>
    <strong>Llamada a la Acción (0:00 - 0:00):</strong> Invitación a visitar el Landing Page y conocer 
    más sobre EcoRoad.
  </li>
</ol>


<h4>Inscripción en Landing Page</h4>

<p>
  El video "About the Product" está embebido en el Landing Page en la sección de "Acerca del Producto", 
  permitiendo que visitantes del sitio vean una introducción visual de EcoRoad antes de registrarse o 
  solicitar más información.
</p>

<p>
  <strong>URL del Landing Page donde está el video:</strong> 
  <a href=""></a>
</p>


---

## Conclusiones

### Conclusiones y recomendaciones

<p>
 Al finalizar el ciclo de desarrollo y validación de la plataforma EcoRoad, el equipo ha llegado a las siguientes conclusiones, contrastando los resultados obtenidos con los planteamientos iniciales del proceso Lean UX:
</p>

<p><strong>1. Validación de Problem Statements y Supuestos (Assumptions):</strong></p>
<p>
  Inicialmente, se estableció como Problem Statement que las empresas constructoras y de mantenimiento vial sufrían de un registro manual, fragmentado y tardío de indicadores ambientales (aire, ruido, agua) mediante planillas físicas y hojas de cálculo. Esta situación les impedía conectar la medición con una respuesta inmediata ante las fiscalizaciones del MTC u OEFA. Tras las entrevistas de validación, se confirmó que esta dispersión genera "ceguera operativa" y estrés en los residentes de obra al momento de compilar los reportes, validando nuestro enfoque en la plataforma centralizada. Nuestro supuesto de negocio (Business Assumption) indicaba que el mayor riesgo era que los equipos de campo se resistieran a adoptar el registro digital y mantuvieran métodos manuales. Sin embargo, la validación demostró que el segmento operativo demanda con urgencia una aplicación móvil, desafiando el supuesto de baja adopción tecnológica siempre y cuando la herramienta cuente con un funcionamiento 100% offline (sin conexión), dado que operan en tramos donde hasta el 70% de la carretera carece de señal.
</p>

<p><strong>2. Contrastación de Hipótesis (Hypothesis Statements):</strong></p>
<ul>
  <li>
    <strong>Hipótesis de Valor para Ingenieros y Gerentes:</strong> Se planteó que al proporcionar un dashboard ambiental geolocalizado por proyecto, se lograría reducir en al menos un 50% el tiempo de detección de incumplimientos normativos. Los hallazgos confirmaron esta hipótesis, ya que la funcionalidad de ver en tiempo real el estado de cada tramo resuelve directamente el dolor de la gestión multisitio en vías abiertas al tráfico.
  </li>
  <li>
    <strong>Hipótesis de Registro de Evidencias:</strong> Se creía que el registro de evidencias (fotografía, fecha, hora y ubicación) asociado a cada incidencia garantizaría que los expedientes de cumplimiento fuesen aceptados sin observaciones. Las entrevistas indicaron que esta característica es vital, pues los especialistas ambientales confirmaron que perder información y fotografías en chats informales de WhatsApp les ha costado paralizaciones de frentes de obra y multas.
  </li>
</ul>

<p><strong>3. Cumplimiento de Criterios de Éxito:</strong></p>
<p>
  Se logró diseñar la arquitectura del sistema, integrando una Landing Page, una Single Page Application en Angular y un API en Spring Boot para procesar la telemetría IoT y los tickets de incidencia. Los criterios de éxito apuntaban a que los clientes registren al menos el 70% de las mediciones de los proyectos directamente en la plataforma. No obstante, los resultados mostraron que el éxito de estas métricas depende de la autonomía del usuario en condiciones ambientales extremas. Esto sugiere que la usabilidad de la interfaz bajo luz solar directa (fuentes tipográficas de alto peso) y la capacidad de sincronización de datos por lotes (batch) tras recuperar la conexión son obligatorias para cumplir dicho criterio de adopción.   
</p>

<p><strong>Recomendaciones (Roadmap):</strong></p>
<p>
  Basados en los hallazgos y el análisis competitivo actual, se recomienda para las siguientes etapas de los productos digitales:
</p>
<ul>
  <li>
    <strong>Desarrollo de Aplicación Nativa Móvil Offline-First:</strong> Dado el uso exclusivo de smartphones en terrenos con conectividad inestable o nula, se recomienda migrar el módulo operativo de campo hacia una app nativa robusta que utilice bases de datos locales. Esto garantizará el registro ininterrumpido de evidencias geolocalizadas que se sincronicen de manera automática al recuperar la señal.
  </li>
  <li>
    <strong>Integración con Suites de Construcción Corporativas:</strong> Para contrarrestar la amenaza de suites generales (como Autodesk Construction Cloud) identificada en el análisis competitivo, se sugiere desarrollar APIs que permitan exportar las incidencias ambientales y mapas directamente a los modelos BIM o software de control documental que ya utilizan las grandes constructoras.
  </li>
  <li>
    <strong>Apertura del Ecosistema IoT (Hardware Agnostic):</strong> Se recomienda refinar el módulo Asset Management Backend para permitir que las empresas no solo adquieran equipos bajo el modelo HaaS de EcoRoad, sino que puedan conectar sus propios sensores ambientales preexistentes mediante protocolos estándar, reduciendo significativamente los costos de capital (CapEx) para facilitar el cierre de ventas.
  </li>

## Video About-the-Team

<p>
  El video "About the Team" presenta al equipo de desarrollo de Caiman, destacando las habilidades, 
  roles y contribuciones de cada miembro en el proyecto EcoRoad. Este video complementa la documentación del 
  proyecto mostrando el lado humano detrás del desarrollo de la solución.
</p>

<h4>Información General del Video</h4>

<table border="1" cellpadding="4" cellspacing="0">
  <tbody>
    <tr>
      <td><strong>Título del Video</strong></td>
      <td>Caimán: Meet the Team Behind EcoRoad</td>
    </tr>
    <tr>
      <td><strong>Duración</strong></td>
      <td>?? minutos ?? segundos</td>
    </tr>
    <tr>
      <td><strong>Fecha de Grabación</strong></td>
      <td>//</td>
    </tr>
    <tr>
      <td><strong>URL YouTube</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>URL Microsoft Stream</strong></td>
      <td><a href=""></a></td>
    </tr>
  </tbody>
</table>

<p><strong>Screenshot del video:</strong></p>
<img src="../images/AboutTheTeam-image.png" alt="EcoRoad About the Team">

<h4>Contenido del Video</h4>

<p>
  El video incluye presentaciones individuales de cada miembro del equipo, destacando:
</p>

<ul>
  <li>Nombre completo y rol en el proyecto</li>
  <li>Responsabilidades principales durante el desarrollo</li>
  <li>Tecnologías y herramientas utilizadas</li>
  <li>Aprendizajes clave del proyecto VEYRA</li>
  <li>Expectativas para futuras iteraciones</li>
</ul>

<h4>Miembros del Equipo</h4>

<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <th>Nombre Completo</th>
      <th>Rol Principal</th>
      <th>Contribuciones Destacadas</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Guillen Chavez, Eduardo Martín</td>
      <td>Backend and Frontend Developer</td>
      <td>Implementación de servicios REST, arquitectura del Backend</td>
    </tr>
    <tr>
      <td>Salcedo Muñoz, Andy Alfredo Hipolito</td>
      <td>Backend and Frontend Developer</td>
      <td>Configuración de Azure, Vercel y GitHub Pages</td>
    </tr>
    <tr>
      <td>Torres Júarez, Alisee Muriel</td>
      <td>Backend and Frontend Developer</td>
      <td>Diseño de interfaces, implementación de componentes Angular</td>
    </tr>
    <tr>
      <td>Roman Lopez, Miguel Angel Junior</td>
      <td>Backend and Frontend Developer</td>
      <td>Desarrollo de vistas, integración con API Backend</td>
    </tr>
    <tr>
      <td>Yarleque Ruiz, Cristina Marcela</td>
      <td>Backend and Frontend Developer</td>
      <td>Diseño de diagramas C4, Frontend, Backend y DataBase</td>
    </tr>
  </tbody>
</table>

<div style="page-break-after: always;"></div>

## Bibliografía

<ul>
  <li>
    Adzic, G. (s.f.). <em>Impact Mapping</em>. 
    Recuperado de <a href="https://www.impactmapping.org/">https://www.impactmapping.org/</a>
  </li>
  <li>
    Angular. (s.f.). <em>Angular Coding Style Guide</em>. 
    Recuperado de <a href="https://angular.io/guide/styleguide">https://angular.io/guide/styleguide</a>
  </li>
  <li>
    Brandolini, A. (s.f.). <em>Introducing EventStorming</em>. 
    Recuperado de <a href="https://www.eventstorming.com/">https://www.eventstorming.com/</a>
  </li>
  <li>
    CareerFoundry. (s.f.). <em>What are User Flows in User Experience (UX) Design?</em>. 
    Recuperado de <a href="https://careerfoundry.com/en/blog/ux-design/what-are-user-flows/">https://careerfoundry.com/en/blog/ux-design/what-are-user-flows/</a>
  </li>
  <li>
    Cohn, M. (s.f.). <em>User Stories</em>. Mountain Goat Software. 
    Recuperado de <a href="https://www.mountaingoatsoftware.com/agile/user-stories">https://www.mountaingoatsoftware.com/agile/user-stories</a>
  </li>
  <li>
    Cone, M. (s.f.). <em>The Markdown Guide</em>. 
    Recuperado de <a href="https://www.markdownguide.org/">https://www.markdownguide.org/</a>
  </li>
  <li>
    Conventional Commits. (s.f.). <em>Conventional Commits</em>. 
    Recuperado de <a href="https://www.conventionalcommits.org/">https://www.conventionalcommits.org/</a>
  </li>
  <li>
    Cucumber. (s.f.). <em>Gherkin Reference</em>. 
    Recuperado de <a href="https://cucumber.io/docs/gherkin/reference/">https://cucumber.io/docs/gherkin/reference/</a>
  </li>
  <li>
    Driessen, V. (2010). <em>A successful Git branching model</em>. nvie.com. 
    Recuperado de <a href="https://nvie.com/posts/a-successful-git-branching-model/">https://nvie.com/posts/a-successful-git-branching-model/</a>
  </li>
  <li>
    DZone. (s.f.). <em>Acceptance Criteria in Scrum: Explanation, Examples, and Template</em>. 
    Recuperado de <a href="https://dzone.com/articles/acceptance-criteria-in-software-explanation-exampl">https://dzone.com/articles/acceptance-criteria-in-software-explanation-exampl</a>
  </li>
  <li>
    Evans, E. (2004). <em>Domain-Driven Design: Tackling Complexity in the Heart of Software</em>. Addison-Wesley Professional.
    Recuperado de <a href="https://www.oreilly.com/library/view/domain-driven-design-tackling/0321125215/">https://www.oreilly.com/library/view/domain-driven-design-tackling/0321125215/</a>
  </li>
  <li>
    Fowler, M. (2006). <em>Ubiquitous Language</em>. 
    Recuperado de <a href="https://martinfowler.com/bliki/UbiquitousLanguage.html">https://martinfowler.com/bliki/UbiquitousLanguage.html</a>
  </li>
  <li>
    Google. (s.f.). <em>Google HTML/CSS Style Guide</em>. 
    Recuperado de <a href="https://google.github.io/styleguide/htmlcssguide.html">https://google.github.io/styleguide/htmlcssguide.html</a>
  </li>
  <li>
    Google. (s.f.). <em>Google JavaScript Style Guide</em>. 
    Recuperado de <a href="https://google.github.io/styleguide/jsguide.html">https://google.github.io/styleguide/jsguide.html</a>
  </li>
  <li>
    Google. (s.f.). <em>Google TypeScript Style Guide</em>. 
    Recuperado de <a href="https://google.github.io/styleguide/tsguide.html">https://google.github.io/styleguide/tsguide.html</a>
  </li>
  <li>
    Google. (s.f.). <em>Google Java Style Guide</em>. 
    Recuperado de <a href="https://google.github.io/styleguide/javaguide.html">https://google.github.io/styleguide/javaguide.html</a>
  </li>
  <li>
    Gothelf, J., & Seiden, J. (2021). <em>Lean UX: Designing Great Products with Agile Teams</em> (3rd ed.). O'Reilly Media.
    Recuperado de <a href="https://www.oreilly.com/library/view/lean-ux-2nd/9781491953594/">https://www.oreilly.com/library/view/lean-ux-2nd/9781491953594/</a>
  </li>
  <li>
    HubSpot. (s.f.). <em>Full List of Meta Tags, Why They Matter for SEO & How to Write Them</em>. 
    Recuperado de <a href="https://blog.hubspot.com/marketing/meta-tags">https://blog.hubspot.com/marketing/meta-tags</a>
  </li>
  <li>
    IBM Design. (s.f.). <em>Empathy Map</em>. Enterprise Design Thinking. 
    Recuperado de <a href="https://www.ibm.com/design/thinking/page/toolkit/activity/empathy-map">https://www.ibm.com/design/thinking/page/toolkit/activity/empathy-map</a>
  </li>
  <li>
    IBM Design. (s.f.). <em>As-is Scenario Map</em>. Enterprise Design Thinking. 
    Recuperado de <a href="https://www.ibm.com/design/thinking/page/toolkit/activity/as-is-scenario-map">https://www.ibm.com/design/thinking/page/toolkit/activity/as-is-scenario-map</a>
  </li>
  <li>
    Martin, R. C. (2017). <em>Clean Architecture: A Craftsman's Guide to Software Structure and Design</em>. Prentice Hall.
    Recuperado de <a href="https://www.oreilly.com/library/view/clean-architecture-a/9780134494272/">https://www.oreilly.com/library/view/clean-architecture-a/9780134494272/</a>
  </li>
  <li>
    Mendel, J. (s.f.). <em>Seriously, what's your (startup's) problem?</em>. Medium. 
    Recuperado de <a href="https://medium.com/@jakemendel/seriously-whats-your-startup-s-problem-b3a884c54ab4">https://medium.com/@jakemendel/seriously-whats-your-startup-s-problem-b3a884c54ab4</a>
  </li>
  <li>
    Nielsen Norman Group. (1994). <em>10 Usability Heuristics for User Interface Design</em>. 
    Recuperado de <a href="https://www.nngroup.com/articles/ten-usability-heuristics/">https://www.nngroup.com/articles/ten-usability-heuristics/</a>
  </li>
  <li>
    Nielsen Norman Group. (2016). <em>The Four Dimensions of Tone of Voice</em>. 
    Recuperado de <a href="https://www.nngroup.com/articles/tone-of-voice-dimensions/">https://www.nngroup.com/articles/tone-of-voice-dimensions/</a>
  </li>
  <li>
    Preston-Werner, T. (s.f.). <em>Semantic Versioning 2.0.0</em>. 
    Recuperado de <a href="https://semver.org/">https://semver.org/</a>
  </li>
  <li>
    Progressa Lean. (s.f.). <em>5W+2H - Técnica de análisis de problemas</em>. 
    Recuperado de <a href="https://www.progressalean.com/5w2h-tecnica-de-analisis-de-problemas/">https://www.progressalean.com/5w2h-tecnica-de-analisis-de-problemas/</a>
  </li>
  <li>
    Refactoring.Guru. (s.f.). <em>Design Patterns</em>. 
    Recuperado de <a href="https://refactoring.guru/es/design-patterns">https://refactoring.guru/es/design-patterns</a>
  </li>
  <li>
    Spring. (s.f.). <em>Spring Boot Reference Documentation</em>. 
    Recuperado de <a href="https://docs.spring.io/spring-boot/docs/current/reference/html/">https://docs.spring.io/spring-boot/docs/current/reference/html/</a>
  </li>
  <li>
    UXPressia. (s.f.). <em>User vs. Buyer Persona: Differences and free template</em>. 
    Recuperado de <a href="https://uxpressia.com/blog/user-persona-vs-buyer-persona-difference">https://uxpressia.com/blog/user-persona-vs-buyer-persona-difference</a>
  </li>
  <li>
    Vernon, V. (2016). <em>Domain-Driven Design Distilled</em>. Addison-Wesley Professional.
    Recuperado de <a href="https://www.oreilly.com/library/view/domain-driven-design-distilled/9780134434964/">https://www.oreilly.com/library/view/domain-driven-design-distilled/9780134434964/</a>
  </li>
  <li>
    Vernon, V. (s.f.). <em>Domain-Driven Design Reference</em>. 
    Recuperado de <a href="https://domainlanguage.com/ddd/reference/">https://domainlanguage.com/ddd/reference/</a>
  </li>
</ul>

<div style="page-break-after: always;"></div>

## Anexos

<h4>Anexo A: Enlaces de Despliegue y Repositorios</h4>

<p>A continuación se listan los enlaces a los entornos de producción y los repositorios de código fuente utilizados durante todo el ciclo de vida del proyecto.</p>

<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <th>Recurso</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Landing Page (GitHub Pages)</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>Frontend Web Application (Vercel Prod)</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>Backend API Services (Azure Prod)</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>API Documentation (Swagger UI)</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>Repositorio Landing Page</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>Repositorio Frontend</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>Repositorio Backend</strong></td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td><strong>Repositorio Project Report</strong></td>
      <td><a href=""></a></td>
    </tr>
  </tbody>
</table>

<h4>Anexo B: Videos de Exposiciones</h4>

<p>Registro histórico de todas las exposiciones y videos promocionales presentados durante el ciclo académico 202520.</p>

<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <th>Entrega / Hito</th>
      <th>Plataforma</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2"><strong>Video de Exposición TB1 (Sprint 1)</strong></td>
      <td>YouTube</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td>Microsoft Stream</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>Video de Exposición TP1 (Sprint 2)</strong></td>
      <td>YouTube</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td>Microsoft Stream</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>Video de Exposición TB2 (Sprint 3)</strong></td>
      <td>YouTube</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td>Microsoft Stream</td>
      <td><a href="#"></a></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>Video de Exposición Final TF1 (Sprint 4)</strong></td>
      <td>YouTube</td>
      <td><a href="#"></a></td>
    </tr>
    <tr>
      <td>Microsoft Stream</td>
      <td><a href="#"></a></td>
    </tr>
  </tbody>
</table>

<h4>Anexo C: Videos del Proyecto</h4>

<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <td rowspan="2"><strong>Video "About the Product"</strong></td>
      <td>YouTube</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td>Microsoft Stream</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>Video "About the Team"</strong></td>
      <td>YouTube</td>
      <td><a href=""></a></td>
    </tr>
    <tr>
      <td>Microsoft Stream</td>
      <td><a href=""></a></td>
    </tr>
  </tbody>
</table>

</body>
</html>
