# Requirements Specification
<a id="3-requirements-specification"></a>
## 3.1. User Stories
<a id="3-1-user-stories"></a>

## 1. Landing Page (Presentación y Conversión)

| ID | Título | Descripción | Criterios de Aceptación | Relacionado con |
| :--- | :--- | :--- | :--- | :--- |
| US01 | Autenticación | **Como** usuario de EcoRoad, **quiero** poder iniciar sesión **para** acceder a mi cuenta y perfil | **Dado** que el usuario ingresa credenciales, **cuando** son válidas, **entonces** se redirige al dashboard. | EP08: Usuario |
| US02 | Demo de Tablero Geolocalizado | **Como** responsable de gestión ambiental, **quiero** ver una vista previa del mapa de indicadores **para** entender cómo se visualizaría mi obra. | **Dado** que el usuario navega la landing, **cuando** llega a la sección "Funciones", **entonces** observa un mapa demo con puntos de monitoreo simulados. | EP05: Mapa |
| US03 | Explicación de planes | **Como** gerente de cartera de proyectos **quiero** comparar los planes Base, Profesional y Enterprise **para** elegir el que se ajuste a mi empresa. | **Dado** que el usuario llega a la sección "Planes", **cuando** la visualiza, **entonces** se muestra una tabla comparativa de funcionalidades por plan. | EP09: Suscripción |
| US04 | CTA Segmento Consultora | **Como** responsable de gestión ambiental **quiero** un botón claro para probar la plataforma, **para** evaluar si resuelve mi problema de monitoreo. | **Dado** que el usuario está en la sección dirigida a consultoras, **cuando** hace clic en "Monitorea tu proyecto", **entonces** es redirigido al registro/login de la Web App. | EP08: Usuario |
| US05 | CTA Segmento Empresa Multi-Proyecto | **Como** gerente de cartera de proyectos **quiero** un botón dirigido a gestión multi-proyecto **para** acceder a la vista que necesito. | **Dado** que el usuario está en la sección dirigida a empresas con múltiples proyectos, **cuando** hace clic en "Gestiona tu cartera", **entonces** es redirigido al dashboard multiproyecto después de haber sido logeado. | EP06: Dashboard |
| US06 | Caso de Uso / Testimonio | **Como** usuario de EcoRoad **quiero** ver un caso de éxito o cifra de impacto **para** confiar en la efectividad de la plataforma. | **Dado** que el usuario hace scroll en la landing, **cuando** llega a la sección de impacto, **entonces** ve métricas ilustrativas. | EP07: Reporte |
| US07 | Notificaciones Push Landing | **Como** usuario de EcoRoad **quiero** aceptar notificaciones del navegador **para** recibir alertas de incumplimientos sin ingresar a la plataforma. | **Dado** que el usuario entra al sitio, **cuando** aparece el prompt de permiso, **entonces** el sistema registra la suscripción push. | EP03: Alerta |
| US08 | Formulario de Contacto Comercial | **Como** gerente de cartera de proyectos **quiero** dejar mis datos de contacto **para** que ventas me contacte con una propuesta personalizada. | **Dado** que el usuario completa el formulario, **cuando** lo envía, **entonces** se registra el lead y se muestra confirmación. | EP09: Suscripción |

---

## 2. Web Application (Frontend Interactivo)

| ID | Título | Descripción | Criterios de Aceptación | Relacionado con |
| :--- | :--- | :--- | :--- | :--- |
| US09 | Formulario de Registro de Indicador | **Como** responsable de gestión ambiental **quiero** llenar un formulario validado **para** registrar mediciones sin enviar errores al servidor. | **Dado** que un campo numérico es obligatorio, **cuando** se deja vacío o fuera de rango, **entonces** el botón "Guardar" se deshabilita. | EP02: Indicador |
| US10 | Tarjetas de Proyecto (Cards) | **Como** usuario de EcoRoad **quiero** ver tarjetas visuales de cada proyecto **para** entender su estado ambiental de un vistazo. | **Dado** que se carga el portafolio, **cuando** llegan los datos, **entonces** se renderiza una Card por proyecto con semáforo de estado (verde/amarillo/rojo). | EP06: Dashboard |
| US11 | Tablero Kanban de Incidencias | **Como** responsable de gestión ambiental, **quiero** mover incidencias entre columnas (Abierta/En revisión/Resuelta) **para** gestionar mi flujo visualmente. | **Dado** que se arrastra una incidencia, **cuando** se suelta en otra columna, **entonces** el estado cambia y se persiste. | EP04: Incidencia |
| US12 | Vista de Mapa Interactivo | **Como** responsable de gestión ambiental **quiero** ver un mapa con pines de colores por punto de monitoreo **para** identificar zonas críticas rápidamente. | **Dado** que se cargan los puntos del proyecto, **cuando** el mapa renderiza, **entonces** cada pin muestra color según nivel de riesgo del indicador. | EP05: Mapa |
| US13 | Filtro por Tipo de Indicador | **Como** responsable de gestión ambiental **quiero** filtrar el mapa/dashboard por tipo de indicador (aire, ruido, agua) **para** enfocar mi revisión. | **Dado** que hay indicadores de varios tipos, **cuando** se selecciona un filtro, **entonces** la vista se actualiza al instante. | EP02: Indicador |
| US14 | Adjuntar Evidencia Fotográfica | **Como** responsable de gestión ambiental **quiero** arrastrar fotos al navegador **para** adjuntarlas como evidencia de una medición. | **Dado** que el archivo está en el dispositivo, **cuando** se suelta o selecciona, **entonces** inicia la barra de progreso de subida. | EP10: Documento |
| US15 | Barra de Progreso de Cumplimiento | **Como** jefe de proyecto, **quiero** ver una barra de progreso del % de indicadores dentro de norma **para** medir el avance rápidamente. | **Dado** que se actualizan indicadores, **cuando** cambia el estado, **entonces** la barra se recalcula. | EP06: Dashboard |
| US16 | Feed de Comentarios en Incidencia | **Como** usuario de EcoRoad **quiero** ver el historial de comentarios de una incidencia **para** entender el contexto de su seguimiento. | **Dado** que hay mensajes previos, **cuando** se abre la incidencia, **entonces** se visualizan en formato de burbujas de texto con fecha y autor. | EP04: Incidencia |
| US17 | Alertas y Notificaciones | **Como** usuario de EcoRoad **quiero** un icono de notificaciones **para** ver alertas de incumplimientos recientes. | **Dado** que llega una nueva alerta, **cuando** el usuario ve el header, **entonces** la campana muestra un punto rojo con el conteo. | EP03: Alerta |
| US18 | Tabla de Incidencias Críticas | **Como** gerente de cartera de proyectos **quiero** una tabla con filas resaltadas **para** identificar las incidencias críticas de un vistazo. | **Dado** que la severidad es alta, **cuando** se renderiza la fila, **entonces** el fondo se pinta de rojo. | EP04: Incidencia |
| US19 | Selector de Rango de Fechas | **Como** usuario de EcoRoad, **quiero** elegir un rango de fechas **para** revisar el histórico de mediciones de un periodo específico. | **Dado** que se abre el selector, **cuando** se elige un rango, **entonces** el dashboard filtra los datos a ese periodo. | EP06: Dashboard |
| US20 | Edición Visual de Punto de Monitoreo | **Como** responsable de gestión ambiental **quiero** un botón de editar en cada punto de monitoreo **para** corregir su ubicación o umbral normativo. | **Dado** que el usuario presiona "Editar", **cuando** guarda, **entonces** la UI se actualiza sin recargar la página. | EP02: Indicador |
| US21 | Login Minimalista | **Como** usuario de EcoRoad **quiero** una interfaz de login minimalista **para** reducir la fricción al entrar a la plataforma. | **Dado** que el usuario carga la URL, **cuando** no hay sesión activa, **entonces** ve un login centrado y limpio. | EP08: Usuario |
| US22 | Vista de Lista de Proyectos | **Como** gerente de cartera de proyectos **quiero** una vista de lista compacta **para** ver más proyectos en una sola pantalla. | **Dado** que el usuario cambia la vista, **cuando** se activa "Lista", **entonces** las tarjetas se convierten en filas. | EP01: Proyecto |
| US23 | Selector de Color de Marca | **Como** administrador de cuenta Enterprise, **quiero** elegir el color corporativo **para** que el dashboard refleje la identidad de mi empresa. | **Dado** que se abre configuración, **cuando** se elige un color, **entonces** los elementos de UI cambian de tono. | EP09: Suscripción |

---

## 3. RESTful API (Backend & Lógica de Negocio)

| ID | Título | Descripción | Criterios de Aceptación | Relacionado con |
|---|---|---|---|---|
| US24 | Auth JWT | **Como** Backend, **quiero** generar tokens JWT **para** asegurar todas las peticiones a la API. | **Dado** que el login es exitoso, **cuando** se responde, **entonces** se incluye un Bearer token válido. | EP11: API |
| US25 | Swagger / Documentación | **Como** Frontend, **quiero** ver la documentación de la API **para** integrarme de forma autónoma. | **Dado** que el servidor corre, **cuando** se accede a /swagger, **entonces** se muestran los modelos y endpoints disponibles. | EP11: API |
| US26 | CRUD Proyectos API | **Como** Dev, **quiero** endpoints GET/POST/PUT/DELETE **para** la persistencia de proyectos viales. | **Dado** que se llama al endpoint, **cuando** el método es válido, **entonces** devuelve JSON con status 200/201. | EP01: Proyecto |
| US27 | Endpoint de Registro de Indicador | **Como** Dev, **quiero** un endpoint POST **para** recibir mediciones ambientales de campo y persistirlas. | **Dado** que llega el JSON de medición, **cuando** cumple el esquema, **entonces** se guarda en base de datos con timestamp. | EP02: Indicador |
| US28 | Motor de Comparación Normativa | **Como** API, **quiero** comparar cada medición contra el límite normativo correspondiente **para** determinar si hay incumplimiento. | **Dado** que se registra un indicador, **cuando** su valor supera el límite configurado, **entonces** se marca como "incumplimiento". | EP03: Alerta |
| US29 | Generador Automático de Incidencia | **Como** motor de reglas, **quiero** crear automáticamente un ticket de incidencia ante un incumplimiento detectado. | **Dado** que un indicador se marca como incumplimiento, **cuando** se procesa, **entonces** se crea una incidencia vinculada al proyecto y punto de monitoreo. | EP04: Incidencia |
| US30 | API de Subida de Evidencias | **Como** Dev, **quiero** un endpoint multipart **para** subir archivos binarios (fotos/documentos) a almacenamiento en la nube. | **Dado** que se envía un binario, **cuando** se procesa correctamente, **entonces** devuelve una URL de acceso. | EP10: Documento |
| US31 | Paginación de Resultados | **Como** Frontend, **quiero** resultados paginados en los listados de indicadores/incidencias **para** optimizar el rendimiento. | **Dado** que hay muchos registros, **cuando** se solicita `size=10`, **entonces** se devuelve solo esa página. | EP11: API |
| US32 | Cifrado de Contraseñas | **Como** administrador del sistema, **quiero** cifrar contraseñas con BCrypt **para** proteger los datos de los usuarios. | **Dado** que se crea un usuario, **cuando** se guarda, **entonces** se almacena el hash del password, no el texto plano. | EP08: Usuario |
| US33 | Cálculo de Salud Ambiental del Proyecto | **Como** API, **quiero** calcular el % de indicadores fuera de norma **para** determinar el color de semáforo del proyecto. | **Dado** que se solicita el estado de salud, **cuando** incumplimientos > umbral definido, **entonces** devuelve estado "ROJO". | EP06: Dashboard |
| US34 | Tarea Programada de Revisión de Vencimientos | **Como** proceso de fondo, **quiero** identificar incidencias sin resolución en X días **para** escalar su prioridad. | **Dado** que es medianoche, **cuando** corre la tarea, **entonces** marca incidencias vencidas y dispara notificación. | EP03: Alerta |
| US35 | Generador de JSON para Reporte de Auditoría | **Como** API, **quiero** estructurar un JSON con histórico de indicadores e incidencias **para** alimentar el motor de generación de PDF. | **Dado** que se pide un reporte, **cuando** se genera, **entonces** incluye datos agregados por punto de monitoreo y periodo. | EP07: Reporte |
| US36 | Endpoint de Exportación a PDF | **Como** backend, **quiero** generar la descarga de un PDF de auditoría **para** que el usuario lo presente ante el ente fiscalizador. | **Dado** que se solicita el reporte, **cuando** el sistema procesa los datos, **entonces** retorna un archivo PDF descargable. | EP07: Reporte |
| US37 | Limitación de Peticiones (Rate Limiting) | **Como** Admin, **quiero** limitar peticiones por IP **para** evitar ataques de denegación de servicio. | **Dado** que una IP supera el límite configurado, **cuando** hace una nueva petición, **entonces** devuelve status 429. | EP11: API |
| US38 | Validación de Umbral por Tipo de Norma | **Como** API, **quiero** permitir configurar distintos límites normativos según el tipo de zona/proyecto **para** adaptarse a la regulación vigente. | **Dado** que se registra un nuevo proyecto, **cuando** se define su ubicación/tipo, **entonces** se asignan los límites normativos correspondientes. | EP01: Proyecto |
| US39 | Gestión de Planes de Suscripción (API) | **Como** API, **quiero** validar el plan activo del cliente **para** restringir el número de proyectos/usuarios permitidos. | **Dado** que un cliente intenta crear un proyecto adicional, **cuando** excede el límite de su plan, **entonces** devuelve error 403 con mensaje de upgrade. | EP09: Suscripción |

---

## 4. Requerimientos de Negocio Compartidos (Fullstack)

| ID | Título | Descripción | Criterios de Aceptación | Relacionado con |
|---|---|---|---|---|
| US40 | Creación de Proyecto Vial | **Como** jefe de gestión ambiental, **quiero** crear un proyecto asignando ubicación y fechas **para** tener su registro en la plataforma. | **Dado** que los datos son válidos, **cuando** se guarda, **entonces** el proyecto aparece en el portafolio y en el mapa. | EP01: Proyecto |
| US41 | Registro de Punto de Monitoreo | **Como** supervisor de obra, **quiero** registrar puntos de monitoreo geolocalizados dentro de un proyecto **para** estructurar la toma de mediciones. | **Dado** que se crea un proyecto, **cuando** se agrega un punto con coordenadas, **entonces** queda disponible para el registro de indicadores. | EP02: Indicador |
| US42 | Asignación de Responsable por Proyecto | **Como** PMO/Gerente, **quiero** asignar un responsable ambiental a cada proyecto **para** dar claridad de accountability. | **Dado** que se crea el proyecto, **cuando** se asigna un usuario, **entonces** este recibe notificación de asignación. | EP08: Usuario |
| US43 | Comentarios en Incidencia | **Como** usuario, **quiero** dejar comentarios en una incidencia **para** mantener la comunicación fluida entre campo y oficina. | **Dado** que se visualiza una incidencia, **cuando** se envía un mensaje, **entonces** se guarda con fecha y autor. | EP04: Incidencia |
| US44 | Salud Ambiental del Portafolio | **Como** gerente de cartera, **quiero** ver un gráfico de salud ambiental de todos mis proyectos **para** tomar decisiones preventivas. | **Dado** que hay incumplimientos, **cuando** se abre el dashboard multi-proyecto, **entonces** el indicador general cambia a Rojo/Ámbar. | EP06: Dashboard |
| US45 | Reporte de Auditoría por Proyecto | **Como** consultora ambiental, **quiero** generar un reporte PDF por proyecto **para** presentarlo ante fiscalización. | **Dado** que se elige exportar, **cuando** el sistema procesa, **entonces** descarga el reporte con histórico e incidencias. | EP07: Reporte |
| US46 | Alerta de Incumplimiento Inminente | **Como** responsable ambiental, **quiero** recibir una alerta cuando un indicador se acerque al límite normativo, no solo cuando lo supere **para** actuar preventivamente. | **Dado** que el valor está dentro del rango de advertencia (ej. 90% del límite), **cuando** se registra, **entonces** se dispara una alerta preventiva. | EP03: Alerta |
| US47 | Alerta de Incidencia sin Atender | **Como** jefe de gestión ambiental, **quiero** recibir alerta si una incidencia no tiene seguimiento en 3 días **para** intervenir a tiempo. | **Dado** que no hay actividad registrada en 72h, **cuando** el sistema valida, **entonces** marca la incidencia como "estancada" y notifica. | EP03: Alerta |
| US48 | Eliminación/Archivo de Proyecto | **Como** PMO Lead, **quiero** archivar proyectos finalizados **para** mantener organizado el portafolio activo. | **Dado** que se confirma archivar, **cuando** se ejecuta, **entonces** el proyecto desaparece de la vista activa pero conserva su histórico. | EP01: Proyecto |
| US49 | Seguimiento de Indicadores por Proyecto | **Como** PM, **quiero** monitorear el estado histórico de los indicadores de un proyecto **para** ver su evolución en el tiempo. | **Dado** que se accede al panel del proyecto, **cuando** se filtran por tipo, **entonces** se muestra la tendencia en el tiempo. | EP02: Indicador |
| US50 | Visualización de KPIs Ambientales | **Como** Stakeholder, **quiero** ver indicadores clave (% cumplimiento, incidencias abiertas, tiempo promedio de resolución) **para** evaluar el desempeño. | **Dado** que el dashboard está activo, **cuando** se consulta, **entonces** muestra los KPIs actualizados. | EP06: Dashboard |
| US51 | Actualización en Tiempo Real del Dashboard | **Como** usuario, **quiero** que el dashboard se actualice solo al registrarse una nueva medición **para** tener datos confiables sin recargar. | **Dado** que hay un cambio en la base de datos, **cuando** ocurre, **entonces** la interfaz refleja el cambio automáticamente. | EP06: Dashboard |
| US52 | Historial de Estados de Incidencia | **Como** Stakeholder, **quiero** ver el historial de cambios de una incidencia **para** entender su evolución completa. | **Dado** que se consulta la bitácora, **cuando** se despliega, **entonces** muestra autor, fecha y estado anterior/nuevo. | EP04: Incidencia |
| US53 | Roles y Permisos | **Como** administrador de cuenta, **quiero** asignar roles (Admin, Supervisor, Lector) **para** proteger la información sensible del proyecto. | **Dado** que se invita a un usuario, **cuando** se le asigna un rol, **entonces** se limitan sus acciones según el rol. | EP08: Usuario |
| US54 | Control de Versiones de Documento Normativo | **Como** consultor ambiental, **quiero** conservar el historial de versiones de instrumentos de gestión ambiental subidos **para** no perder revisiones anteriores. | **Dado** que se sube un archivo con el mismo nombre, **cuando** se detecta duplicado, **entonces** se crea una nueva versión sin sobrescribir. | EP10: Documento |
| US55 | Búsqueda Global de Proyectos/Incidencias | **Como** Líder, **quiero** buscar proyectos o incidencias por nombre/código **para** ahorrar tiempo localizando información. | **Dado** que se ingresa un término, **cuando** se busca, **entonces** lista resultados relevantes de todo el sistema. | EP01: Proyecto |
| US56 | Documentos Obligatorios por Hito Normativo | **Como** consultora ambiental, **quiero** marcar qué documentos son indispensables para un hito de auditoría, **para** estandarizar el proceso. | **Dado** que se define el hito, **cuando** se marca como "Requerido", **entonces** bloquea el cierre del hito si el documento falta. | EP10: Documento |
| US57 | Upgrade/Downgrade de Plan | **Como** cliente, **quiero** cambiar mi plan de suscripción **para** ajustarlo a mi cantidad real de proyectos activos. | **Dado** que el usuario solicita cambio de plan, **cuando** se confirma, **entonces** se actualizan los límites y el ciclo de facturación. | EP09: Suscripción |


---

### 3.2. Impact Mapping
<a id="3-2-impact-mapping"></a>

En esta sección se presenta el desglose estratégico del modelo de negocio de EcoRoad mediante la técnica de **Impact Mapping**, vinculando la meta de negocio SMART con los cambios de comportamiento requeridos en los segmentos de cliente, las soluciones funcionales provistas y las historias de usuario asociadas.

<p align="center">
  <img src="../assets/Chapter-3/Impact_map.png" alt="Impact Mapping Consolidado - EcoRoad" width="100%"/>
</p>

### 3.3. Product Backlog
<a id="3-3-product-backlog"></a>

| # Orden | User Story Id | Título | Descripción | Story Points (1/2/3/5/8) |
|---|---|---|---|---|
| 1 | US21 | Login Minimalista | Como usuario de EcoRoad, quiero una interfaz de login minimalista para reducir la fricción al entrar a la plataforma. | 2 |
| 2 | US24 | Auth JWT | Como Backend, quiero generar tokens JWT para asegurar todas las peticiones a la API. | 5 |
| 3 | US32 | Cifrado de Contraseñas | Como administrador del sistema, quiero cifrar contraseñas con BCrypt para proteger los datos de los usuarios. | 3 |
| 4 | US01 | Autenticación | Como usuario de EcoRoad, quiero poder iniciar sesión para acceder a mi cuenta y perfil. | 2 |
| 5 | US53 | Roles y Permisos | Como administrador de cuenta, quiero asignar roles (Admin, Supervisor, Lector) para proteger la información sensible del proyecto. | 8 |
| 6 | US40 | Creación de Proyecto Vial | Como jefe de gestión ambiental, quiero crear un proyecto asignando ubicación y fechas para tener su registro en la plataforma. | 3 |
| 7 | US26 | CRUD Proyectos API | Como Dev, quiero endpoints GET/POST/PUT/DELETE para la persistencia de proyectos viales. | 5 |
| 8 | US25 | Swagger / Documentación | Como Frontend, quiero ver la documentación de la API para integrarme de forma autónoma. | 2 |
| 9 | US38 | Validación de Umbral por Tipo de Norma | Como API, quiero permitir configurar distintos límites normativos según el tipo de zona/proyecto para adaptarse a la regulación vigente. | 5 |
| 10 | US42 | Asignación de Responsable por Proyecto | Como PMO/Gerente, quiero asignar un responsable ambiental a cada proyecto para dar claridad de accountability. | 3 |
| 11 | US41 | Registro de Punto de Monitoreo | Como supervisor de obra, quiero registrar puntos de monitoreo geolocalizados dentro de un proyecto para estructurar la toma de mediciones. | 5 |
| 12 | US20 | Edición Visual de Punto de Monitoreo | Como responsable de gestión ambiental, quiero un botón de editar en cada punto de monitoreo para corregir su ubicación o umbral normativo. | 2 |
| 13 | US22 | Vista de Lista de Proyectos | Como gerente de cartera de proyectos, quiero una vista de lista compacta para ver más proyectos en una sola pantalla. | 2 |
| 14 | US48 | Eliminación/Archivo de Proyecto | Como PMO Lead, quiero archivar proyectos finalizados para mantener organizado el portafolio activo. | 3 |
| 15 | US10 | Tarjetas de Proyecto (Cards) | Como usuario de EcoRoad, quiero ver tarjetas visuales de cada proyecto para entender su estado ambiental de un vistazo. | 3 |
| 16 | US51 | Actualización en Tiempo Real del Dashboard | Como usuario, quiero que el dashboard se actualice solo al registrarse una nueva medición para tener datos confiables sin recargar. | 8 |
| 17 | US27 | Endpoint de Registro de Indicador | Como Dev, quiero un endpoint POST para recibir mediciones ambientales de campo y persistirlas. | 5 |
| 18 | US09 | Formulario de Registro de Indicador | Como responsable de gestión ambiental, quiero llenar un formulario validado para registrar mediciones sin enviar errores al servidor. | 3 |
| 19 | US13 | Filtro por Tipo de Indicador | Como responsable de gestión ambiental, quiero filtrar el mapa/dashboard por tipo de indicador (aire, ruido, agua) para enfocar mi revisión. | 2 |
| 20 | US49 | Seguimiento de Indicadores por Proyecto | Como PM, quiero monitorear el estado histórico de los indicadores de un proyecto para ver su evolución en el tiempo. | 5 |
| 21 | US19 | Selector de Rango de Fechas | Como usuario de EcoRoad, quiero elegir un rango de fechas para revisar el histórico de mediciones de un periodo específico. | 3 |
| 22 | US28 | Motor de Comparación Normativa | Como API, quiero comparar cada medición contra el límite normativo correspondiente para determinar si hay incumplimiento. | 8 |
| 23 | US29 | Generador Automático de Incidencia | Como motor de reglas, quiero crear automáticamente un ticket de incidencia ante un incumplimiento detectado. | 5 |
| 24 | US46 | Alerta de Incumplimiento Inminente | Como responsable ambiental, quiero recibir una alerta cuando un indicador se acerque al límite normativo, no solo cuando lo supere. | 5 |
| 25 | US34 | Tarea Programada de Revisión de Vencimientos | Como proceso de fondo, quiero identificar incidencias sin resolución en X días para escalar su prioridad. | 3 |
| 26 | US47 | Alerta de Incidencia sin Atender | Como jefe de gestión ambiental, quiero recibir alerta si una incidencia no tiene seguimiento en 3 días para intervenir a tiempo. | 3 |
| 27 | US17 | Alertas y Notificaciones | Como usuario de EcoRoad, quiero un icono de notificaciones para ver alertas de incumplimientos recientes. | 2 |
| 28 | US11 | Tablero Kanban de Incidencias | Como responsable de gestión ambiental, quiero mover incidencias entre columnas (Abierta/En revisión/Resuelta) para gestionar mi flujo visualmente. | 8 |
| 29 | US18 | Tabla de Incidencias Críticas | Como gerente de cartera de proyectos, quiero una tabla con filas resaltadas para identificar las incidencias críticas de un vistazo. | 2 |
| 30 | US43 | Comentarios en Incidencia | Como usuario, quiero dejar comentarios en una incidencia para mantener la comunicación fluida entre campo y oficina. | 3 |
| 31 | US16 | Feed de Comentarios en Incidencia | Como usuario de EcoRoad, quiero ver el historial de comentarios de una incidencia para entender el contexto de su seguimiento. | 3 |
| 32 | US52 | Historial de Estados de Incidencia | Como Stakeholder, quiero ver el historial de cambios de una incidencia para entender su evolución completa. | 3 |
| 33 | US14 | Adjuntar Evidencia Fotográfica | Como responsable de gestión ambiental, quiero arrastrar fotos al navegador para adjuntarlas como evidencia de una medición. | 3 |
| 34 | US30 | API de Subida de Evidencias | Como Dev, quiero un endpoint multipart para subir archivos binarios (fotos/documentos) a almacenamiento en la nube. | 5 |
| 35 | US54 | Control de Versiones de Documento Normativo | Como consultor ambiental, quiero conservar el historial de versiones de instrumentos de gestión ambiental subidos para no perder revisiones anteriores. | 8 |
| 36 | US56 | Documentos Obligatorios por Hito Normativo | Como consultora ambiental, quiero marcar qué documentos son indispensables para un hito de auditoría, para estandarizar el proceso. | 3 |
| 37 | US55 | Búsqueda Global de Proyectos/Incidencias | Como Líder, quiero buscar proyectos o incidencias por nombre/código para ahorrar tiempo localizando información. | 5 |
| 38 | US12 | Vista de Mapa Interactivo | Como responsable de gestión ambiental, quiero ver un mapa con pines de colores por punto de monitoreo para identificar zonas críticas rápidamente. | 8 |
| 39 | US02 | Demo de Tablero Geolocalizado (Landing) | Como responsable de gestión ambiental, quiero ver una vista previa del mapa de indicadores para entender cómo se visualizaría mi obra. | 3 |
| 40 | US33 | Cálculo de Salud Ambiental del Proyecto | Como API, quiero calcular el % de indicadores fuera de norma para determinar el color de semáforo del proyecto. | 3 |
| 41 | US15 | Barra de Progreso de Cumplimiento | Como jefe de proyecto, quiero ver una barra de progreso del % de indicadores dentro de norma para medir el avance rápidamente. | 2 |
| 42 | US44 | Salud Ambiental del Portafolio | Como gerente de cartera, quiero ver un gráfico de salud ambiental de todos mis proyectos para tomar decisiones preventivas. | 5 |
| 43 | US50 | Visualización de KPIs Ambientales | Como Stakeholder, quiero ver indicadores clave (% cumplimiento, incidencias abiertas, tiempo promedio de resolución) para evaluar el desempeño. | 5 |
| 44 | US05 | CTA Segmento Empresa Multi-Proyecto (Landing) | Como gerente de cartera de proyectos, quiero un botón dirigido a gestión multi-proyecto para acceder a la vista que necesito. | 2 |
| 45 | US35 | Generador de JSON para Reporte de Auditoría | Como API, quiero estructurar un JSON con histórico de indicadores e incidencias para alimentar el motor de generación de PDF. | 5 |
| 46 | US36 | Endpoint de Exportación a PDF | Como backend, quiero generar la descarga de un PDF de auditoría para que el usuario lo presente ante el ente fiscalizador. | 5 |
| 47 | US45 | Reporte de Auditoría por Proyecto | Como consultora ambiental, quiero generar un reporte PDF por proyecto para presentarlo ante fiscalización. | 3 |
| 48 | US06 | Caso de Uso / Testimonio (Landing) | Como usuario de EcoRoad, quiero ver un caso de éxito o cifra de impacto para confiar en la efectividad de la plataforma. | 2 |
| 49 | US04 | CTA Segmento Consultora (Landing) | Como responsable de gestión ambiental, quiero un botón claro para probar la plataforma, para evaluar si resuelve mi problema de monitoreo. | 2 |
| 50 | US03 | Explicación de Planes (Landing) | Como gerente de cartera de proyectos, quiero comparar los planes Base, Profesional y Enterprise para elegir el que se ajuste a mi empresa. | 3 |
| 51 | US08 | Formulario de Contacto Comercial (Landing) | Como gerente de cartera de proyectos, quiero dejar mis datos de contacto para que ventas me contacte con una propuesta personalizada. | 2 |
| 52 | US39 | Gestión de Planes de Suscripción (API) | Como API, quiero validar el plan activo del cliente para restringir el número de proyectos/usuarios permitidos. | 5 |
| 53 | US57 | Upgrade/Downgrade de Plan | Como cliente, quiero cambiar mi plan de suscripción para ajustarlo a mi cantidad real de proyectos activos. | 5 |
| 54 | US23 | Selector de Color de Marca | Como administrador de cuenta Enterprise, quiero elegir el color corporativo para que el dashboard refleje la identidad de mi empresa. | 5 |
| 55 | US07 | Notificaciones Push Landing | Como usuario de EcoRoad, quiero aceptar notificaciones del navegador para recibir alertas de incumplimientos sin ingresar a la plataforma. | 5 |
| 56 | US31 | Paginación de Resultados | Como Frontend, quiero resultados paginados en los listados de indicadores/incidencias para optimizar el rendimiento. | 3 |
| 57 | US37 | Limitación de Peticiones (Rate Limiting) | Como Admin, quiero limitar peticiones por IP para evitar ataques de denegación de servicio. | 5 |
