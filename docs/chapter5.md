# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration
En esta sección, el equipo presenta y describe los productos de software que  utilizados a lo largo del desarrollo del proyecto. Para cada herramienta se especifica su nombre, propósito dentro del proyecto y la ruta de acceso, ya sea mediante enlace web en el caso de soluciones basadas en SaaS, o mediante enlace de descarga cuando se trata de aplicaciones instalables en los equipos de los integrantes.
Estas herramientas permiten apoyar de manera integral el ciclo de vida del producto digital, abarcando actividades como la gestión del proyecto, el levantamiento de requerimientos, el diseño UX/UI, el desarrollo de software, las pruebas, el despliegue y la documentación

**Project Management**

* WhatsApp (SaaS/Application): Aplicación de mensajería instantánea utilizada por el equipo para coordinar actividades, resolver dudas y mantener comunicación continua durante el desarrollo del proyecto. Permite una interacción rápida y eficiente, facilitando la toma de decisiones y la organización del trabajo en equipo.  
Ruta: https://www.whatsapp.com/

* Trello (SaaS/Application): Herramienta de gestión de proyectos basada en la metodología Kanban, utilizada para planificar, organizar y dar seguimiento a las tareas del proyecto. A través de tableros, listas y tarjetas, permite visualizar el progreso de las actividades, asignar responsabilidades y gestionar los entregables de cada sprint.  
Ruta: https://trello.com/

**Requirements & UX Design**

* UXPressia (SaaS): Herramienta empleada para la elaboración de User Personas, Empathy Maps, Journey Maps e Impact Maps, permitiendo comprender mejor las necesidades, comportamientos y expectativas de los usuarios. Facilita el análisis centrado en el usuario y apoya en la definición de requerimientos del sistema.  
Ruta: https://uxpressia.com/

**Product UX/UI Design**

* Figma (SaaS/Application): Plataforma colaborativa utilizada para diseñar wireframes, mockups y prototipos interactivos. Permite el trabajo en tiempo real entre los miembros del equipo, facilitando la iteración del diseño y la validación de la experiencia de usuario antes del desarrollo.  
Ruta: https://www.figma.com/

* LucidChart (SaaS): Herramienta utilizada para la creación de User Flows, Wireflows y diagramas UML. Permite representar de manera visual la navegación del usuario y la estructura del sistema, facilitando la comprensión de los procesos y la interacción dentro de la aplicación.  
Ruta: https://www.lucidchart.com/

**Software Development**

* Structurizr (SaaS): Herramienta para modelar la arquitectura del sistema mediante el modelo C4, permitiendo visualizar los distintos niveles del sistema (contexto, contenedores, componentes y código). Facilita la comunicación de la arquitectura entre los miembros del equipo.  
Ruta: https://structurizr.com/

* Structurizr DSL (Diagram-as-Code): Lenguaje utilizado para definir diagramas C4 mediante código, lo que permite versionar, mantener y actualizar la arquitectura de forma más eficiente.

* PlantUML (Diagram-as-Code): Herramienta utilizada para la creación de diagramas UML, facilitando la automatización y actualización de los diagramas dentro del proyecto.  
Ruta: https://plantuml.com/

* Vertabelo (SaaS): Herramienta utilizada para el diseño y modelado de bases de datos, permitiendo estructurar entidades, relaciones y esquemas de manera clara y organizada.  
Ruta: https://vertabelo.com/

* Miro (SaaS): Plataforma colaborativa utilizada para la realización de sesiones de EventStorming, facilitando la identificación de eventos de dominio y la comprensión de los procesos del negocio.  
Ruta: https://miro.com/

* Visual Studio Code (Aplicación): Editor de código fuente utilizado para el desarrollo del sistema. Ofrece soporte para múltiples lenguajes, extensiones y herramientas de depuración, lo que mejora la productividad del equipo.  
Ruta: https://code.visualstudio.com/

**Software Deployment**

* Google Chrome (Aplicación): Navegador web utilizado para realizar pruebas funcionales y validar la correcta visualización del sistema. Permite inspeccionar elementos, depurar código y verificar la compatibilidad del producto.  
Ruta: https://www.google.com/chrome

* GitHub (SaaS): Plataforma utilizada para el almacenamiento de repositorios, control de versiones y trabajo colaborativo. Se emplean prácticas como GitFlow Workflow para la gestión de ramas, Conventional Commits para estandarizar los mensajes de commits y Semantic Versioning para el versionado del software.  
Ruta: https://github.com/

* Live Preview (Extensión): Extensión que permite visualizar los cambios realizados en HTML, CSS y JavaScript en tiempo real dentro del navegador, facilitando el desarrollo y la validación de la interfaz.

**Software Documentation**

* Markdown (Lenguaje de marcado): Lenguaje de marcado ligero utilizado para la documentación del proyecto, permitiendo una escritura clara, estructurada y fácil de mantener en repositorios.  
Ruta: https://www.markdownguide.org/

### 5.1.2. Source Code Management

Para la gestión del código fuente, el equipo utilizó **GitHub** como plataforma de control de versiones, lo que permitió llevar un seguimiento ordenado de los cambios, facilitar la colaboración y mantener control sobre el desarrollo del proyecto durante el Sprint.

**Repositorios del proyecto**

<div align="center">

| Componente                  | Repositorio                                                                 |
|---------------------------|------------------------------------------------------------------------------|
| Landing Page              | https://github.com/upc-web-applications/riskguard-landingpage               |
| Frontend Web Application | https://github.com/upc-web-applications/Frontend                            |
| Web Services (Backend)   | https://github.com/upc-web-applications/Backend                             |

</div>

**Estrategia de control de versiones (GitFlow)**

Se tomó como base el modelo **GitFlow**, aunque adaptado al alcance del Sprint 1. Se definieron las ramas principales **main**, que contiene la versión estable, y **develop**, destinada a la integración de nuevas funcionalidades (*features*). Cada *feature* será desarrollada de manera independiente antes de su integración. Sin embargo, para este primer Sprint el trabajo se realizó principalmente sobre la rama *main*, ya que el objetivo fue obtener una primera versión funcional del Landing Page.

**Convención de ramas**

Para los siguientes Sprints, se definieron convenciones para organizar el desarrollo:

- **Feature:** desarrollo de nuevas funcionalidades desde `develop`  
  Convención: `feature/nombre-descriptivo`  

- **Release:** preparación de versiones previas al lanzamiento  
  Convención: `release/vX.Y.Z`  

- **Hotfix:** corrección de errores críticos en producción  
  Convención: `hotfix/vX.Y.Z`  

**Versionamiento (Semantic Versioning)**

Se adoptará **Semantic Versioning (SemVer)** con el formato `MAJOR.MINOR.PATCH`.  
Los cambios **MAJOR** representan modificaciones incompatibles, los **MINOR** nuevas funcionalidades o *features*, y los **PATCH** correcciones o ajustes menores.

**Convención de commits (Conventional Commits)**

Para mantener consistencia en el historial, se utilizó la convención **Conventional Commits**:

- `feat:` nueva funcionalidad  
- `fix:` corrección de errores  
- `docs:` cambios en documentación  
- `style:` formato o estilos sin afectar lógica  
- `refactor:` mejora interna del código  
- `chore:` tareas de mantenimiento  
### 5.1.3. Source Code Style Guide & Conventions

Para el desarrollo del proyecto **RiskGuard**, el equipo tomó como referencia guías reconocidas como la **HTML Style Guide and Coding Conventions de W3Schools**, la **Google HTML/CSS Style Guide**, la **Google JavaScript Style Guide** y las **C# Coding Conventions de Microsoft**, con el objetivo de mantener un código consistente, legible y alineado a buenas prácticas. Todo el desarrollo se realizó utilizando nomenclatura en inglés.

**HTML**

Se adoptaron lineamientos de W3Schools para estructurar correctamente el contenido del Landing Page.

- Se emplea HTML5 como estándar, incluyendo la declaración `<!DOCTYPE html>` al inicio del documento.  
- Los elementos y atributos se escriben en minúsculas para mantener uniformidad.  
- Los valores de los atributos se definen con comillas dobles.  
- Se incluye el atributo `lang` en la etiqueta `<html>` para indicar el idioma del sitio.  
- Todas las imágenes contienen el atributo `alt` con descripciones relevantes.  
- Se utiliza indentación de 2 espacios para mejorar la lectura del código.  
- Se evita el uso de estilos en línea, delegando el diseño a hojas de estilo externas.  
- Se emplean comentarios para identificar secciones principales.

**CSS**

Se siguieron las recomendaciones de la **Google HTML/CSS Style Guide** para organizar los estilos del proyecto.

- Se utilizan nombres de clases en formato `kebab-case`.  
- Los estilos se agrupan por secciones del Landing Page.  
- Se prioriza la reutilización de clases para evitar duplicidad.  
- Se mantiene una estructura ordenada y legible.  
- Se implementa diseño responsive.  
- Se utilizan comentarios para separar secciones de estilos.

**JavaScript**

Para la lógica base se consideraron las recomendaciones de la **Google JavaScript Style Guide**.

- Se utiliza `camelCase` para variables y funciones.  
- Se emplea `const` y `let` en lugar de `var`.  
- Se utilizan nombres descriptivos para funciones y variables.  
- Se mantiene el código modular y organizado.  
- Se separa la lógica de la manipulación del DOM cuando es posible.  
- Se prioriza un código claro, evitando redundancias innecesarias.  

**React (JSX)**

Para la implementación del frontend se aplicaron buenas prácticas específicas de React.

- Los componentes se nombran en `PascalCase` (`App`, `Header`, `HeroSection`).  
- Cada componente cumple una única responsabilidad para mejorar la mantenibilidad.  
- `main.jsx` se encarga de renderizar la aplicación en el DOM.  
- `App.jsx` organiza la estructura general del Landing Page.  
- Se promueve la reutilización de componentes.  
- Se mantiene separación entre lógica y presentación dentro de los componentes.

**C#**

Para el desarrollo backend se adoptarán las **C# Coding Conventions de Microsoft**.

- Clases y métodos en `PascalCase`.  
- Variables y parámetros en `camelCase`.  
- Interfaces con prefijo `I`.  
- Organización por capas (Controllers, Services, Models).  
- Uso de comentarios XML para documentación.

**Convenciones generales**

- Todo el código se desarrolla en inglés.  
- Se prioriza la legibilidad y organización.  
- Se evita la duplicidad de código.  
- Se mantiene una estructura clara del proyecto.  

### 5.1.4. Software Deployment Configuration
En esta sección se describe la configuración del despliegue del proyecto, detallando los pasos necesarios para lograr la publicación del producto a partir de su repositorio de código fuente.
Para este Sprint, el alcance se centra en el desarrollo del **Landing Page de RiskGuard**, por lo que la configuración de despliegue se define únicamente para este componente. El objetivo es establecer un proceso que permita publicar el sitio de manera accesible, asegurando su correcta visualización y disponibilidad en línea.

**GitHub Pages**  
Para la publicación mediante GitHub Pages se definió el siguiente procedimiento:

1. Utilizar la rama `main` como fuente del despliegue.  
2. Acceder a la configuración del repositorio en GitHub.  
3. Ingresar a la sección **Pages** dentro de *Settings*.  
4. Seleccionar la rama `main` como origen de publicación.  
5. Guardar la configuración para habilitar la generación automática del sitio.
   
**Vercel**  
Para el despliegue en Vercel se definió el siguiente proceso:

1. Vincular el repositorio de GitHub con la cuenta de Vercel.  
2. Importar el proyecto desde el repositorio.  
3. Configurar el entorno de despliegue (Vite).  
4. Definir la rama `main` como fuente.  
5. Habilitar el despliegue automático del sitio.

Una vez desplegado, el sitio estará disponible para su acceso en línea mediante la URL generada por la plataforma de despliegue. En la fase de mantenimiento, las actualizaciones se gestionarán mediante commits y merges hacia la rama principal (`main`), siguiendo el flujo de control de versiones definido por el equipo. Cada cambio integrado en esta rama generará automáticamente una nueva versión del sitio desplegado, permitiendo que las mejoras y correcciones se reflejen de manera continua.

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. *Sprint Planning 1*

En este Sprint 1, el equipo se centró en el desarrollo de la Landing Page de RiskGuard, con el objetivo de presentar de manera clara y atractiva la propuesta de valor del sistema. Se trabajaron secciones clave como la sección principal, características, cómo funciona, segmentos, estadísticas y contacto, organizando el trabajo por secciones para facilitar la colaboración entre los integrantes y lograr una integración ordenada del sitio.

| **Campo** | **Detalle** |
|----------|------------|
| Sprint # | 1 |
| Date | 2026-04-05 |
| Time | 10:00 PM |
| Location | Reunión virtual (Google Meet) |
| Prepared By | Flores Eusebio, Angel Thyago |
| Attendees | Aponte Pablo, Isabel Luisa / Laura Acosta, Victor Jhosef / Flores Siguas, Marlon Alessandro / Blancas Chávez, Carlos Franco / Flores Eusebio, Angel Thyago |
| Sprint Goal | Our focus is on developing a responsive landing page for RiskGuard that clearly presents its value proposition through the main section, along with sections for características, cómo funciona, segmentos, estadísticas y contactar. We believe it delivers a better understanding of how the platform helps organizations manage risks and improve safety. This will be confirmed when users can navigate all sections smoothly and understand the purpose of the system on both desktop and mobile devices. |
| Sprint n Velocity | 25 SP |
| Sum of Story Points | 20 SP |

#### 5.2.1.2. *Aspect Leaders and Collaborators*

En este Sprint, los aspectos corresponden a las secciones de la Landing Page de RiskGuard. 
Se asignaron roles de liderazgo y colaboración para cada sección con el fin de mejorar la organización del equipo.

| Miembro del equipo (Apellido, Nombre) | Usuario GitHub | Propuesta de Valor (L/C) | Características (L/C) | Cómo funciona (L/C) | Segmentos (L/C) | Estadísticas (L/C) | Contactar (L/C) | Integración (L/C) |
|--------------------------------------|---------------|--------------------------|----------------------|--------------------|-----------------|--------------------|-----------------|-------------------|
| Aponte Pablo, Isabel Luisa           | IsabelAponte234 | C | C | C | C | C | C | C |
| Laura Acosta, Victor Jhosef          | Zatrynox        | C | C | C | C | C | C | L |
| Blancas Chávez, Carlos Franco        | CarlosBlancas969 | L | L |L | C | L | C | C |
| Flores Eusebio, Angel Thyago         | angelfdevs      | C | C | C | C | C | C | C |

#### 5.2.1.3. *Sprint Backlog 1*

<p><strong>Sprint #:</strong> Sprint 1</p>

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th colspan="2">User Story</th>
      <th colspan="6">Work-Item / Task</th>
    </tr>
    <tr>
      <th>Id</th>
      <th>Title</th>
      <th>Id</th>
      <th>Title</th>
      <th>Description</th>
      <th>Estimation (Hours)</th>
      <th>Assigned To</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>US16</td>
      <td>Visualización de métricas de impacto predictivo</td>
      <td>T11</td>
      <td>Diseño Estadísticas</td>
      <td>Diseñar tarjetas de métricas</td>
      <td>3 </td>
      <td>Laura Acosta, Victor Jhosef</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US16</td>
      <td>Visualización de métricas de impacto predictivo</td>
      <td>T12</td>
      <td>Implementación Estadísticas</td>
      <td>Mostrar indicadores visuales</td>
      <td>4</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US17</td>
      <td>Interacción con botones de conversión</td>
      <td>T15</td>
      <td>Eventos botones</td>
      <td>Configurar los botones</td>
      <td>2</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US61</td>
      <td>Identidad y Acceso General</td>
      <td>T01</td>
      <td>Diseño Header</td>
      <td>Diseñar estructura del navbar</td>
      <td>3</td>
      <td>Flores Thyago, Angel</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US61</td>
      <td>Identidad y Acceso General</td>
      <td>T02</td>
      <td>Implementación Header</td>
      <td>Implementar navbar con logo y menú</td>
      <td>3</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US62</td>
      <td>Propuesta de Valor</td>
      <td>T03</td>
      <td>Diseño Hero</td>
      <td>Diseñar sección principal</td>
      <td>3</td>
      <td>Laura Acosta, Victor Jhosef</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US74</td>
      <td>Propuesta de Valor</td>
      <td>T04</td>
      <td>Implementación Hero</td>
      <td>Agregar texto e imagen principal</td>
      <td>4</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US63</td>
      <td>Catálogo de Capacidades Técnicas</td>
      <td>T05</td>
      <td>Diseño Funciones</td>
      <td>Diseñar tarjetas de funcionalidades</td>
      <td>2</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US63</td>
      <td>Catálogo de Capacidades Técnicas</td>
      <td>T06</td>
      <td>Implementación Características</td>
      <td>Mostrar funcionalidades del sistema</td>
      <td>4</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US64</td>
      <td>Metodología y Validación Social</td>
      <td>T07</td>
      <td>Diseño Cómo funciona</td>
      <td>Diseñar flujo de pasos</td>
      <td>2</td>
      <td>Flores Thyago, Angel</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US64</td>
      <td>Metodología y Validación Social</td>
      <td>T08</td>
      <td>Implementación Cómo funciona</td>
      <td>Mostrar proceso del sistema</td>
      <td>3</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US65</td>
      <td>Beneficios por Rol Operativo</td>
      <td>T09</td>
      <td>Diseño Segmentos</td>
      <td>Diseñar tarjetas por rol</td>
      <td>2</td>
      <td>Flores Thyago, Angel</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US65</td>
      <td>Beneficios por Rol Operativo</td>
      <td>T10</td>
      <td>Implementación Segmentos</td>
      <td>Mostrar beneficios por usuario</td>
      <td>3</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US66</td>
      <td>Cierre y Conversión de Prospectos</td>
      <td>T13</td>
      <td>Diseño CTA</td>
      <td>Diseñar botones de acción</td>
      <td>2 </td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US66</td>
      <td>Cierre y Conversión de Prospectos</td>
      <td>T14</td>
      <td>Implementación CTA</td>
      <td>Agregar botones de contacto</td>
      <td>3</td>
      <td>Blancas Chávez, Carlos Franco</td>
      <td>Completed</td>
    </tr>
  </tbody>
</table>

#### 5.2.1.4. *Development Evidence for Sprint Review*

Durante el Sprint 1, el equipo se centró exclusivamente en el repositorio del Landing Page de RiskGuard. Se realizaron un total de 4 commits el día 26 de abril de 2026, abarcando desde la carga inicial del proyecto hasta la documentación, correcciones de compilación y el despliegue mediante GitHub Pages. A continuación, se presenta el registro de commits:

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Repository</th>
      <th>Branch</th>
      <th>Commit Id</th>
      <th>Commit Message</th>
      <th>Commit Body</th>
      <th>Commited on (Date)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>5c9b242</td>
      <td>Add files via upload</td>
      <td>Implementación completa de la Landing Page (estructura HTML, estilos CSS y secciones: inicio, características, cómo funciona, segmentos, estadísticas y contacto)</td>
      <td>26 de abril de 2026</td>
    </tr>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>57e4417</td>
      <td>docs: deploy github pages</td>
      <td>Configuración y despliegue del proyecto en GitHub Pages</td>
      <td>26 de abril de 2026</td>
    </tr>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>8b240d6</td>
      <td>fix: build</td>
      <td>Se corrigieron errores en la compilación del proyecto</td>
      <td>26 de abril de 2026</td>
    </tr>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>a5f06db</td>
      <td>feat: añadir Readme Landing</td>
      <td>Se agregó el archivo README para la Landing Page de RiskGuard</td>
      <td>26 de abril de 2026</td>
    </tr>
  </tbody>
</table>

#### 5.2.1.5. *Execution Evidence for Sprint Review*

Este Sprint 1 estuvo enfocado en la construcción inicial de la Landing Page de RiskGuard, logrando una primera versión completamente navegable. Se implementaron las secciones principales:
* Hero (RiskGuard): Sección principal que presenta la propuesta de valor y el propósito del sistema.
* Características: Describe las funcionalidades clave de la plataforma y sus beneficios.
* Cómo funciona: Explica el proceso de uso del sistema desde la recopilación de datos hasta la generación de alertas.
* Segmentos: Muestra los tipos de usuarios o áreas a las que está dirigida la solución.
* Estadísticas: Presenta datos relevantes que evidencian la problemática y el impacto del sistema.
* Contactar: Sección que invita al usuario a proteger su planta industrial, ofreciendo iniciar una prueba gratuita o comunicarse con ventas para implementar RiskGuard rápidamente.

El resultado es una interfaz clara, moderna y responsive que comunica efectivamente la propuesta de valor del sistema: la predicción y prevención de riesgos en entornos industriales.

A continuación, las vistas principales desarrolladas:

<h5 align="center">Inicio</h5>
<p align="center">Vista principal con la propuesta de valor.</p>

<p align="center">
  <img src="https://i.postimg.cc/tg3pxQCZ/landing.jpg" width="500"/>
</p>

<h5 align="center">Características</h5>
<p align="center">Funciones clave del sistema.</p>

<p align="center">
  <img src="https://i.postimg.cc/2SzS7SM4/Whats-App-Image-2026-04-26-at-12-02-57-PM.jpg" width="500"/>
</p>

<h5 align="center">Cómo funciona</h5>
<p align="center">Flujo de uso del sistema.</p>

<p align="center">
  <img src="https://i.postimg.cc/Z5T5x52d/Whats-App-Image-2026-04-26-at-12-02-23-PM.jpg" width="500"/>
</p>

<h5 align="center">Segmentos</h5>
<p align="center">Usuarios objetivo.</p>

<p align="center">
  <img src="https://i.postimg.cc/MpWpmpNB/Whats-App-Image-2026-04-26-at-12-02-23-PM-(1).jpg" width="500"/>
</p>

<h5 align="center">Estadísticas</h5>
<p align="center">Datos sobre seguridad industrial.</p>

<p align="center">
  <img src="https://i.postimg.cc/5N5tzC7g/Whats-App-Image-2026-04-26-at-12-02-23-PM-(2).jpg" width="500"/>
</p>

<h5 align="center">Contactar</h5>
<p align="center">Prueba gratuita o contacto.</p>

<p align="center">
  <img src="https://i.postimg.cc/FH9HVH8J/Whats-App-Image-2026-04-26-at-12-02-23-PM-(3).jpg" width="500"/>
</p>

* Video de la Ejecución
[Ver enlace del video](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQDBzzayTq6kQIJAhP26LMO3Ad0Nf1A-UaCJg4qfbtvTvh8?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=mg8Nk6)

#### 5.2.1.6. *Services Documentation Evidence for Sprint Review*

En el Sprint 1, el trabajo se enfocó únicamente en el desarrollo del Landing Page de RiskGuard, por lo que no se incluyó la implementación de servicios web ni APIs. Debido a esto, no corresponde presentar documentación de endpoints en esta etapa.

El esfuerzo del equipo estuvo dirigido a la construcción de la interfaz visual y la experiencia de usuario, permitiendo mostrar de forma clara la propuesta de valor, las funcionalidades y los segmentos a los que está orientada la solución. Al tratarse de una página estática, no fue necesario integrar componentes backend.

La incorporación de Web Services y la documentación de endpoints se realizará en Sprints posteriores, cuando se desarrollen funcionalidades más avanzadas que requieran procesamiento de datos y lógica de negocio.

#### 5.2.1.7. *Software Deployment Evidence for Sprint Review*

El despliegue del Landing Page de **RiskGuard** se realizó utilizando dos plataformas: **GitHub Pages** y **Vercel**, ambas orientadas a la publicación de aplicaciones web estáticas sin necesidad de configurar servidores adicionales.

**Procedimiento realizado**

Se verificó que la versión final del proyecto estuviera almacenada y actualizada en la rama **main** del repositorio.

**GitHub Pages**

- Se accedió al repositorio en GitHub y se ingresó a **Settings → Pages**.  
- En la sección **Source**, se seleccionó la rama **main** y la carpeta raíz.  
- Se guardó la configuración para generar automáticamente la página pública.  
- Se validó que el sitio esté disponible en línea.  

**Vercel**

- Se vinculó el repositorio de GitHub con Vercel.  
- Se configuró el despliegue automático desde la rama **main**.  
- Se ejecutó el proceso de build y publicación.  
- Se verificó el acceso al entorno de producción.  

<p align="center">
  <img src="https://i.postimg.cc/VNXz275M/Whats-App-Image-2026-04-26-at-12-59-55-PM.jpg" width="500"/>
</p>

- **GitHub Pages:**  
  https://upc-web-applications.github.io/riskguard-landingpage/#  

- **Vercel:**  
  https://riskguard-landingpage.vercel.app/


#### 5.2.1.8. *Team Collaboration Insights during Sprint*

Durante el Sprint 1, todos los integrantes del equipo participaron en el desarrollo del Landing Page de RiskGuard, lo cual se evidencia en los commits realizados dentro del repositorio riskguard-landingpage. El trabajo se desarrolló de manera colaborativa, abarcando tanto el diseño como la implementación de las distintas secciones.

En particular, Blancas Chávez, Carlos Franco tuvo un rol destacado en la estructuración e integración general del sitio. Laura Acosta, Victor Jhosef se encargó de la integración del proyecto, consolidando las distintas secciones desarrolladas por el equipo. Por su parte, Flores Eusebio, Angel Thyago, Aponte Pablo e Isabel Luisa  participaron en el diseño visual  y ajustes de la interfaz para mejorar la experiencia de usuario.

El equipo trabajó directamente sobre la rama main, realizando commits continuos para avanzar en el desarrollo. Durante este Sprint no se utilizó un flujo formal de Pull Requests, ya que el objetivo principal fue construir una primera versión funcional del Landing Page en el menor tiempo posible.

<p align="center">
  <img src="https://i.postimg.cc/YqJ9VL8Z/Whats-App-Image-2026-04-26-at-1-13-58-PM.jpg" width="500"/>
</p>

<p align="center">
  <img src="https://i.postimg.cc/0Q22mY2x/Whats-App-Image-2026-04-26-at-1-13-41-PM.jpg" width="500"/>
</p>

### 5.2.2. Sprint 2
#### 5.2.2.1.Sprint Planning 2.

En este Sprint 2, el equipo se enfocó en el desarrollo integral del frontend de la aplicación RiskGuard, implementando las principales interfaces, dashboards y flujos interactivos dirigidos tanto a operarios como a supervisores y gerentes. Durante este Sprint se desarrollaron funcionalidades relacionadas con el registro y seguimiento de incidentes, visualización de alertas, dashboards de monitoreo, mapas de calor, historial de reportes, autenticación y navegación general del sistema. Asimismo, se trabajó con integraciones mediante Fake API para validar el comportamiento y experiencia de usuario antes de la integración definitiva con el backend. El trabajo colaborativo permitió abarcar gran parte de las User Stories priorizadas, garantizando una experiencia responsive, navegable y funcional en las distintas vistas de la plataforma.

| **Campo** | **Detalle** |
|----------|------------|
| Sprint # | 2 |
| Date | 2026-05-10 |
| Time | 4:00 PM |
| Location | Reunión virtual (Google Meet / Zoom) |
| Prepared By | Flores Eusebio, Angel Thyago |
| Attendees | Aponte Pablo, Isabel Luisa / Laura Acosta, Victor Jhosef  / Blancas Chávez, Carlos Franco / Flores Eusebio, Angel Thyago |
| Sprint Goal | Our focus is on developing the frontend interfaces and interactive flows for RiskGuard across the bounded contexts of Account Generation and Authentication, Site / Area and Industrial Asset, Inspection / Unsafe Condition, Risk Assessment (IPERC), Mitigation, Monitoring / Dashboard, and Reports / Compliance. We believe it delivers an organized, realistic and user-centered experience to operators, supervisors and managers by allowing them to interact with the core functionalities of industrial risk prevention and monitoring before backend integration. This will be confirmed when users can seamlessly navigate through the implemented modules, register and monitor incidents, visualize dashboards and reports, and validate the usability and responsiveness of the application across desktop and mobile devices. |
| Sprint n Velocity |    SP |
| Sum of Story Points |  SP |

#### 5.2.2.2. Aspect Leaders and Collaborators.
En este Sprint, los aspectos corresponden a los principales Bounded Contexts desarrollados para la aplicación RiskGuard. Se asignaron roles de liderazgo y colaboración para cada módulo con el fin de mejorar la organización, distribución de tareas y coordinación entre los integrantes del equipo durante el desarrollo del frontend.

| Miembro del equipo (Apellido, Nombre) | Usuario GitHub | Account Generation and Authentication BC (L/C) | Site / Area and Industrial Asset BC (L/C) | Inspection / Unsafe Condition BC (L/C) | Risk Assessment (IPERC) BC (L/C) | Mitigation BC (L/C) | Monitoring / Dashboard BC (L/C) | Reports / Compliance BC (L/C) |
|--------------------------------------|---------------|-----------------------------------------------|-------------------------------------------|----------------------------------------|----------------------------------|---------------------|----------------------------------|-------------------------------|
| Aponte Pablo, Isabel Luisa | IsabelAponte234 | C | C | C | C | C | C | L |
| Laura Acosta, Victor Jhosef | Zatrynox | C | C| C | L | L | C | C |
| Blancas Chávez, Carlos Franco | CarlosBlancas969 | C | L | L | C | C | C | C |
| Flores Eusebio, Angel Thyago | angelfdevs | L | C | C | C | C | L | C |

#### 5.2.2.3. Sprint Backlog 2.
#### 5.2.2.3.1. Sprint Backlog - Integrante 1

| User Story ID | Título | Task ID | Descripción | Estimación (hrs) | Asignado a | Status |
|---|---|---|---|---|---|---|
| US05 | Selección de Sector al Registrar Incidente | T01 | Implementar dropdown de áreas activas filtrado por sede en el formulario de inspección | 2 | Blancas Chávez, Carlos Franco | Done |
| US07 | Selección del Tipo de Incidente | T02 | Implementar dropdown de tipos de incidente con opción "Otro" y campo adicional | 2 | Blancas Chávez, Carlos Franco | Done |
| US08 | Registro de Condición Insegura Vinculada a un Activo | T03 | Implementar dropdown de activos filtrado por área seleccionada | 2 | Blancas Chávez, Carlos Franco | Done |
| US03 | Registro Rápido de Casi-Accidente | T04 | Implementar formulario completo de inspección con validaciones y envío a fake API | 3 | Blancas Chávez, Carlos Franco | Done |
| US04 | Adjuntar Evidencia Fotográfica al Reporte | T05 | Implementar carga de foto con previsualización y validación de tamaño máximo 5MB | 2 | Blancas Chávez, Carlos Franco | Done |
| US10 | Confirmación de Recepción del Reporte | T06 | Implementar pantalla de detalle de inspección con ticket generado automáticamente | 1 | Blancas Chávez, Carlos Franco | Done |
| US12 | Historial de Reportes del Operario | T07 | Implementar lista de inspecciones con filtros por estado y contador de estadísticas | 2 | Blancas Chávez, Carlos Franco | Done |
| US13 | Consulta del Detalle de un Reporte Enviado | T08 | Implementar vista de detalle de inspección con estado, acción correctiva y foto | 2 | Blancas Chávez, Carlos Franco | Done |
| US14 | Visualización de Alertas Activas en el Sector | T09 | Implementar lista de inspecciones pendientes y en progreso con badges de urgencia | 1 | Blancas Chávez, Carlos Franco | Done |
| - | BC Sede — CRUD completo | T10 | Implementar lista, formulario y detalle de sedes con create, update y delete | 3 | Blancas Chávez, Carlos Franco | Done |
| - | BC Área — CRUD completo | T11 | Implementar lista, formulario y detalle de áreas vinculadas a sede con nivel de riesgo | 3 | Blancas Chávez, Carlos Franco | Done |
| - | BC Activo Industrial — CRUD completo | T12 | Implementar lista, formulario y detalle de activos vinculados a área y sede | 3 | Blancas Chávez, Carlos Franco | Done |
| - | Fake API — db.json | T13 | Crear base de datos fake con datos de sedes, áreas, activos e inspecciones para json-server | 1 | Blancas Chávez, Carlos Franco | Done |
| - | Arquitectura DDD | T14 | Estructurar cada BC con capas domain, infrastructure, application y presentation siguiendo el patrón del curso | 2 | Blancas Chávez, Carlos Franco | Done |
| - | i18n ES/EN | T15 | Implementar internacionalización con vue-i18n para español e inglés con botón de cambio en sidebar | 1 | Blancas Chávez, Carlos Franco | Done |
| - | Diseño dark theme RiskGuard | T16 | Implementar estilos globales con paleta de colores #060D1A, #E8460A usando PrimeVue y PrimeFlex | 2 | Blancas Chávez, Carlos Franco | Done |

#### 5.2.2.3.2. Sprint Backlog - Integrante 2
<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th colspan="2">User Story</th>
      <th colspan="6">Work-Item / Task</th>
    </tr>
    <tr>
      <th>Id</th>
      <th>Title</th>
      <th>Id</th>
      <th>Title</th>
      <th>Description</th>
      <th>Estimation (Hours)</th>
      <th>Assigned To</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>US37</td>
      <td>Visualización del Dashboard Ejecutivo de Seguridad</td>
      <td>T01</td>
      <td>Implementación KPIs</td>
      <td>Implementar tarjetas de indicadores clave: incidentes activos, resueltos, sectores críticos y cumplimiento SST</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US37</td>
      <td>Visualización del Dashboard Ejecutivo de Seguridad</td>
      <td>T02</td>
      <td>Detalle de indicador por sector</td>
      <td>Al hacer clic en un KPI, mostrar dialog con listado de sectores y alertas activas; cerrar con un solo clic para volver        al dashboard</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US38</td>
      <td>Visualización de Tendencias de Accidentabilidad</td>
      <td>T03</td>
      <td>Gráfico de tendencias</td>
      <td>Implementar gráfica de línea con evolución mensual de incidentes diferenciada por tipo</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US38</td>
      <td>Visualización de Tendencias de Accidentabilidad</td>
      <td>T04</td>
      <td>Exportar gráfica como imagen</td>
      <td>Implementar descarga de la gráfica de tendencias en formato PNG con un solo clic</td>
      <td>3</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
   <tr>
      <td>US39</td>
      <td>Exportación de Formatos de Auditoría para SUNAFIL</td>
      <td>T05</td>
      <td>Generación reportes auditoría PDF y Excel</td>
      <td>Implementar formulario de exportación con selección de rango de fechas y formato, generación de documento de auditoría en PDF y Excel</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
      <tr>
      <td>US39</td>
      <td>Exportación de Formatos de Auditoría para SUNAFIL</td>
      <td>T07</td>
      <td>Historial y gestión de reportes generados</td>
      <td>Implementar historial de reportes generados</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US40</td>
      <td>Seguimiento del Cumplimiento del Plan Anual de SST</td>
      <td>T07</td>
      <td>Diseño seguimiento SST</td>
      <td>Diseñar tarjetas de cumplimiento de actividades del plan anual de SST con indicador de color por porcentaje</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US40</td>
      <td>Seguimiento del Cumplimiento del Plan Anual de SST</td>
      <td>T08</td>
      <td>Implementación seguimiento SST</td>
      <td>-Implementar vista con cumplimiento global, actividades completadas, gráfica de evolución mensual,         exportación de informe anual PDF y generación de reporte de cumplimiento en PDF o Excel</td>
      <td>5</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US41</td>
      <td>Visualización de Indicadores Predictivos de Riesgo</td>
      <td>T09</td>
      <td>Diseño indicadores predictivos</td>
      <td>Diseñar tarjetas de indicadores predictivos</td>
      <td>3</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US41</td>
      <td>Visualización de Indicadores Predictivos de Riesgo</td>
      <td>T10</td>
      <td>Implementación indicadores predictivos</td>
      <td>Mostrar indicadores predictivos: sectores con tendencia creciente, tipos recurrentes y tiempo promedio de resolución</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US41</td>
      <td>Visualización de Indicadores Predictivos de Riesgo</td>
      <td>T11</td>
      <td>Exportación resumen ejecutivo predictivo PDF</td>
      <td>Implementar generación y descarga del resumen ejecutivo en PDFd</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US42</td>
      <td>Notificación de Alerta Crítica No Resuelta a Gerencia</td>
      <td>T12</td>
      <td>Implementación alertas críticas</td>
      <td>Implementar tabla con acciones marcar como resuelto y eliminar, con tags de severidad por tipo y estado</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
  <tr>
      <td>US43</td>
      <td>Registro Histórico de Incidentes para Trazabilidad Legal</td>
      <td>T13</td>
      <td>Implementación tabla historial de solo lectura</td>
      <td>Implementar tabla inmutable de incidentes sin opciones de edición para garantizar trazabilidad legal ante SUNAFIL</td>
      <td>5</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US43</td>
      <td>Registro Histórico de Incidentes para Trazabilidad Legal</td>
      <td>T14</td>
      <td>Filtros por sector, tipo y rango de fechas</td>
      <td>Implementar filtros de búsqueda por sector, tipo de incidente y rango de fechas con actualización del contador de resultados filtrados</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>US45</td>
      <td>Generación de Reporte Mensual de Gestión de SST</td>
      <td>T15</td>
      <td>Generación de reporte en PDF</td>
      <td>Implementar generación y descarga automática del reporte mensual consolidado en PDF con jsPDF</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
     <tr>
      <td>US45</td>
      <td>Generación de Reporte Mensual de Gestión de SST</td>
      <td>T16</td>
      <td>Historial y previsualización de reportes mensuales</td>
      <td>Implementar historial de reportes mensuales generados con previsualización en historial, re-descarga y eliminación con confirmación</td>
      <td>5</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>TS08</td>
      <td>Endpoint para Obtener Indicadores del Dashboard Ejecutivo</td>
      <td>T17</td>
      <td>Consumo endpoint GET /api/v1/kpi_dashboard</td>
      <td>Consumir el endpoint GET /api/v1/kpi_dashboard para obtener los cuatro indicadores KPI y sincronizarlos reactivamente en el store mediante syncKPIs</td>
      <td>5</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>TS08</td>
      <td>Endpoint para Obtener Tendencias Históricas de Accidentabilidad</td>
      <td>T09</td>
      <td>Consumo endpoint GET /api/v1/historical_trends</td>
      <td>Consumir el endpoint GET /api/v1/historical_trends para obtener la evolución mensual de incidentes y aplicar filtro por sector y por tipo en el frontend</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>TS10</td>
      <td>Endpoint para Gestión de Reportes Generados</td>
      <td>T19</td>
      <td>Consumo endpoints GET, POST y DELETE /api/v1/generated_reports</td>
      <td>Consumir los endpoints de reportes generados para listar, registrar y eliminar reportes; la generación del documento PDF o Excel se realiza en el cliente con jsPDF</td>
      <td>4</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>TS11</td>
      <td>Endpoint para Gestión de Alertas Críticas</td>
      <td>T20</td>
      <td>Consumo endpoints GET, PATCH y DELETE /api/v1/critical_alerts</td>
      <td>Consumir los endpoints de alertas críticas para listar, actualizar estado y eliminar alertas, con recálculo automático del KPI de sectores críticos tras cada operación</td>
      <td>5</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
    <tr>
      <td>TS12</td>
      <td>Endpoint para Obtener el Plan Anual de SST y su Cumplimiento</td>
      <td>T21</td>
      <td>Consumo endpoint GET /api/v1/annual_ohs_plan</td>
      <td>Consumir el endpoint GET /api/v1/annual_ohs_plan para obtener el porcentaje de cumplimiento global y el desglose por sector, y alimentar la vista de seguimiento SST y el KPI del dashboard</td>
      <td>5</td>
      <td>Aponte Pablo, Isabel Luisa</td>
      <td>Completed</td>
    </tr>
  </tbody>
</table>

#### 5.2.2.3.3. Sprint Backlog - Integrante 3

| User Story ID | Título | Task ID | Descripción | Estimación (hrs) | Asignado a | Status |
|---|---|---|---|---|---|---|
| US19 | Visualización del Mapa de Calor Operativo | T01 | Implementar dashboard principal con KPIs de tickets pendientes, tickets en progreso y mapa de calor por sectores | 3 | Flores Eusebio, Angel Thyago | Done |
| US29 | Exploración Sectorizada y Filtrado de Alertas Activas | T03 | Implementar filtros de tickets por sector, nivel de riesgo y estado dentro de la bandeja de tickets | 3 | Flores Eusebio, Angel Thyago | Done |
| US28 | Asignación de Tickets de Acción Correctiva | T04 | Implementar bandeja de tickets con acciones para asignar técnico o visualizar detalle de asignación | 3 | Flores Eusebio, Angel Thyago | Done |
| US28 | Asignación de Tickets de Acción Correctiva | T05 | Implementar formulario de asignación y reasignación de técnico responsable a un ticket | 3 | Flores Eusebio, Angel Thyago | Done |
| US33 | Escalamiento Automático por Incumplimiento de SLA | T06 | Mostrar estado SLA incumplido en tickets vencidos y adaptar el tiempo restante como tiempo excedido | 2 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración de Sectores y Áreas Operativas | T07 | Implementar sección Mapa de Sectores con listado, contador de sectores y contador de activos relacionados | 3 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración de Sectores y Áreas Operativas | T08 | Implementar formulario de creación y edición de sectores con código automático, descripción y estado activo/inactivo | 3 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración y Gestión de Activos Industriales | T09 | Implementar sección Gestión de Activos con listado, contador total y acciones por estado operativo | 3 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración y Gestión de Activos Industriales | T10 | Implementar formulario de creación y edición de activos industriales con código automático y campos bloqueados cuando corresponde | 3 | Flores Eusebio, Angel Thyago | Done |
| US34 | Programación de Mantenimiento Preventivo de Activos | T11 | Implementar formulario para programar mantenimiento preventivo sobre un activo y actualizar su estado a mantenimiento | 3 | Flores Eusebio, Angel Thyago | Done |
| US34 | Programación de Mantenimiento Preventivo de Activos | T12 | Implementar reactivación de activos en mantenimiento y actualización de la fecha de última revisión | 2 | Flores Eusebio, Angel Thyago | Done |
| US27 | Gestión y Administración de Personal Técnico | T13 | Implementar Directorio Técnico con listado de técnicos, especialidad, estado y acción de detalle | 3 | Flores Eusebio, Angel Thyago | Done |
| US27 | Gestión y Administración de Personal Técnico | T14 | Implementar formulario de registro y edición de técnicos con código automático y estado activo/inactivo | 3 | Flores Eusebio, Angel Thyago | Done |
| US27 | Gestión y Administración de Personal Técnico | T15 | Integrar técnicos activos con el formulario de asignación de tickets correctivos | 2 | Flores Eusebio, Angel Thyago | Done |
| US35 | Generación y Exportación de Reportes de Cumplimiento | T16 | Implementar sección Reportes y Cumplimiento con reportes por sector, estado y rango de fechas | 3 | Flores Eusebio, Angel Thyago | Done |
| US35 | Generación y Exportación de Reportes de Cumplimiento | T17 | Implementar filtros de reportes por sector, opción Todos, fechas y botón para limpiar filtros | 2 | Flores Eusebio, Angel Thyago | Done |
| - | Fake API — json-server | T19 | Crear y ajustar db.json con sectores, tickets, técnicos, activos, mantenimientos preventivos y reportes archivados | 2 | Flores Eusebio, Angel Thyago | Done |
| - | Arquitectura DDD del BC Monitoring | T20 | Estructurar el bounded context monitoring-dashboard con capas application, domain, infrastructure y presentation | 3 | Flores Eusebio, Angel Thyago | Done |
| - | Modelos de Dominio y Assemblers | T21 | Crear entidades y assemblers para tickets, sectores, técnicos, activos, mapa de calor y mantenimientos preventivos | 3 | Flores Eusebio, Angel Thyago | Done |
| - | Integración API e Infraestructura | T22 | Implementar MonitoringApi usando BaseApi, BaseEndpoint y variables de entorno para endpoints del fake API | 2 | Flores Eusebio, Angel Thyago | Done |
| - | Navegación y Rutas | T23 | Configurar rutas del bounded context para dashboard, tickets, sectores, técnicos, activos, mantenimiento y reportes | 2 | Flores Eusebio, Angel Thyago | Done |
| - | i18n ES/EN | T24 | Implementar textos principales en español e inglés usando vue-i18n, incluyendo navegación y footer | 2 | Flores Eusebio, Angel Thyago | Done |
| - | Diseño dark theme RiskGuard | T25 | Ajustar estilos globales con tema oscuro, acento naranja, tablas PrimeVue, formularios, sidebar y footer | 3 | Flores Eusebio, Angel Thyago | Done |
| - | Configuración para Deploy | T26 | Preparar variables de entorno para Vercel y API desplegada en Render | 1 | Flores Eusebio, Angel Thyago | Done |
| US01 | Autenticación de Operario | T26 | Implementar pantalla de inicio de sesión RiskGuard con formulario de correo y contraseña | 2 | Angel Thyago Flores Eusebio | Done |
| US01 | Autenticación de Operario | T27 | Validar formato de correo antes de procesar el inicio de sesión | 1 | Angel Thyago Flores Eusebio | Done |
| US01 | Autenticación de Operario | T28 | Validar credenciales preconfiguradas del operario desde la Fake API | 2 | Angel Thyago Flores Eusebio | Done |
| US01 | Autenticación de Operario | T29 | Implementar mensaje de error para correo o contraseña incorrectos | 1 | Angel Thyago Flores Eusebio | Done |
| US01 | Autenticación de Operario | T30 | Implementar contador de intentos fallidos y bloqueo temporal después de 5 intentos | 2 | Angel Thyago Flores Eusebio | Done |
| US01 | Autenticación de Operario | T31 | Redirigir al operario autenticado hacia su panel correspondiente según su rol | 2 | Angel Thyago Flores Eusebio | Done |
| US02 | Cierre de Sesión del Operario | T32 | Implementar botón de cierre de sesión dentro del panel autenticado | 1 | Angel Thyago Flores Eusebio | Done |
| US02 | Cierre de Sesión del Operario | T33 | Limpiar la sesión activa del usuario al cerrar sesión y redirigir al login | 2 | Angel Thyago Flores Eusebio | Done |
| US02 | Cierre de Sesión del Operario | T34 | Implementar cierre automático de sesión por inactividad luego de 30 segundos | 2 | Angel Thyago Flores Eusebio | Done |
| US24 | Autenticación Segura de Supervisor | T35 | Implementar pantalla de inicio de sesión RiskGuard con formulario de correo y contraseña | 2 | Angel Thyago Flores Eusebio | Done |
| US24 | Autenticación Segura de Supervisor | T36 | Validar formato de correo antes de procesar el inicio de sesión | 1 | Angel Thyago Flores Eusebio | Done |
| US24 | Autenticación Segura de Supervisor | T37 | Validar credenciales preconfiguradas del supervisor desde la Fake API | 2 | Angel Thyago Flores Eusebio | Done |
| US24 | Autenticación Segura de Supervisor | T38 | Implementar mensaje de error para correo o contraseña incorrectos | 1 | Angel Thyago Flores Eusebio | Done |
| US24 | Autenticación Segura de Supervisor | T39 | Redirigir al supervisor autenticado hacia su panel correspondiente según su rol | 1 | Angel Thyago Flores Eusbio | Done | 
| US36 | Autenticación Segura de Gerente o Administrador | T40 | Configurar usuarios demo para administrador, supervisor y operario en db.json | 1 | Angel Thyago Flores Eusebio | Done |
| US36 | Autenticación Segura de Gerente o Administrador | T41 | Implementar validación de credenciales para usuarios de alta dirección | 2 | Angel Thyago Flores Eusebio | Done |
| US36 | Autenticación Segura de Gerente o Administrador | T42| Mostrar panel simple según el rol autenticado: administración, supervisor u operario | 2 | Angel Thyago Flores Eusebio | Done |
| - | Identity Access — Arquitectura DDD | T43 | Estructurar el bounded context con capas application, domain, infrastructure y presentation | 2 | Angel Thyago Flores Eusebio | Done |
| - | Identity Access — Entidades de Dominio | T44 | Crear entidades User, Session y AccessLog con nomenclatura en inglés y atributos neutros | 2 | Angel Thyago Flores Eusebio | Done |
| - | Identity Access — Infrastructure | T45 | Implementar BaseApi, BaseEndpoint, IdentityAccessApi y assemblers siguiendo el estilo de learning-center | 3 | Angel Thyago Flores Eusebio | Done |
| - | Fake API — Identity Access | T46 | Crear datos fake de roles, usuarios, sesiones y registros de acceso usando uuid | 2 | Angel Thyago Flores Eusebio | Done |
| - | i18n ES/EN | T47 | Implementar textos en español e inglés para login, validaciones, panel y cierre de sesión | 1 | Angel Thyago Flores Eusebio | Done |
| - | Diseño RiskGuard | T48 | Adaptar el diseño visual al tema oscuro de RiskGuard con color principal naranja | 2 | Angel Thyago Flores Eusebio | Done |
| - | Deploy y Configuración | T49 | Configurar variables de entorno para desarrollo y producción con envDir en Vite | 1 | Angel Thyago Flores Eusebio | Done |



#### 5.2.2.4.Development Evidence for Sprint Review.

Durante el Sprint 2, el equipo realizó el desarrollo de las funcionalidades correspondientes a cada Epic en el repositorio frontend del proyecto RiskGuard. A continuación se presenta el registro de commits realizados en las ramas de trabajo de cada integrante, evidenciando el progreso y las contribuciones individuales durante el período del sprint.

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Repository</th>
      <th>Branch</th>
      <th>Commit Id</th>
      <th>Commit Message</th>
      <th>Commit Body</th>
      <th>Commited on (Date)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>4066cfd</td>
      <td>Create index</td>
      <td>Creación del archivo índice del proyecto</td>
      <td>Apr 24, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>8a88511</td>
      <td>add inspection and headquarters BC</td>
      <td>Agregado bounded context de inspección y sede central</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>8aa1c72</td>
      <td>fix: rename in english</td>
      <td>Corrección de nombres de archivos y variables al inglés</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>0ebc3b5</td>
      <td>Merge pull request #1 from upc-web-applications/feature/inspection_headquarters</td>
      <td>Fusión de la rama feature/inspection_headquarters al flujo principal</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>41a4aa4</td>
      <td>feat: upload bc</td>
      <td>Subida del bounded context de evaluación de riesgos</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>b8e45b7</td>
      <td>fix: add</td>
      <td>Corrección y adición de archivos faltantes en el módulo</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>3570ff1</td>
      <td>fix: add</td>
      <td>Segunda corrección de archivos faltantes en el módulo</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/monitoring-dashboard</td>
      <td>5034b80</td>
      <td>monitoring-dashboard bc</td>
      <td>Agregado bounded context del dashboard de monitoreo del supervisor</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/monitoring-dashboard</td>
      <td>2f1d68a</td>
      <td>update feature/monitoring-dashboard</td>
      <td>Actualización de componentes y vistas del panel de monitoreo</td>
      <td>May 15, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>b1cc4de</td>
      <td>Merge branch 'main' of Frontend-RiskGuard</td>
      <td>Sincronización con la rama main del repositorio personal</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>f9d6a2c</td>
      <td>feat: add es and en</td>
      <td>Agregado archivos de internacionalización en español e inglés</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>03a43ab</td>
      <td>feat: add database db</td>
      <td>Agregado archivo de base de datos json-server</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>b6b23eb</td>
      <td>feat: add env</td>
      <td>Agregado archivo de variables de entorno del proyecto</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>b3ec027</td>
      <td>feat: add shared</td>
      <td>Agregado componentes y recursos compartidos del módulo</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>3415ec1</td>
      <td>feat: add entities</td>
      <td>Agregado entidades del dominio de reportes y cumplimiento SST</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>42e7dcf</td>
      <td>feat: add assemblers and api</td>
      <td>Agregado assemblers y servicios de consumo de API</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>4f10c4e</td>
      <td>feat: add store</td>
      <td>Agregado store  para gestión de estado del módulo</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>70fdeae</td>
      <td>feat: add presentation reports styles</td>
      <td>Agregado estilos y estructura visual de las vistas de reportes</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>3fcc99b</td>
      <td>feat: add configuration</td>
      <td>Agregado configuración del módulo de reportes y cumplimiento</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>dbeea7d</td>
      <td>fix: correct position</td>
      <td>Corrección de posicionamiento de elementos en la interfaz</td>
      <td>May 13, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>297db99</td>
      <td>feat: add service pdf and excel</td>
      <td>Agregado servicio de generación de documentos PDF y Excel con jsPDF</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>e0cf4ad</td>
      <td>feat: add new presentation</td>
      <td>Agregado nueva vista de presentación del módulo de reportes</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>de75928</td>
      <td>feat: update routes</td>
      <td>Actualización del enrutamiento para las vistas de reportes</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>3b0f309</td>
      <td>feat: reports updates</td>
      <td>Actualización de componentes y lógica del módulo de reportes</td>
      <td>May 14, 2026</td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/user-authentication</td>
      <td>8116699</td>
      <td>authentication bc</td>
      <td>Agregado bounded context de autenticación de usuarios</td>
      <td>May 15, 2026</td>
    </tr>
  </tbody>
</table>

#### 5.2.2.5.Execution Evidence for Sprint Review.

Durante el Sprint se lograron avances significativos en la visualización y navegación de la aplicación, incluyendo interfaces de identificacion, Dashboard del operador, del supervisor y del gerente

#### Account Generation and Authentication BC

<h5 align="center">Inicio de autenticación</h5>

<p align="center">
  <img src="https://i.postimg.cc/1z3GFxQN/Whats-App-Image-2026-05-15-at-10-14-36-PM.jpg" width="500"/>
</p>

*Pantalla de autenticación del sistema donde el usuario ingresa sus credenciales para acceder a la plataforma.*

#### Site / Area and Industrial Asset BC

#### Inspection / Unsafe Condition BC

#### Risk Assessment (IPERC) BC  

#### Mitigation BC 

#### Monitoring / Dashboard BC 

#### Reports / Compliance BC
<h5 align="center">1. Visualización de Inicio del Gerente</h5>

<p align="center">
  <img src="https://i.postimg.cc/VNMh3c36/Whats-App-Image-2026-05-15-at-9-35-46-PM-(2).jpg" width="500"/>
</p>

*Vista principal del gerente con acceso al resumen general del sistema y métricas de seguridad.*

<h5 align="center">2. Visualización de Nuevo Reporte del Gerente</h5>

<p align="center">
  <img src="https://i.postimg.cc/0yh3WNH7/Whats-App-Image-2026-05-15-at-9-35-46-PM-(3).jpg" width="500"/>
</p>

*Vista orientada al registro de nuevos reportes de incidentes y condiciones inseguras.*

<h5 align="center">3. Visualización de Mis Reportes del Gerente</h5>

<p align="center">
  <img src="https://i.postimg.cc/jSB9gjkP/Whats-App-Image-2026-05-15-at-9-35-46-PM-(4).jpg" width="500"/>
</p>

*Vista para la consulta y administración de reportes generados dentro del sistema.*

<h5 align="center">4. Visualización del Historial de Incidentes del Gerente</h5>

<p align="center">
  <img src="https://i.postimg.cc/JzSg6hdt/Whats-App-Image-2026-05-15-at-9-35-46-PM-(5).jpg" width="500"/>
</p>
*Vista enfocada en el seguimiento y análisis del historial de incidentes registrados.*

<h5 align="center">5. Visualización de Alertas Críticas del Gerente</h5>

<p align="center">
  <img src="https://i.postimg.cc/HkFKZLPY/Whats-App-Image-2026-05-15-at-9-35-46-PM-(6).jpg" width="500"/>
</p>

*Vista de alertas críticas para supervisar eventos de riesgo y estados de atención.*

<h5 align="center">6. Visualización de Indicadores Predictivos del Gerente</h5>

<p align="center">
  <img src="https://i.postimg.cc/DwRDjzYf/Whats-App-Image-2026-05-15-at-9-35-46-PM-(7).jpg" width="500"/>
</p>
*Vista de indicadores predictivos con métricas y tendencias relacionadas a seguridad industrial.*

<h5 align="center">7. Visualización del Plan SST del Gerente</h5>

<p align="center">
  <img src="https://i.postimg.cc/L8G7Cs08/Whats-App-Image-2026-05-15-at-9-35-46-PM-(8).jpg" width="500"/>
</p>

*Vista del Plan SST con indicadores de cumplimiento, actividades completadas y monitoreo mensual.*

* Video de la Ejecución del Web app  Dashboard Gerente
[Ver enlace](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQBALHFNZT8gT4yDbhrSrY9UAZIWLt8aMd3C8mnHjEJcOPc?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=3vniTW)

#### 5.2.2.6.Services Documentation Evidence for Sprint Review.

En esta sección se incluye la relación de Endpoints documentados con OpenAPI, relacionados con el alcance del Sprint. A continuación se resume los logros alcanzados en relación con Documentación de Web Services para este Sprint.
Para este Sprint no se cuenta con un repositorio independiente de Web Services ni con servicios backend desplegados. La aplicación consume una API local simulada basada en json-server, definida dentro del mismo repositorio frontend mediante los archivos `server/db.json` y `server/routes.json`. Por este motivo, el repositorio de Servicios Web corresponde al repositorio frontend del proyecto RiskGuard, donde se encuentran definidos y versionados los endpoints mock.

Se documentan los endpoints simulados utilizados para validar las funcionalidades desarrolladas durante el sprint.

**Repositorio API/local:** https://github.com/upc-web-applications/Frontend.git 

**URL base local:** `http://localhost:3000/api/v1`  
**Archivo de datos simulado:** `server/db.json`  
**Archivo de rutas simulado:** `server/routes.json`

**Commits relacionados con Documentación e implementación de endpoints:**

| Commit Id | Mensaje |
|---|---|
| 42e7dcf | feat: add assemblers and api |
| 4f10c4e | feat: add store |
| 3415ec1 | feat: add entities |
| 03a43ab | feat: add database db |
| 3b0f309 | feat: reports updates |
| b6b23eb | feat: add env |

**Tabla de Endpoints**


<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Endpoint</th>
      <th>Acciones implementadas</th>
      <th>URL local</th>
      <th>Verbo HTTP</th>
      <th>Sintaxis de llamada</th>
      <th>Parámetros</th>
      <th>Ejemplo de Response</th>
      <th>Explicación</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>/kpi_dashboard</code></td>
      <td>Obtener indicadores KPI del dashboard ejecutivo</td>
      <td><code>http://localhost:3000/api/v1/kpi_dashboard</code></td>
      <td><code>GET</code></td>
      <td><code>GET /api/v1/kpi_dashboard</code></td>
      <td>No requiere parámetros</td>
      <td><pre>[
  { "id": "KPI_001", "name": "active_incidents",
    "value": 3, "goal": 0, "status": "alert" },
  { "id": "KPI_002", "name": "resolved_incidents",
    "value": 6, "goal": 10, "status": "optimal" },
  { "id": "KPI_003", "name": "critical_sectors",
    "value": 2, "goal": 0, "status": "danger" },
  { "id": "KPI_004", "name": "ohs_plan_compliance",
    "value": 72, "goal": 80, "status": "alert" }
]</pre></td>
      <td>Cada objeto contiene el nombre del indicador (<code>name</code>), el valor actual (<code>value</code>), la meta (<code>goal</code>) y el estado visual (<code>optimal</code>, <code>alert</code>, <code>danger</code>). El frontend sincroniza estos valores reactivamente mediante <code>syncKPIs()</code> al resolver incidentes o alertas.</td>
    </tr>
    <tr>
      <td><code>/historical_trends</code></td>
      <td>Obtener evolución mensual de incidentes por tipo y sector</td>
      <td><code>http://localhost:3000/api/v1/historical_trends</code></td>
      <td><code>GET</code></td>
      <td><code>GET /api/v1/historical_trends</code></td>
      <td>No requiere parámetros. El filtrado por sector y tipo se aplica en el frontend.</td>
      <td><pre>{
  "id": "TREND_2024_04",
  "month": 4, "year": 2024,
  "total_incidents": 22,
  "incidents_by_type": {
    "Chemical Leak": 9,
    "Pressure Anomaly": 7,
    "Unsafe Condition": 4,
    "Abnormal Vibration": 2
  },
  "incidents_by_sector": {
    "WAREHOUSE_B": 9,
    "GAS_PLANT": 7
  }
}</pre></td>
      <td>Cada registro corresponde a un mes. El frontend filtra <code>incidents_by_sector</code> al seleccionar un sector y construye datasets por tipo usando <code>incidents_by_type</code>. Los meses con incremento mayor al 20% respecto al anterior se resaltan en rojo en la gráfica.</td>
    </tr>
    <tr>
      <td><code>/critical_alerts</code></td>
      <td>Listar alertas críticas del sistema</td>
      <td><code>http://localhost:3000/api/v1/critical_alerts</code></td>
      <td><code>GET</code></td>
      <td><code>GET /api/v1/critical_alerts</code></td>
      <td>No requiere parámetros</td>
      <td><pre>[
  {
    "id": "ALERT_001",
    "type": "CRITICAL",
    "sector": "WAREHOUSE_B",
    "risk_type": "Chemical Leak",
    "elapsed_hours": 72,
    "responsible_supervisor": "Ana Torres",
    "status": "unresolved",
    "message": "Fuga de ácido en contenedor
     IBC-12 supera el umbral de seguridad."
  }
]</pre></td>
      <td>El campo <code>type</code> puede ser <code>CRITICAL</code> o <code>ALERT</code>. El campo <code>status</code> puede ser <code>unresolved</code>, <code>in_review</code> o <code>resolved</code>. El frontend calcula el KPI <code>critical_sectors</code> contando sectores con alertas <code>unresolved</code> o <code>in_review</code>.</td>
    </tr>
    <tr>
      <td><code>/critical_alerts/{id}</code></td>
      <td>Actualizar estado de una alerta crítica</td>
      <td><code>http://localhost:3000/api/v1/critical_alerts/{id}</code></td>
      <td><code>PATCH</code></td>
      <td><code>PATCH /api/v1/critical_alerts/ALERT_001</code></td>
      <td><code>id</code> en la URL. Body: <code>{ "status": "resolved" }</code></td>
      <td><pre>{
  "id": "ALERT_001",
  "type": "CRITICAL",
  "sector": "WAREHOUSE_B",
  "status": "resolved",
  "elapsed_hours": 72,
  "responsible_supervisor": "Ana Torres",
  "message": "Fuga de ácido en contenedor
   IBC-12 supera el umbral de seguridad."
}</pre></td>
      <td>Al recibir la respuesta, el store actualiza el registro en el arreglo local y ejecuta <code>syncKPIs()</code> para recalcular el KPI de sectores críticos sin recargar la página.</td>
    </tr>
    <tr>
      <td><code>/critical_alerts/{id}</code></td>
      <td>Eliminar una alerta crítica</td>
      <td><code>http://localhost:3000/api/v1/critical_alerts/{id}</code></td>
      <td><code>DELETE</code></td>
      <td><code>DELETE /api/v1/critical_alerts/ALERT_001</code></td>
      <td><code>id</code> en la URL</td>
      <td><pre>{} (HTTP 200)</pre></td>
      <td>El store filtra el arreglo local eliminando el registro con el id correspondiente y recalcula los KPIs reactivamente mediante <code>syncKPIs()</code>.</td>
    </tr>
    <tr>
      <td><code>/annual_ohs_plan</code></td>
      <td>Obtener cumplimiento global y desglose mensual del plan anual de SST</td>
      <td><code>http://localhost:3000/api/v1/annual_ohs_plan</code></td>
      <td><code>GET</code></td>
      <td><code>GET /api/v1/annual_ohs_plan</code></td>
      <td>No requiere parámetros</td>
      <td><pre>{
  "id": "PLAN_2024", "year": 2024,
  "global_compliance": 72, "goal": 80,
  "completed_activities": 86,
  "total_activities": 120,
  "critical_months": 2,
  "monthly_details": [
    { "month": 1, "compliance": 70,
      "completed_activities": 8,
      "planned_activities": 12,
      "status": "acceptable" },
    { "month": 2, "compliance": 45,
      "completed_activities": 5,
      "planned_activities": 12,
      "status": "critical" }
  ]
}</pre></td>
      <td>El frontend usa <code>global_compliance</code> para mostrar el indicador con color (verde ≥80%, amarillo 50–79%, rojo &lt;50%) y <code>monthly_details</code> para construir la gráfica de evolución mensual. El campo <code>details_by_sector</code> alimenta el panel de detalle al hacer clic en el KPI del dashboard.</td>
    </tr>
    <tr>
      <td><code>/predictive_indicators</code></td>
      <td>Obtener indicadores predictivos de riesgo de los últimos 30 días</td>
      <td><code>http://localhost:3000/api/v1/predictive_indicators</code></td>
      <td><code>GET</code></td>
      <td><code>GET /api/v1/predictive_indicators</code></td>
      <td>No requiere parámetros</td>
      <td><pre>{
  "id": "PRED_001",
  "period_days": 30,
  "total_incidents": 42,
  "previous_month_variation": 15,
  "average_resolution_time_hours": 8,
  "sectors_with_increasing_trend": [
    { "sector": "WAREHOUSE_B",
      "status": "critical" },
    { "sector": "GAS_PLANT",
      "status": "warning" }
  ]
}</pre></td>
      <td>El campo <code>sectors_with_increasing_trend</code> se muestra como tags de severidad (<code>danger</code> para critical, <code>warning</code> para warning). El campo <code>previous_month_variation</code> indica el porcentaje de variación respecto al mes anterior.</td>
    </tr>
    <tr>
      <td><code>/historical_incident_records</code></td>
      <td>Consultar historial completo de incidentes (solo lectura)</td>
      <td><code>http://localhost:3000/api/v1/historical_incident_records</code></td>
      <td><code>GET</code></td>
      <td><code>GET /api/v1/historical_incident_records</code></td>
      <td>No requiere parámetros. El filtrado por sector, tipo y rango de fechas se aplica en el frontend.</td>
      <td><pre>{
  "id": "INC_006",
  "date": "2024-03-03",
  "section": "GAS_PLANT",
  "incident_type": "Pressure Anomaly",
  "description": "High pressure alert in
   pipeline B — valve showed 140%
   of nominal value",
  "resolved": false,
  "criticality": "CRITICAL",
  "operator_id": "OP_003"
}</pre></td>
      <td>La tabla del historial es de solo lectura. No se habilita ningún campo de edición para garantizar la trazabilidad legal ante auditorías de SUNAFIL.</td>
    </tr>
    <tr>
      <td><code>/generated_reports</code></td>
      <td>Listar reportes generados</td>
      <td><code>http://localhost:3000/api/v1/generated_reports</code></td>
      <td><code>GET</code></td>
      <td><code>GET /api/v1/generated_reports</code></td>
      <td>No requiere parámetros. El filtrado por mes, año y tipo se aplica en el frontend.</td>
      <td><pre>[
  {
    "id": "DmNMTQ6",
    "type": "monthly",
    "month": 1, "year": 2026,
    "format": "pdf",
    "generation_date":
      "2026-05-15T02:27:04.290Z",
    "file_name":
      "RiskGuard_Reporte_Mensual_
       enero_2026.pdf",
    "status": "generated",
    "size_kb": 14
  }
]</pre></td>
      <td>El campo <code>type</code> puede ser <code>monthly</code>, <code>audit</code> o <code>compliance</code>. El campo <code>format</code> puede ser <code>pdf</code> o <code>xlsx</code>. El frontend regenera el archivo al hacer clic en descargar usando los datos del store junto con jsPDF.</td>
    </tr>
    <tr>
      <td><code>/generated_reports</code></td>
      <td>Registrar nuevo reporte generado</td>
      <td><code>http://localhost:3000/api/v1/generated_reports</code></td>
      <td><code>POST</code></td>
      <td><code>POST /api/v1/generated_reports</code></td>
      <td>Body: <code>{ "type", "month", "year", "format", "generation_date", "file_name", "status", "size_kb" }</code></td>
      <td><pre>{
  "id": "xK9pQmR",
  "type": "monthly",
  "month": 3, "year": 2026,
  "format": "pdf",
  "file_name":
    "RiskGuard_Reporte_Mensual_
     marzo_2026.pdf",
  "status": "generated",
  "size_kb": 14
} (HTTP 201)</pre></td>
      <td>El registro se agrega al arreglo local del store sin recargar la página. La generación y descarga del archivo PDF o Excel se realiza completamente en el cliente con jsPDF.</td>
    </tr>
    <tr>
      <td><code>/generated_reports/{id}</code></td>
      <td>Eliminar un reporte generado del historial</td>
      <td><code>http://localhost:3000/api/v1/generated_reports/{id}</code></td>
      <td><code>DELETE</code></td>
      <td><code>DELETE /api/v1/generated_reports/DmNMTQ6</code></td>
      <td><code>id</code> en la URL</td>
      <td><pre>{} (HTTP 200)</pre></td>
      <td>El store filtra el arreglo local eliminando el registro correspondiente. La acción requiere confirmación previa del usuario mediante un diálogo de confirmación.</td>
    </tr>
  </tbody>
  <tbody>
  <tr>
    <td><code>/roles</code></td>
    <td>Obtener los roles disponibles del sistema</td>
    <td><code>http://localhost:3001/api/v1/roles</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/roles</code></td>
    <td>No requiere parámetros</td>
    <td><pre>[
  {
    "id": "4afbd60b-8da6-46a6-9b48-2d04b8fa2161",
    "code": "supervisor",
    "name": "Supervisor",
    "description": "Valida alertas, tickets y estado operativo de planta"
  }
]</pre></td>
    <td>El frontend usa este endpoint para identificar el rol del usuario autenticado y mostrar el panel correspondiente: supervisor, administrador u operario de planta.</td>
  </tr>

  <tr>
    <td><code>/users</code></td>
    <td>Obtener usuarios registrados para validar credenciales</td>
    <td><code>http://localhost:3001/api/v1/users</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/users</code></td>
    <td>No requiere parámetros</td>
    <td><pre>[
  {
    "id": "e5e103d0-1f8e-4b27-8dd3-03a71651b344",
    "roleId": "4afbd60b-8da6-46a6-9b48-2d04b8fa2161",
    "fullName": "Supervisor Turno Alpha",
    "email": "supervisor@riskguard.tech",
    "password": "Risk123",
    "status": "active",
    "failedAttempts": 0,
    "blockedUntil": null
  }
]</pre></td>
    <td>El store de autenticación consulta los usuarios para validar correo, contraseña, estado de cuenta, intentos fallidos y rol asignado. La contraseña se usa solo para simulación con json-server.</td>
  </tr>

  <tr>
    <td><code>/users/{id}</code></td>
    <td>Actualizar intentos fallidos, bloqueo o estado del usuario</td>
    <td><code>http://localhost:3001/api/v1/users/{id}</code></td>
    <td><code>PUT</code></td>
    <td><code>PUT /api/v1/users/e5e103d0-1f8e-4b27-8dd3-03a71651b344</code></td>
    <td><code>id</code> en la URL. Body con el usuario completo actualizado.</td>
    <td><pre>{
  "id": "e5e103d0-1f8e-4b27-8dd3-03a71651b344",
  "status": "blocked",
  "failedAttempts": 5,
  "blockedUntil": "2026-05-16T01:20:00.000Z"
}</pre></td>
    <td>Cuando el usuario falla sus credenciales, el frontend incrementa <code>failedAttempts</code>. Si llega a 5 intentos, cambia el estado a <code>blocked</code> y registra la fecha de desbloqueo.</td>
  </tr>

  <tr>
    <td><code>/sessions</code></td>
    <td>Registrar una nueva sesión al iniciar sesión correctamente</td>
    <td><code>http://localhost:3001/api/v1/sessions</code></td>
    <td><code>POST</code></td>
    <td><code>POST /api/v1/sessions</code></td>
    <td>Body con datos de sesión generados en el frontend usando <code>uuid</code>.</td>
    <td><pre>{
  "id": "11cc99b8-30b9-4f97-9cca-2e7d9d0dc54a",
  "userId": "e5e103d0-1f8e-4b27-8dd3-03a71651b344",
  "token": "RG-0f1f137f-016f-4e92-b3ab-81c5f78cc04b",
  "createdAt": "2026-05-16T01:08:28.306Z",
  "lastActivityAt": "2026-05-16T01:08:28.306Z",
  "isValid": true,
  "closedAt": null,
  "closeReason": ""
}</pre></td>
    <td>El frontend crea una sesión fake para representar que el usuario inició sesión. El token no se muestra al usuario; solo queda como dato interno de simulación.</td>
  </tr>

  <tr>
    <td><code>/sessions/{id}</code></td>
    <td>Actualizar una sesión al cerrar sesión o expirar por inactividad</td>
    <td><code>http://localhost:3001/api/v1/sessions/{id}</code></td>
    <td><code>PUT</code></td>
    <td><code>PUT /api/v1/sessions/11cc99b8-30b9-4f97-9cca-2e7d9d0dc54a</code></td>
    <td><code>id</code> en la URL. Body con la sesión completa actualizada.</td>
    <td><pre>{
  "id": "11cc99b8-30b9-4f97-9cca-2e7d9d0dc54a",
  "isValid": false,
  "closedAt": "2026-05-16T01:08:29.668Z",
  "closeReason": "manual-logout"
}</pre></td>
    <td>Al cerrar sesión, el store cambia <code>isValid</code> a <code>false</code>. También se usa para registrar el cierre automático por inactividad con <code>session-expired-by-inactivity</code>.</td>
  </tr>

  <tr>
    <td><code>/accessLogs</code></td>
    <td>Registrar auditoría de accesos e intentos de autenticación</td>
    <td><code>http://localhost:3001/api/v1/accessLogs</code></td>
    <td><code>POST</code></td>
    <td><code>POST /api/v1/accessLogs</code></td>
    <td>Body con datos del intento de acceso generado en el frontend usando <code>uuid</code>.</td>
    <td><pre>{
  "id": "9efd03c7-d6ce-4d4c-9ce4-be8682d70a15",
  "userId": "e5e103d0-1f8e-4b27-8dd3-03a71651b344",
  "email": "supervisor@riskguard.tech",
  "attemptAt": "2026-05-16T01:08:28.384Z",
  "wasSuccessful": true,
  "ipAddress": "192.168.1.15",
  "failureReason": ""
}</pre></td>
    <td>Este endpoint registra intentos exitosos, credenciales incorrectas, cuentas bloqueadas, correos no registrados y cierres de sesión para mantener trazabilidad del acceso.</td>
  </tr>
</tbody>
<tbody>
  <tr>
    <td><code>/heatMapZones</code></td>
    <td>Listar sectores y datos del mapa de calor</td>
    <td><code>http://localhost:3002/api/v1/heatMapZones</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/heatMapZones</code></td>
    <td>No requiere parámetros</td>
    <td><pre>[
  {
    "id": 1,
    "code": "SEC-001",
    "name": "Calderas",
    "description": "Sector de calderas y sistemas de presion.",
    "heatIndex": 94,
    "riskLevel": "Critico",
    "status": "Activo"
  }
]</pre></td>
    <td>El frontend usa este recurso para cargar el mapa de sectores, el mapa de calor y el contador de sectores totales. Cada sector incluye su nivel de riesgo, estado operativo y datos descriptivos.</td>
  </tr>

  <tr>
    <td><code>/heatMapZones</code></td>
    <td>Registrar nuevo sector operativo</td>
    <td><code>http://localhost:3002/api/v1/heatMapZones</code></td>
    <td><code>POST</code></td>
    <td><code>POST /api/v1/heatMapZones</code></td>
    <td>Body: <code>{ "code", "name", "description", "heatIndex", "riskLevel", "status" }</code></td>
    <td><pre>{
  "id": 6,
  "code": "SEC-006",
  "name": "Hornos",
  "description": "Sector de hornos industriales.",
  "heatIndex": 0,
  "riskLevel": "Bajo",
  "status": "Activo"
}</pre></td>
    <td>Permite crear sectores desde la sección Mapa de Sectores. El código del sector se genera automáticamente en el frontend antes de enviar el registro al fake API.</td>
  </tr>

  <tr>
    <td><code>/heatMapZones/{id}</code></td>
    <td>Actualizar datos de un sector</td>
    <td><code>http://localhost:3002/api/v1/heatMapZones/{id}</code></td>
    <td><code>PUT</code></td>
    <td><code>PUT /api/v1/heatMapZones/1</code></td>
    <td><code>id</code> en la URL. Body con los datos actualizados del sector.</td>
    <td><pre>{
  "id": 1,
  "code": "SEC-001",
  "name": "Calderas Norte",
  "description": "Sector actualizado.",
  "heatIndex": 94,
  "riskLevel": "Critico",
  "status": "Activo"
}</pre></td>
    <td>Se utiliza para editar el nombre, descripción y estado del sector. El código permanece como dato de referencia y no se modifica desde el formulario.</td>
  </tr>

  <tr>
    <td><code>/tickets</code></td>
    <td>Listar tickets de acción correctiva</td>
    <td><code>http://localhost:3002/api/v1/tickets</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/tickets</code></td>
    <td>No requiere parámetros. Los filtros por sector, riesgo y estado se aplican en el frontend.</td>
    <td><pre>[
  {
    "id": 1,
    "code": "T-001",
    "sector": "Calderas",
    "assetName": "Caldera B-12",
    "incidentType": "Fuga de presion",
    "riskLevel": "Critico",
    "assignedTechnician": "",
    "status": "Pendiente",
    "slaStatus": "En tiempo"
  }
]</pre></td>
    <td>Este endpoint alimenta la Bandeja de Tickets y el dashboard. El frontend muestra los tickets pendientes, en progreso, el estado SLA y permite ingresar a la asignación de técnico.</td>
  </tr>

  <tr>
    <td><code>/tickets/{id}</code></td>
    <td>Asignar o reasignar técnico a un ticket</td>
    <td><code>http://localhost:3002/api/v1/tickets/{id}</code></td>
    <td><code>PUT</code></td>
    <td><code>PUT /api/v1/tickets/1</code></td>
    <td><code>id</code> en la URL. Body con el ticket actualizado.</td>
    <td><pre>{
  "id": 1,
  "code": "T-001",
  "sector": "Calderas",
  "assignedTechnician": "Luis Carpio",
  "requiredSpecialty": "Calderas",
  "assignmentDetails": "Revisar valvula principal.",
  "status": "En Progreso"
}</pre></td>
    <td>Se usa cuando el supervisor asigna una acción correctiva. Al guardar, el ticket queda asociado a un técnico y su estado cambia a En Progreso.</td>
  </tr>

  <tr>
    <td><code>/technicians</code></td>
    <td>Listar técnicos disponibles</td>
    <td><code>http://localhost:3002/api/v1/technicians</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/technicians</code></td>
    <td>No requiere parámetros</td>
    <td><pre>[
  {
    "id": 1,
    "code": "TEC-01",
    "firstName": "Ana",
    "lastName": "Paredes",
    "fullName": "Ana Paredes",
    "specialty": "Mecanica industrial",
    "status": "Activo"
  }
]</pre></td>
    <td>El frontend usa esta información en el Directorio Técnico y en el formulario de asignación de tickets, mostrando principalmente técnicos activos.</td>
  </tr>

  <tr>
    <td><code>/technicians</code></td>
    <td>Registrar nuevo técnico</td>
    <td><code>http://localhost:3002/api/v1/technicians</code></td>
    <td><code>POST</code></td>
    <td><code>POST /api/v1/technicians</code></td>
    <td>Body: <code>{ "code", "firstName", "lastName", "fullName", "specialty", "email", "phone", "status" }</code></td>
    <td><pre>{
  "id": 4,
  "code": "TEC-04",
  "firstName": "Diego",
  "lastName": "Ramos",
  "fullName": "Diego Ramos",
  "specialty": "Electricidad",
  "status": "Activo"
}</pre></td>
    <td>Permite crear técnicos desde el Directorio Técnico. El código se asigna automáticamente y el nuevo técnico puede aparecer luego en la lista de asignación de tickets.</td>
  </tr>

  <tr>
    <td><code>/technicians/{id}</code></td>
    <td>Actualizar datos de un técnico</td>
    <td><code>http://localhost:3002/api/v1/technicians/{id}</code></td>
    <td><code>PUT</code></td>
    <td><code>PUT /api/v1/technicians/1</code></td>
    <td><code>id</code> en la URL. Body con los datos actualizados del técnico.</td>
    <td><pre>{
  "id": 1,
  "code": "TEC-01",
  "firstName": "Ana",
  "lastName": "Paredes",
  "fullName": "Ana Paredes",
  "specialty": "Mecanica industrial",
  "status": "Activo"
}</pre></td>
    <td>Se utiliza para editar datos del técnico. El código técnico se mantiene bloqueado en la interfaz para conservar la trazabilidad.</td>
  </tr>

  <tr>
    <td><code>/assets</code></td>
    <td>Listar activos industriales</td>
    <td><code>http://localhost:3002/api/v1/assets</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/assets</code></td>
    <td>No requiere parámetros</td>
    <td><pre>[
  {
    "id": 1,
    "name": "Caldera de Vapor",
    "code": "ACT-001",
    "brand": "Fulton",
    "sector": "Calderas",
    "riskLevel": "Critico",
    "lastReview": "2026-03-15",
    "status": "Critico"
  }
]</pre></td>
    <td>Alimenta la sección Gestión de Activos y el contador de activos totales mostrado también en Mapa de Sectores.</td>
  </tr>

  <tr>
    <td><code>/assets</code></td>
    <td>Registrar nuevo activo industrial</td>
    <td><code>http://localhost:3002/api/v1/assets</code></td>
    <td><code>POST</code></td>
    <td><code>POST /api/v1/assets</code></td>
    <td>Body: <code>{ "name", "code", "brand", "sector", "riskLevel", "lastReview", "status" }</code></td>
    <td><pre>{
  "id": 5,
  "name": "Compresor Industrial",
  "code": "ACT-005",
  "brand": "Atlas Copco",
  "sector": "Ensamblaje",
  "riskLevel": "Medio",
  "lastReview": "2026-05-15",
  "status": "Operativo"
}</pre></td>
    <td>Permite registrar activos desde Gestión de Activos. El código se genera automáticamente y no es ingresado manualmente por el usuario.</td>
  </tr>

  <tr>
    <td><code>/assets/{id}</code></td>
    <td>Actualizar datos o estado de un activo</td>
    <td><code>http://localhost:3002/api/v1/assets/{id}</code></td>
    <td><code>PUT</code></td>
    <td><code>PUT /api/v1/assets/3</code></td>
    <td><code>id</code> en la URL. Body con el activo actualizado.</td>
    <td><pre>{
  "id": 3,
  "name": "Tanque de Acido Sulfurico",
  "code": "ACT-003",
  "brand": "ChemTank",
  "sector": "Quimicos",
  "riskLevel": "Alto",
  "lastReview": "2026-05-18",
  "status": "Operativo"
}</pre></td>
    <td>Se usa para editar activos, pasarlos a mantenimiento o reactivarlos. Al reactivar un activo, la fecha de última revisión se actualiza con la fecha de reactivación del mantenimiento.</td>
  </tr>

  <tr>
    <td><code>/preventiveMaintenances</code></td>
    <td>Listar mantenimientos preventivos</td>
    <td><code>http://localhost:3002/api/v1/preventiveMaintenances</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/preventiveMaintenances</code></td>
    <td>No requiere parámetros</td>
    <td><pre>[
  {
    "id": 3,
    "assetId": 3,
    "assetName": "Tanque de Acido Sulfurico",
    "technician": "Luis Carpio",
    "scheduledDate": "2026-05-14",
    "reactivationDate": "2026-05-18",
    "status": "En Mantenimiento"
  }
]</pre></td>
    <td>Permite conocer qué activos tienen mantenimiento programado, finalizado o activo. Se usa para decidir si un activo debe mostrar acción de edición o reactivación.</td>
  </tr>

  <tr>
    <td><code>/preventiveMaintenances</code></td>
    <td>Programar mantenimiento preventivo</td>
    <td><code>http://localhost:3002/api/v1/preventiveMaintenances</code></td>
    <td><code>POST</code></td>
    <td><code>POST /api/v1/preventiveMaintenances</code></td>
    <td>Body: <code>{ "assetId", "assetName", "technician", "scheduledDate", "reactivationDate", "description", "status" }</code></td>
    <td><pre>{
  "id": 4,
  "assetId": 2,
  "assetName": "Brazo Robotico",
  "technician": "Ana Paredes",
  "scheduledDate": "2026-05-20",
  "reactivationDate": "2026-05-22",
  "description": "Revision preventiva.",
  "status": "En Mantenimiento"
}</pre></td>
    <td>Se ejecuta al programar mantenimiento desde Gestión de Activos. Además del registro del mantenimiento, el frontend actualiza el estado del activo a Mantenimiento.</td>
  </tr>

  <tr>
    <td><code>/preventiveMaintenances/{id}</code></td>
    <td>Actualizar estado de mantenimiento</td>
    <td><code>http://localhost:3002/api/v1/preventiveMaintenances/{id}</code></td>
    <td><code>PUT</code></td>
    <td><code>PUT /api/v1/preventiveMaintenances/3</code></td>
    <td><code>id</code> en la URL. Body con el mantenimiento actualizado.</td>
    <td><pre>{
  "id": 3,
  "assetId": 3,
  "assetName": "Tanque de Acido Sulfurico",
  "technician": "Luis Carpio",
  "scheduledDate": "2026-05-14",
  "reactivationDate": "2026-05-18",
  "status": "Finalizado",
  "finishedAt": "2026-05-18T10:30:00.000Z"
}</pre></td>
    <td>Se utiliza cuando el supervisor reactiva un activo. El mantenimiento pasa a Finalizado y el activo vuelve a estado Operativo.</td>
  </tr>

  <tr>
    <td><code>/archivedReports</code></td>
    <td>Listar reportes archivados de cumplimiento</td>
    <td><code>http://localhost:3002/api/v1/archivedReports</code></td>
    <td><code>GET</code></td>
    <td><code>GET /api/v1/archivedReports</code></td>
    <td>No requiere parámetros. El filtrado por sector y rango de fechas se aplica en el frontend.</td>
    <td><pre>[
  {
    "id": 1,
    "heatMapId": 2,
    "code": "INC-110",
    "ticketCode": "T-010",
    "date": "2025-10-24",
    "sector": "Quimicos",
    "status": "Cerrado",
    "documentUrl": "/reports/T-010.pdf"
  }
]</pre></td>
    <td>Este recurso alimenta la sección Reportes y Cumplimiento. El frontend filtra los reportes por sector, permite seleccionar Todos y muestra reportes de incidentes resueltos en un intervalo de fechas.</td>
  </tr>
</tbody>


</table>

**Capturas de Interacción con Datos de Muestra**
<h5 align="center">GET /api/v1/kpi_dashboard</h5>

<p align="center">
  <img src="https://i.postimg.cc/zGRvRNXh/Captura-de-pantalla-2026-05-15-145344.png" width="500"/>
</p>

*Respuesta del endpoint con los cuatro indicadores KPI. Los estados `alert` y `danger` se visualizan en el dashboard mediante tags de color.*

<h5 align="center">GET /api/v1/historical_trends</h5>

<p align="center">
  <img src="https://i.postimg.cc/MGpQM44g/Captura-de-pantalla-2026-05-15-150618.png" width="500"/>
</p>

*Retorno de la evolución mensual de incidentes. Los datos se filtran por sector en el frontend para construir los datasets de la gráfica de línea.*

<h5 align="center">GET /api/v1/critical_alerts</h5>

<p align="center">
  <img src="https://i.postimg.cc/0QCLKQBw/Captura-de-pantalla-2026-05-15-152655.png" width="500"/>
</p>

*Listado de alertas críticas con estado `unresolved`. El frontend calcula el KPI de sectores críticos a partir de estos registros.*

<h5 align="center">PATCH /api/v1/critical_alerts/ALERT_001</h5>

<p align="center">
  <img src="https://i.postimg.cc/prwY2QBx/Whats-App-Image-2026-05-15-at-3-31-04-PM.jpg" width="500"/>
</p>

*Actualización del estado de la alerta a `resolved`. El store recalcula automáticamente los KPIs tras recibir la respuesta.*

<h5 align="center">DELETE /api/v1/critical_alerts/ALERT_001</h5>

<p align="center">
  <img src="https://i.postimg.cc/2590sZM2/Whats-App-Image-2026-05-15-at-3-33-34-PM.jpg" width="500"/>
</p>

*Eliminación de la alerta. Respuesta HTTP 200 con body vacío `{}`.*

<h5 align="center">GET /api/v1/annual_ohs_plan</h5>

<p align="center">
  <img src="https://i.postimg.cc/YCnN0wRy/Whats-App-Image-2026-05-15-at-3-35-29-PM.jpg" width="500"/>
</p>

*Plan anual con cumplimiento global del 72%, por debajo de la meta del 80%. El frontend muestra el indicador en amarillo con etiqueta "Aceptable".*

<h5 align="center">GET /api/v1/predictive_indicators</h5>

<p align="center">
  <img src="https://i.postimg.cc/yYrWSYq7/Whats-App-Image-2026-05-15-at-3-37-08-PM.jpg" width="500"/>
</p>

*Indicadores predictivos con sectores de tendencia creciente. `WAREHOUSE_B` aparece con tag rojo (`critical`) y `GAS_PLANT` con tag amarillo (`warning`).*

<h5 align="center">GET /api/v1/historical_incident_records</h5>

<p align="center">
  <img src="https://i.postimg.cc/5t9CwKPR/Whats-App-Image-2026-05-15-at-3-46-25-PM.jpg" width="500"/>
</p>

*Historial de incidentes de solo lectura. El frontend aplica filtros por sector, tipo y rango de fechas sobre los datos ya cargados.*

<h5 align="center">GET /api/v1/generated_reports</h5>

<p align="center">
  <img src="https://i.postimg.cc/WzFCWn4f/Whats-App-Image-2026-05-15-at-3-39-33-PM.jpg" width="500"/>
</p>

*Listado de reportes generados con tipo `monthly` y formato PDF.*

<h5 align="center">POST /api/v1/generated_reports</h5>

<p align="center">
  <img src="https://i.postimg.cc/8PBQqZHm/Whats-App-Image-2026-05-15-at-3-41-08-PM.jpg" width="500"/>
</p>

*Registro de un nuevo reporte. El servidor retorna HTTP 201 con el id generado automáticamente. El store agrega el registro al historial sin recargar la página.*

<h5 align="center">DELETE /api/v1/generated_reports/Z4PRqZP</h5>

<p align="center">
  <img src="https://i.postimg.cc/9MVyNFF1/Whats-App-Image-2026-05-15-at-3-43-05-PM-(1).jpg" width="500"/>
</p>

*Eliminación del reporte con id `Z4PRqZP`. Respuesta HTTP 200 con body vacío `{}`.*
#### 5.2.2.7.Software Deployment Evidence for Sprint Review.

Durante el Sprint 2 se realizó el despliegue completo de la aplicación RiskGuard, tanto del frontend como del backend simulado. El frontend, desarrollado en Vue 3 con Vite, fue desplegado  en  Vercel y Firebase

#### Despliegue de Firebase + render  para Reportes y Cumplimiento
Firebase Hosting. El backend simulado con json-server fue desplegado en **Render**, exponiendo los endpoints REST consumidos por la aplicación.
Backend – Render
Se creó un repositorio independiente con el archivo `db.json` y el `package.json` configurado con el comando de inicio:

<p align="center">
  <img src="https://i.postimg.cc/52dmYFXh/Whats-App-Image-2026-05-15-at-8-51-24-PM-(2).jpg" width="500"/>
</p>

El servicio fue desplegado como un Web Service en Render, obteniendo la URL base:
`https://db-server-risk-2.onrender.com`
Los endpoints disponibles incluyen: `/kpi_dashboard`, `/critical_alerts`, `/predictive_indicators`, `/generated_reports`, `/monthly_reports`, `/historical_incident_records`, `/historical_trends` y `/annual_ohs_plan`.

<p align="center">
  <img src="https://i.postimg.cc/g0fMDBjY/Whats-App-Image-2026-05-15-at-9-12-09-PM.jpg" width="500"/>
</p>

Luego creamos nuestro proyecto en firebase 
<p align="center">
  <img src="https://i.postimg.cc/pLbBhnm3/Whats-App-Image-2026-05-15-at-8-58-51-PM.jpg" width="500"/>
</p>

Luego ejecutamos los siguientes comandos para el despliegue:

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
npm run build
firebase deploy
```
<p align="center">
  <img src="https://i.postimg.cc/7Z8NGT5d/Whats-App-Image-2026-05-15-at-8-58-15-PM.jpg" width="500"/>
</p>

El directorio de publicación fue configurado como `dist` en `firebase.json`, y la aplicación fue configurada como Single Page App (SPA). La URL de producción obtenida fue:
Boundend context : Reportes y cumplimiento

https://riskguard-7fe11.web.app
#### 5.2.2.8.Team Collaboration Insights during Sprint
