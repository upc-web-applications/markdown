#	NombreProyecto by NombreStartup
<div align="center">
<br><br>
<img src="https://marketingperu.beglobal.biz/wp-content/uploads/2025/01/logo-upc-png-transparente-1.png" alt="drawing" width="100"/> <br><br>

**Universidad Peruana de Ciencias Aplicadas (UPC)**

Facultad de Ingeniería
Carrera de Ingeniería de Software

Ciclo 2026-10 <br><br>

Aplicaciones Web

NRC:12190

Profesor: Hugo Allan Mori Paiva <br><br>

Informe del Trabajo Final

Startup: NombreStartup

Product: NombreProyecto <br><br>

Integrantes:

u20241e158 - Aponte Pablo, Isabel Luisa

u202418655 - Laura Acosta, Victor Jhosuef

u202415412 - Flores Siguas, Marlon Alessandro

Abril 2026

</div>

# Registro de Versiones del Informe

| Version | Fecha | Autor | Descripción de modificación |
| -------- | -------- | -------- | -------- |
| 1.0.0    | Text     | Text     |


# Projet Report Collaboration Insights

Project Report URL: https://github.com/upc-web-applications

# Tabla de contenidos

**Capítulo I: Introducción**  
1.1. [Startup Profile](#11-startup-profile)  
1.1.1. [Descripción del startup](#111-descripción-del-startup)  
1.1.2. [Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)  

1.2. [Solution Profile](#12-solution-profile)  
1.2.1. [Antecedentes y problemática](#121-antecedentes-y-problemática)  
1.2.2. [Lean UX Process](#122-lean-ux-process)  
1.2.2.1. [Lean UX Problem Statements](#1221-lean-ux-problem-statements)  
1.2.2.2. [Lean UX Assumptions](#1222-lean-ux-assumptions)  
1.2.2.3. [Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)  
1.2.2.4. [Lean UX Canvas](#1224-lean-ux-canvas)  

1.3. [Segmentos objetivo](#13-segmentos-objetivo)  


**Capítulo II: Requirements Elicitation & Analysis**  
2.1. [Competidores](#21-competidores)  
2.1.1. [Análisis competitivo](#211-análisis-competitivo)  
2.1.2. [Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)  

2.2. [Entrevistas](#22-entrevistas)  
2.2.1. [Diseño de entrevistas](#221-diseño-de-entrevistas)  
2.2.2. [Registro de entrevistas](#222-registro-de-entrevistas)  
2.2.3. [Análisis de entrevistas](#223-análisis-de-entrevistas)  

2.3. [Needfinding](#23-needfinding)  
2.3.1. [User Personas](#231-user-personas)  
2.3.2. [User Task Matrix](#232-user-task-matrix)  
2.3.3. [User Journey Mapping](#233-user-journey-mapping)  
2.3.4. [Empathy Mapping](#234-empathy-mapping)  

2.4. [Big Picture EventStorming](#24-big-picture-eventstorming)  
2.5. [Ubiquitous Language](#25-ubiquitous-language)  


**Capítulo III: Requirements Specification**  
3.1. [User Stories](#31-user-stories)  
3.2. [Impact Mapping](#32-impact-mapping)  
3.3. [Product Backlog](#33-product-backlog)  


**Capítulo IV: Product Design**  
4.1. [Style Guidelines](#41-style-guidelines)  
4.1.1. [General Style Guidelines](#411-general-style-guidelines)  
4.1.2. [Web Style Guidelines](#412-web-style-guidelines)  

4.2. [Information Architecture](#42-information-architecture)  
4.2.1. [Organization Systems](#421-organization-systems)  
4.2.2. [Labeling Systems](#422-labeling-systems)  
4.2.3. [SEO Tags and Meta Tags](#423-seo-tags-and-meta-tags)  
4.2.4. [Searching Systems](#424-searching-systems)  
4.2.5. [Navigation Systems](#425-navigation-systems)  

4.3. [Landing Page UI Design](#43-landing-page-ui-design)  
4.3.1. [Landing Page Wireframe](#431-landing-page-wireframe)  
4.3.2. [Landing Page Mock-up](#432-landing-page-mock-up)  

4.4. [Web Applications UX/UI Design](#44-web-applications-uxui-design)  
4.4.1. [Web Applications Wireframes](#441-web-applications-wireframes)  
4.4.2. [Web Applications Wireflow Diagrams](#442-web-applications-wireflow-diagrams)  
4.4.3. [Web Applications Mock-ups](#443-web-applications-mock-ups)  
4.4.4. [Web Applications User Flow Diagrams](#444-web-applications-user-flow-diagrams)  

4.5. [Web Applications Prototyping](#45-web-applications-prototyping)  

4.6. [Domain-Driven Software Architecture](#46-domain-driven-software-architecture)  
4.6.1. [Design-Level EventStorming](#461-design-level-eventstorming)  
4.6.2. [Software Architecture Context Diagram](#462-software-architecture-context-diagram)  
4.6.3. [Software Architecture Container Diagrams](#463-software-architecture-container-diagrams)  
4.6.4. [Software Architecture Components Diagrams](#464-software-architecture-components-diagrams)  

4.7. [Software Object-Oriented Design](#47-software-object-oriented-design)  
4.7.1. [Class Diagrams](#471-class-diagrams)  

4.8. [Database Design](#48-database-design)  
4.8.1. [Database Diagrams](#481-database-diagrams)  


**Capítulo V: Product Implementation, Validation & Deployment**  
5.1. [Software Configuration Management](#51-software-configuration-management)  
5.1.1. [Software Development Environment Configuration](#511-software-development-environment-configuration)  
5.1.2. [Source Code Management](#512-source-code-management)  
5.1.3. [Source Code Style Guide & Conventions](#513-source-code-style-guide--conventions)  
5.1.4. [Software Deployment Configuration](#514-software-deployment-configuration)  

5.2. [Landing Page, Services & Applications Implementation](#52-landing-page-services--applications-implementation)  
5.2.1. [Sprint 1](#521-sprint-1)  
5.2.1.1. [Sprint Planning 1](#5211-sprint-planning-1)  
5.2.1.2. [Aspect Leaders and Collaborators](#5212-aspect-leaders-and-collaborators)  
5.2.1.3. [Sprint Backlog 1](#5213-sprint-backlog-1)  
5.2.1.4. [Development Evidence for Sprint Review](#5214-development-evidence-for-sprint-review)  
5.2.1.5. [Execution Evidence for Sprint Review](#5215-execution-evidence-for-sprint-review)  
5.2.1.6. [Services Documentation Evidence for Sprint Review](#5216-services-documentation-evidence-for-sprint-review)  
5.2.1.7. [Software Deployment Evidence for Sprint Review](#5217-software-deployment-evidence-for-sprint-review)  
5.2.1.8. [Team Collaboration Insights during Sprint](#5218-team-collaboration-insights-during-sprint)  

5.3 [Validation Interviews](#53-validation-interview)  
5.3.1. [Diseño de Entrevistas](#531-diseño-entrevistas)  
5.3.2. [Registro de Entrevistas](#532-registro-entrevistas)  
5.3.3. [Evaluaciones según heurísticas](#533-evaluacion-heuristicas)  

5.4. [Video About-the-Product](#54-video-about-the-product)  

**Final**  
[Conclusiones](#conclusiones)  
[Recomendaciones](#recomendaciones)  
[Bibliografía](#bibliografía)  
[Anexos](#anexos)

# Student Outcome

| Criterio Especifico | Acciones realizadas | Conclusiones |
| -------- | -------- | -------- |
| Text     | Text     | Text     |


# Capítulo I: Introducción

## 1.1. Startup Profile
RiskGuard Solutions es una iniciativa concebida por estudiantes 
de Ingeniería de Sistemas de Software, cuyo objetivo primordial es 
la aplicación de la tecnología para la optimización de la seguridad 
en entornos industriales.  Nuestro proyecto, RiskGuard, surge de la 
imperiosa necesidad de mitigar los riesgos laborales en fábricas, 
donde una cantidad considerable de incidentes y casi-accidentes no 
son debidamente registrados ni analizados.

La propuesta se materializa en una aplicación web diseñada para 
facilitar el registro y procesamiento de información de seguridad 
ingresada por operarios, supervisores y personal de recursos humanos.  
A partir del análisis exhaustivo de estos datos, el sistema genera 
alertas y visualizaciones estratégicas que contribuyen a la identificación 
de riesgos potenciales y a la prevención de accidentes laborales.tar el 
registro y procesamiento de información de seguridad ingresada por operarios, 
supervisores y personal de recursos humanos.  A partir del análisis 
exhaustivo de estos datos, el sistema genera alertas y visualizaciones 
estratégicas que contribuyen a la identificación de riesgos potenciales 
y a la prevención de accidentes laborales.

RiskGuard Solutions se presenta como una solución práctica, accesible 
y de fácil uso, orientada a la mejora de la toma de decisiones y a la 
protección integral de la salud y el bienestar de los trabajadores.

### 1.1.1. Descripción del startup

**Nombre de la startup**

NOMBRESTARTUP

**Descripción**


**Visión**
Aspiramos a ser una startup reconocida a nivel nacional por brindar soluciones 
innovadoras y de alto impacto en el ámbito de la seguridad industrial.  Nuestro 
objetivo es destacarnos por nuestra capacidad para reducir significativamente 
los accidentes laborales y mejorar sustancialmente las condiciones de trabajo 
en las empresas.


**Misión**
Nuestra misión consiste en desarrollar soluciones tecnológicas avanzadas 
que permitan a las empresas industriales gestionar y prevenir riesgos laborales 
de manera eficiente.  A través del uso estratégico de herramientas digitales, 
contribuimos a la protección integral de la salud de los trabajadores, priorizando 
su bienestar en el entorno laboral.


**Propuesta de Valor**
En nuestra empresa, la innovación constituye el motor fundamental para el progreso 
y la mejora continua de la seguridad en los entornos industriales.  Priorizamos la 
protección de la salud y el bienestar de los trabajadores, considerándolos el eje 
central de nuestras acciones.  Además, nos comprometemos a ofrecer soluciones accesibles, 
diseñadas para que cualquier usuario pueda utilizarlas sin dificultad.  La colaboración 
es la base sólida sobre la que construimos el trabajo en equipo, y la escalabilidad 
representa la clave para adaptarnos eficazmente a las necesidades cambiantes y 
dinámicas de las empresas.



**Características principales**



### 1.1.2. Perfiles de integrantes del equipo

| Foto | Nombre | Descripción |
| -------- | -------- | -------- |
| ![](https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_640.png) | u20241e158, Aponte Pablo, Isabel Luisa| |
| ![](https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_640.png) | APELLIDOS, NOMBRES (CÓDIGO) | |
| ![](https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_640.png) | Flores Siguas, Marlon ALessandro (u202415412) | |
| ![](https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_640.png) | APELLIDOS, NOMBRES (CÓDIGO) | |
| ![](https://cdn.pixabay.com/photo/2015/10/05/22/37/blank-profile-picture-973460_640.png) | Laura Acosta, Victor Jhosuef (u202418655) | |

## 1.2. Solution Profile

### 1.2.1. Antecedentes y problemática

### 1.2.2. Lean UX Process

#### *1.2.2.1. Lean UX Problem Statements*



#### *1.2.2.2. Lean UX Assumptions*



#### *1.2.2.3. Lean UX Hypothesis Statements*



#### *1.2.2.4. Lean UX Canvas*



## 1.3. Segmentos objetivo



# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores

### 2.1.1. Análisis competitivo


### 2.1.2. Estrategias y tácticas frente a competidores



## 2.2. Entrevistas

### 2.2.1. Diseño de entrevistas



### 2.2.2. Registro de entrevistas



### 2.2.3. Análisis de entrevistas



## 2.3. Needfinding

### 2.3.1. User Personas



### 2.3.2. User Task Matrix



### 2.3.3. User Journey Mapping



### 2.3.4. Empathy Mapping



## 2.4. Big Picture EventStorming



## 2.5. Ubiquitous Language



# Capítulo III: Requirements Specification

## 3.1. User Stories



## 3.2. Impact Mapping



## 3.3. Product Backlog



# Capítulo IV: Product Design

## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines



### 4.1.2. Web Style Guidelines



## 4.2. Information Architecture

### 4.2.1. Organization Systems



### 4.2.2. Labeling Systems



### 4.2.3. SEO Tags and Meta Tags



### 4.2.4. Searching Systems



### 4.2.5. Navigation Systems



## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe



### 4.3.2. Landing Page Mock-up



## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes



### 4.4.2. Web Applications Wireflow Diagrams



### 4.4.3. Web Applications Mock-ups



### 4.4.4. Web Applications User Flow Diagrams



## 4.5. Web Applications Prototyping



## 4.6. Domain-Driven Software Architecture

### 4.6.1. Design-Level EventStorming



### 4.6.2. Software Architecture Context Diagram



### 4.6.3. Software Architecture Container Diagrams



### 4.6.4. Software Architecture Components Diagrams



## 4.7. Software Object-Oriented Design

### 4.7.1. Class Diagrams



## 4.8. Database Design

### 4.8.1. Database Diagrams



# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration



### 5.1.2. Source Code Management



### 5.1.3. Source Code Style Guide & Conventions



### 5.1.4. Software Deployment Configuration



## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. *Sprint Planning 1*



#### 5.2.1.2. *Aspect Leaders and Collaborators*



#### 5.2.1.3. *Sprint Backlog 1*



#### 5.2.1.4. *Development Evidence for Sprint Review*



#### 5.2.1.5. *Execution Evidence for Sprint Review*



#### 5.2.1.6. *Services Documentation Evidence for Sprint Review*



#### 5.2.1.7. *Software Deployment Evidence for Sprint Review*



#### 5.2.1.8. *Team Collaboration Insights during Sprint*

## 5.3. Validation Interviews


### 5.3.1. Diseño de Entrevistas


### 5.3.2. Registro de Entrevistas


### 5.3.3. Evaluación según heurísticas



## 5.4. Video About The Product 





# Conclusiones



# Recomendaciones



# Bibliografía



# Anexos
