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
