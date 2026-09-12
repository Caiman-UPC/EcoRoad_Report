# Capítulo 1

## Introducción

El presente proyecto tiene como finalidad el diseño, desarrollo e implementación de una solución **HaaS/SaaS** (Hardware as a Service + Software as a Service), compuesta por un RESTful API de elaboración interna y una Web Application integrada con dicho API, con el objetivo de resolver problemáticas reales del sector de infraestructura vial en el ámbito de la gestión y el cumplimiento ambiental. Esta solución se construye bajo un enfoque de ingeniería de software moderna, incorporando metodologías ágiles, diseño centrado en el usuario (Lean UX) y una arquitectura orientada a servicios.

En el contexto actual, las empresas constructoras y las consultoras/supervisoras ambientales que participan en proyectos viales enfrentan desafíos relacionados con el registro, procesamiento y control en tiempo real de indicadores ambientales (aire, ruido, agua), especialmente en obras donde aún predominan procesos manuales, semi-digitalizados o dependientes de reportes que pueden ser alterados o entregados fuera de tiempo. Estas limitaciones generan retrasos en la detección de incumplimientos normativos, mayor exposición a sanciones, procesos de auditoría lentos y costosos, y una desconfianza estructural entre quien ejecuta la obra y quien la fiscaliza.

Frente a este escenario, el presente proyecto propone el desarrollo de **EcoRoad**, un ecosistema digital que centraliza —mediante una red propia de sensores IoT— el registro de indicadores ambientales, automatiza la detección de incumplimientos normativos mediante un motor de alertas preventivas, y visualiza en tiempo real el estado ambiental de múltiples proyectos viales, contribuyendo a la mejora de la eficiencia operativa de las constructoras y a la reducción del riesgo regulatorio y de esfuerzo de fiscalización de las supervisoras ambientales.

## 1.1 Startup Profile

La presente sección describe el contexto general de la startup responsable del desarrollo de la solución propuesta. Se presenta una visión general de la organización, su enfoque tecnológico y propuesta de valor, así como la caracterización de los integrantes del equipo, destacando sus perfiles y roles dentro del proyecto.

### 1.1.1 Descripción de la Startup

**Kaimán** es una startup tecnológica enfocada en el desarrollo de soluciones digitales bajo un modelo híbrido **HaaS/SaaS**, orientadas a la gestión y el cumplimiento ambiental en el sector de infraestructura vial. Su propuesta de valor se centra en transformar el registro manual, disperso y potencialmente manipulable de datos ambientales en un ecosistema automatizado en tiempo real, alimentado por una red propia de sensores IoT, accesible, escalable y adaptable a distintos tamaños de operación empresarial.

El nombre **Kaimán** hace alusión al caimán como especie bioindicadora: su presencia y bienestar reflejan el equilibrio ambiental del ecosistema que habita, de la misma manera en que la plataforma desarrollada por la startup busca reflejar, en tiempo real y con datos inalterables, el estado de salud ambiental de cada proyecto vial que monitorea, actuando como un observador neutral entre las partes.

El modelo de negocio de Kaimán es inherentemente escalable y de **doble ingreso (dual revenue)**: la plataforma vende suscripciones independientes a los dos actores que operan sobre una misma obra vial —la empresa constructora y la empresa supervisora/consultora ambiental— cada una con un módulo exclusivo, financieramente separado, sostenido mediante planes segmentados (Base, Profesional y Enterprise) que permiten el crecimiento de la startup a la par del crecimiento de sus clientes, sin incrementos proporcionales en los costos operativos.

En el marco de este proyecto, la startup desarrolla **EcoRoad**, una plataforma HaaS/SaaS que provee tanto el hardware de sensores ambientales como el software de gestión, dirigida principalmente a empresas constructoras y empresas supervisoras/consultoras ambientales que buscan, respectivamente, evitar infracciones normativas y automatizar la fiscalización de obras viales.

#### Misión

Desarrollar soluciones tecnológicas que permitan a las empresas constructoras y a las empresas supervisoras ambientales del sector vial optimizar el monitoreo, control y cumplimiento de sus obligaciones ambientales, mediante datos captados por sensores IoT propios, en tiempo real, automatización de alertas preventivas y visualización geolocalizada, actuando como árbitro tecnológico neutral entre ambas partes.

#### Visión

Ser la plataforma HaaS/SaaS de referencia en Latinoamérica para la gestión y fiscalización ambiental de proyectos de infraestructura vial, destacando por su innovación, escalabilidad, y por ofrecer datos ambientales inalterables que generan confianza mutua entre constructoras y entes fiscalizadores.

### 1.1.2. Perfiles de los Miembros del Equipo
<a id="1-1-2-perfiles-de-los-miembros-del-equipo"></a>

| Foto | Apellido y Nombre | 
| --- | --- | 
| |Eduardo Martín Guillén Chávez |
| |Andy Alfredo Hipolito Salcedo Muñpoz |
| | |
| | |
| | |


## 1.2 Solution Profile
<a id="1-2-solution-profile"></a>

*EcoRoad* es una plataforma digital integral basada en un modelo SaaS, diseñada para dar soporte a los procesos de monitoreo, control y auditoría ambiental en proyectos de infraestructura vial. Permite a empresas constructoras y consultoras ambientales registrar indicadores ambientales, detectar automáticamente incumplimientos normativos y visualizar en tiempo real, sobre un mapa geolocalizado, el estado de salud ambiental de sus obras.

### 1.2.1 Antecedentes y Problemática
<a id="1-2-1-antecedentes-y-problematica"></a>

La actividad constructora es uno de los motores más dinámicos de la economía peruana, con la obra pública —donde la infraestructura vial tiene un peso importante— como uno de los principales impulsores del crecimiento sectorial (CAPECO, 2025). La ejecución de estos proyectos está sujeta a un marco normativo ambiental cada vez más exigente, fiscalizado para el subsector transportes por la Dirección de Gestión Ambiental del MTC, mientras que la elaboración de los instrumentos de gestión ambiental requeridos recae en consultoras inscritas en el Registro Nacional de Consultoras Ambientales (RNCA) de SENACE, que agrupa a 1,293 consultoras habilitadas a nivel nacional (SENACE, 2024). A pesar de este marco, la digitalización del monitoreo ambiental en obra sigue siendo incipiente, mientras el OEFA avanza hacia una fiscalización más estricta apoyada en monitoreo continuo (OEFA, 2025).

#### What / ¿QUÉ?

EcoRoad busca resolver la fragmentación y el registro manual de datos ambientales durante la ejecución de proyectos viales, integrando tableros geolocalizados en tiempo real, un motor automatizado de alertas e incidencias y un dashboard de control multi-proyecto en un único sistema.

#### When / ¿CUÁNDO?

Esta necesidad es crítica en el contexto actual, en el que la fiscalización ambiental avanza hacia una mayor exigencia tecnológica y en el que la reactivación de la inversión vial incrementa el número de obras activas que requieren monitoreo simultáneo.

#### Where / ¿DÓNDE?

Ocurre principalmente en los proyectos de infraestructura vial ejecutados en el Perú, tanto en zonas urbanas como en tramos interprovinciales, así como en las oficinas centrales de las empresas constructoras y consultoras que supervisan dichos proyectos de forma remota.

#### Who / ¿QUIÉN?

Afecta principalmente a las empresas constructoras que ejecutan las obras viales y deben evidenciar el cumplimiento ambiental ante entidades fiscalizadoras (MTC, OEFA), y a las consultoras ambientales encargadas de diseñar y ejecutar los planes de monitoreo.

#### Why / ¿POR QUÉ?

Porque las infracciones ambientales no detectadas a tiempo generan sanciones económicas, restricciones para participar en licitaciones públicas y daño reputacional. Centralizar el monitoreo y automatizar la detección de incumplimientos reduce el riesgo regulatorio y optimiza el tiempo dedicado a auditorías.

#### How / ¿CÓMO?

Mediante EcoRoad, una plataforma web centralizada en la nube donde el personal de campo registra los indicadores ambientales, el motor automatizado los compara contra los límites normativos y, ante una superación, genera una alerta y crea un ticket de incidencia visible en los tableros y el dashboard geolocalizados.

#### How Much / ¿CUÁNTO?

El modelo de ingresos es de tipo SaaS, mediante planes de suscripción escalables: *Base, **Profesional* y *Enterprise*, diferenciados por número de proyectos, usuarios y funcionalidades de análisis incluidas.

### 1.2.2 Lean UX Process
<a id="1-2-2-lean-ux-process"></a>

#### 1.2.2.1. Lean UX Problem Statements
<a id="1-2-2-1-lean-ux-problem-statements"></a>

El estado actual de *la gestión ambiental en proyectos de infraestructura vial* se ha enfocado principalmente en *el registro manual y disperso de indicadores ambientales, sin herramientas de análisis automatizado ni visualización centralizada, lo que provoca **detección tardía de incumplimientos normativos, mayor exposición a sanciones y auditorías lentas y costosas.* Esta situación afecta a *empresas constructoras y consultoras ambientales*, quienes dependen de métodos desactualizados para monitorear y documentar el cumplimiento ambiental de sus proyectos.

Lo que los productos o servicios existentes no logran resolver es la *centralización digital, en tiempo real, del monitoreo ambiental y la gestión de incidencias en proyectos viales. Nuestro producto, **EcoRoad*, abordará esta brecha mediante una plataforma web SaaS que centraliza el registro de indicadores ambientales, detecta automáticamente las superaciones normativas y ofrece tableros geolocalizados para visualizar múltiples proyectos en simultáneo.

Nuestro enfoque inicial estará dirigido a *empresas constructoras medianas y grandes que ejecutan proyectos viales en el Perú, así como a **consultoras ambientales registradas en el RNCA*. Sabremos que tenemos éxito cuando observemos una reducción medible en el tiempo de detección de incumplimientos, mayor cantidad de incidencias resueltas antes de una fiscalización externa, y una reducción en el tiempo dedicado a preparar auditorías.
