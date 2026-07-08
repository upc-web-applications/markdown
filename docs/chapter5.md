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

 A partir del Sprint 2, el equipo adoptó plenamente el flujo de ramas feature, desarrollando cada bounded context de forma independiente antes de integrarlo mediante pull request.

Las ramas feature utilizadas durante el Sprint 2 fueron:

- `feature/reports_cumplimiento`  
- `feature/monitoring-dashboard`  
- `feature/inspection_headquarters`  
- `feature/assessment_mitigation`  
- `feature/user-authentication`

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
- Todas las imágenes contienen el atributo `alt` con descripciónes relevantes.  
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
En esta sección se describe la configuración del despliegue del proyecto, detallando los pasos necesarios para lograr la publicación del producto a partir de su repositorio de código fuente..

**GitHub Pages**  
Utilizado para la publicación del Landing Page de RiskGuard durante el Sprint 1.

1. Utilizar la rama `main` como fuente del despliegue.  
2. Acceder a la configuración del repositorio en GitHub.  
3. Ingresar a la sección **Pages** dentro de *Settings*.  
4. Seleccionar la rama `main` como origen de publicación.  
5. Guardar la configuración para habilitar la generación automática del sitio.
   
**Vercel**  
Utilizado para el despliegue del Landing Page durante el Sprint 1 y Sprint 2.

1. Vincular el repositorio de GitHub con la cuenta de Vercel.  
2. Importar el proyecto desde el repositorio.  
3. Configurar el entorno de despliegue (Vite).  
4. Definir la rama `main` como fuente.  
5. Habilitar el despliegue automático del sitio.

**Firebase Hosting**  
Utilizado para el despliegue de la Web Application (frontend Vue 3) a partir del Sprint 2.

1. Instalar Firebase CLI: `npm install -g firebase-tools`.  
2. Autenticarse con `firebase login`.  
3. Ejecutar `firebase init hosting` en la raíz del proyecto y seleccionar el proyecto `riskguard-7fe11`.  
4. Configurar el directorio público como `dist` y habilitar la opción de Single Page App.  
5. Generar el build de producción con `npm run build`.  
6. Desplegar con `firebase deploy`.  

La aplicación queda disponible en: `https://riskguard-7fe11.web.app`

**Render**  
Utilizado para el despliegue del servidor de datos simulado (json-server) a partir del Sprint 2.

1. Crear una cuenta en Render (`render.com`).  
2. Conectar la cuenta de GitHub con Render.  
3. Crear un nuevo **Web Service** y seleccionar el repositorio del backend.  
4. Configurar los parámetros de despliegue:  
   - **Build Command:** `npm install`  
   - **Start Command:** `npm start`  
5. Asegurarse de que el `package.json` incluya el script de inicio:  
   ```json
   "start": "json-server --watch db.json --routes routes.json --port 3000 --host 0.0.0.0"
   ```
6. Hacer clic en **Create Web Service** y esperar que finalice el primer deploy.

Una vez desplegados ambos servicios, las actualizaciones se gestionan mediante commits y merges hacia la rama principal (`main`), siguiendo el flujo GitFlow definido por el equipo. Cada cambio integrado generará automáticamente una nueva versión del producto desplegado, permitiendo que las mejoras y correcciones se reflejen de manera continua.

### 5.1.5. Continuous Improvement

A lo largo de las tres entregas del proyecto (AV1, TB1, AV2), el equipo implementó mejoras continuas basadas en la retroalimentación recibida y en la autoevaluación de cada sprint. A continuación se documentan las principales correcciones y mejoras aplicadas:

**Entrega AV1 → TB1:**

1. **Corrección de nomenclatura de User Stories**: Se estandarizó el formato de identificación de User Stories y Technical Stories (US01-US66, TS01-TS20) eliminando guiones y espacios, y se aseguró la consistencia en todos los capítulos del informe.

2. **Actualización del Registro de Versiones**: Se agregó la fila correspondiente a TB1 en la tabla de versiones del informe, documentando la fecha (16/05/2026) y los autores de los cambios.

3. **Mejora de la sección Collaboration Insights**: Se incorporaron capturas de pantalla del repositorio GitHub mostrando el historial de commits por autor y las estadísticas de contribución por miembro del equipo.

4. **Completitud de User Stories**: Se completaron todas las historias de usuario pendientes, alcanzando un total de 66 User Stories y 20 Technical Stories organizadas en 6 épicas, cubriendo la totalidad del alcance definido en el Lean UX Canvas.

**Entrega TB1 → AV2:**

1. **Reemplazo de Fake API por Web Services reales**: En el Sprint 3, se migró completamente la infraestructura de datos de json-server (Fake API) a un backend real implementado en C# con ASP.NET Core 8, Entity Framework Core, MySQL y autenticación JWT, eliminando la dependencia de datos simulados.

2. **Implementación de Code Reviews**: A partir del Sprint 3, se estableció un proceso de revisiones de código mediante Pull Requests, donde cada integración de ramas feature fue revisada por al menos un miembro del equipo antes de ser fusionada a develop.

3. **Mejora de la tabla Development Evidence**: Se reemplazó la columna "Commited on (Date)" por "Evidence URL" en las tablas de evidencia de commits de los tres sprints, proporcionando enlaces directos a cada commit en GitHub.

4. **Corrección de ortografía y tildes**: Se realizó una revisión exhaustiva de la ortografía en todos los capítulos del informe, corrigiendo más de 50 palabras con tildes faltantes y errores gramaticales.

5. **Reemplazo de imágenes externas por recursos locales**: Todas las imágenes alojadas en servicios externos (postimg.cc, postimage.me) fueron descargadas y referenciadas localmente desde `docs/images/`, eliminando la dependencia de servidores externos para la visualización del informe.

6. **Corrección de numeración de secciones**: Se corrigió la numeración de la sección Sprint 3 (de 5.2.2 a 5.2.3) y la sección de Registro de Entrevistas (de 5.3.2 a 2.2.2). Se unificó el formato de la tabla del Sprint Backlog 3 para que sea consistente con los sprints anteriores.

7. **Mejora de la sección Student Outcome**: Se agregaron las evidencias correspondientes a la entrega AV2 para cada criterio del Student Outcome 5 (ABET), documentando las contribuciones de cada miembro del equipo en los tres sprints del proyecto.

8. **Estandarización de mayúsculas**: Se unificó el uso de mayúsculas en términos como "Landing Page" y "Sprint Goal" en todo el documento, eliminando las inconsistencias identificadas en la revisión.

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. *Sprint Planning 1*

En este Sprint 1, el equipo se centró en el desarrollo de la Landing Page de RiskGuard, con el objetivo de presentar de manera clara y atractiva la propuesta de valor del sistema. Se trabajaron secciones clave como la sección principal, características, cómo funciona, segmentos, estadísticas y contacto, organizando el trabajo por secciones para facilitar la colaboración entre los integrantes y lograr una integración ordenada del sitio.

| **Campo** | **Detalle** |
|----------|------------|
| Sprint # | 1 |
| Date | 2026-04-12 |
| Time | 4:00 PM |
| Location | Reunión virtual (Google Meet / Zoom) |
| Prepared By | Flores Eusebio, Angel Thyago |
| Attendees (to planning meeting) | Aponte Pablo, Isabel Luisa / Laura Acosta, Victor Jhosef / Blancas Chávez, Carlos Franco / Flores Eusebio, Angel Thyago |
| Sprint n – 1 Review Summary | No aplica. Este es el primer Sprint del proyecto, por lo que no existe un Sprint anterior cuyo resultado pueda ser revisado. |
| Sprint n – 1 Retrospective Summary | No aplica. Al ser el primer Sprint, no se cuenta con una retrospectiva previa. El equipo estableció los acuerdos iniciales de trabajo: uso de GitHub como repositorio central, comunicación por WhatsApp y Google Meet, y distribución de tareas mediante Trello. |
| Sprint Goal | Our focus is on building the Landing Page for RiskGuard to establish the product's digital presence and communicate its value proposition to industrial safety stakeholders. We believe it delivers a clear, professional and responsive web page that effectively conveys the platform's capabilities in industrial risk prevention and occupational health and safety (SST). This will be confirmed when the Landing Page is deployed on GitHub Pages with all planned sections functional, responsive across desktop and mobile devices, and validated by the Product Owner as aligned with the product vision. |
| Sprint n Velocity | 20 SP |
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

En esta sección se presenta el Sprint Backlog correspondiente al Sprint 1 del proyecto, el cual tuvo como objetivo principal implementar la Landing Page de la plataforma RiskGuard y establecer la presencia digital del producto. Durante este Sprint, el equipo desarrolló User Stories relacionadas con la visualización de métricas de impacto predictivo, la interacción con botones de conversión, la presentación de la propuesta de valor y el diseño responsive de la página de aterrizaje orientada a captar potenciales clientes del sector industrial. Asimismo, se realizó la descomposición de cada User Story en tareas técnicas específicas (Work-items/Tasks), permitiendo organizar el trabajo de manera incremental, asignar responsabilidades y realizar el seguimiento del avance del Sprint mediante la herramienta de gestión del proyecto.

**Tablero Trello:** https://trello.com/invite/b/6a33807f046587a11bd72763/ATTId192c77528e7fa368154cbd580aa20c0312D01B0/riskguard

![Trello Sprint 1](images/trello-sprint-1.png)

| User Story ID | Título | Task ID | Descripción | Estimación (hrs) | Asignado a | Status |
|---|---|---|---|---|---|---|
| US16 | Visualización de Métricas de Impacto Predictivo | T01 | Diseñar tarjetas de métricas predictivas con indicadores visuales de siniestralidad, porcentajes de reducción y codificación por color según impacto | 4 | Laura Acosta, Victor Jhosef | Done |
| US16 | Visualización de Métricas de Impacto Predictivo | T02 | Implementar indicadores estadísticos de impacto predictivo con animaciones de conteo, barras de progreso y diseño responsive usando PrimeVue | 6 | Blancas Chávez, Carlos Franco | Done |
| US17 | Interacción con Botones de Conversión | T03 | Implementar registro de eventos de clic en botones de conversión, validación de múltiples interacciones sin errores y compatibilidad cross-device | 5 | Blancas Chávez, Carlos Franco | Done |
| US61 | Identidad y Acceso General | T04 | Diseñar estructura del navbar responsive con logo, menú de navegación y botones de acceso para desktop y móvil | 4 | Flores Thyago, Angel | Done |
| US61 | Identidad y Acceso General | T05 | Implementar navbar funcional con logo corporativo, menú hamburguesa en móvil, enlaces de navegación interna y botón de inicio de sesión | 6 | Blancas Chávez, Carlos Franco | Done |
| US62 | Propuesta de Valor | T06 | Diseñar sección hero principal con título impactante, subtítulo descriptivo, imagen ilustrativa y llamada a la acción alineada a la identidad visual de RiskGuard | 4 | Laura Acosta, Victor Jhosef | Done |
| US62 | Propuesta de Valor | T07 | Implementar sección hero con texto de propuesta de valor, imagen principal optimizada, botones CTA y diseño responsive | 6 | Blancas Chávez, Carlos Franco | Done |
| US63 | Catálogo de Capacidades Técnicas | T08 | Diseñar tarjetas de funcionalidades clave del sistema con íconos representativos, títulos y descripciónes breves por cada módulo | 4 | Aponte Pablo, Isabel Luisa | Done |
| US63 | Catálogo de Capacidades Técnicas | T09 | Implementar grid de funcionalidades con tarjetas interactivas mostrando módulos del sistema: monitoreo, reportes, alertas y cumplimiento SST | 6 | Blancas Chávez, Carlos Franco | Done |
| US64 | Metodología y Validación Social | T10 | Diseñar sección de flujo de pasos ilustrando el proceso operativo del sistema desde el registro de incidentes hasta la resolución y reportes | 4 | Flores Thyago, Angel | Done |
| US64 | Metodología y Validación Social | T11 | Implementar sección "Cómo funciona" con pasos numerados, íconos descriptivos y línea de tiempo visual del proceso de gestión de riesgos | 6 | Blancas Chávez, Carlos Franco | Done |
| US65 | Beneficios por Rol Operativo | T12 | Diseñar tarjetas segmentadas por rol (operario, supervisor, gerente) con beneficios específicos y diferenciación visual por perfil de usuario | 4 | Flores Thyago, Angel | Done |
| US65 | Beneficios por Rol Operativo | T13 | Implementar sección de beneficios por segmento de usuario con tarjetas diferenciadas, íconos por rol y descripción de valor para cada perfil | 6 | Blancas Chávez, Carlos Franco | Done |
| US66 | Cierre y Conversión de Prospectos | T14 | Diseñar sección de cierre con botones de conversión "Iniciar prueba gratuita" y "Hablar con ventas", alineados a la guía de estilo de RiskGuard | 4 | Aponte Pablo, Isabel Luisa | Done |
| US66 | Cierre y Conversión de Prospectos | T15 | Implementar botones CTA de conversión con redirección a formularios de contacto, efectos hover y diseño responsive para desktop y móvil | 6 | Blancas Chávez, Carlos Franco | Done |

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
      <th>Evidence URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>5c9b242</td>
      <td>Add files via upload</td>
      <td>Implementación completa de la Landing Page (estructura HTML, estilos CSS y secciones: inicio, características, cómo funciona, segmentos, estadísticas y contacto)</td>
      <td><a href="https://github.com/upc-web-applications/riskguard-landingpage/commit/5c9b242">Ver commit</a></td>
    </tr>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>57e4417</td>
      <td>docs: deploy github pages</td>
      <td>Configuración y despliegue del proyecto en GitHub Pages</td>
      <td><a href="https://github.com/upc-web-applications/riskguard-landingpage/commit/57e4417">Ver commit</a></td>
    </tr>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>8b240d6</td>
      <td>fix: build</td>
      <td>Se corrigieron errores en la compilación del proyecto</td>
      <td><a href="https://github.com/upc-web-applications/riskguard-landingpage/commit/8b240d6">Ver commit</a></td>
    </tr>
    <tr>
      <td>RiskGuard_LandingPage</td>
      <td>main</td>
      <td>a5f06db</td>
      <td>feat: añadir Readme Landing</td>
      <td>Se agregó el archivo README para la Landing Page de RiskGuard</td>
      <td><a href="https://github.com/upc-web-applications/riskguard-landingpage/commit/a5f06db">Ver commit</a></td>
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
  <img src="images/ch5-img-1.jpg" width="500"/>
</p>

<h5 align="center">Características</h5>
<p align="center">Funciones clave del sistema.</p>

<p align="center">
  <img src="images/ch5-img-2.jpg" width="500"/>
</p>

<h5 align="center">Cómo funciona</h5>
<p align="center">Flujo de uso del sistema.</p>

<p align="center">
  <img src="images/ch5-img-3.jpg" width="500"/>
</p>

<h5 align="center">Segmentos</h5>
<p align="center">Usuarios objetivo.</p>

<p align="center">
  <img src="images/ch5-img-4.jpg" width="500"/>
</p>

<h5 align="center">Estadísticas</h5>
<p align="center">Datos sobre seguridad industrial.</p>

<p align="center">
  <img src="images/ch5-img-5.jpg" width="500"/>
</p>

<h5 align="center">Contactar</h5>
<p align="center">Prueba gratuita o contacto.</p>

<p align="center">
  <img src="images/ch5-img-6.jpg" width="500"/>
</p>

* Video de la Ejecución
  
https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQDBzzayTq6kQIJAhP26LMO3Ad0Nf1A-UaCJg4qfbtvTvh8?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=

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
  <img src="images/ch5-img-7.jpg" width="500"/>
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
  <img src="images/ch5-img-8.jpg" width="500"/>
</p>

<p align="center">
  <img src="images/ch5-img-9.jpg" width="500"/>
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
| Attendees (to planning meeting) | Aponte Pablo, Isabel Luisa / Laura Acosta, Victor Jhosef / Blancas Chávez, Carlos Franco / Flores Eusebio, Angel Thyago |
| Sprint n – 1 Review Summary | Durante el Sprint 1, el equipo completó exitosamente la Landing Page de RiskGuard con todas las secciones planificadas (propuesta de valor, funcionalidades, proceso operativo, segmentos por rol, métricas de impacto y contacto). El Product Owner validó que la página refleja la identidad visual del producto y comunica adecuadamente la propuesta de valor a los tres segmentos objetivo. Se desplegó en GitHub Pages con diseño responsive funcional en desktop y móvil. |
| Sprint n – 1 Retrospective Summary | El equipo identificó como acierto la división clara de tareas de diseño e implementación por sección, lo que permitió avanzar en paralelo. Como oportunidad de mejora, se señaló la necesidad de adoptar GitFlow con ramas feature desde el inicio del siguiente Sprint, ya que en el Sprint 1 se trabajó principalmente sobre main. También se acordó establecer convenciones de commits (Conventional Commits) y mejorar la documentación de los componentes desarrollados. |
| Sprint Goal | Our focus is on developing the frontend interfaces and interactive flows for RiskGuard across the bounded contexts of Account Generation and Authentication, Site / Area and Industrial Asset, Inspection / Unsafe Condition, Risk Assessment (IPERC), Mitigation, Monitoring / Dashboard, and Reports / Compliance. We believe it delivers an organized, realistic and user-centered experience to operators, supervisors and managers by allowing them to interact with the core functionalities of industrial risk prevention and monitoring before backend integration. This will be confirmed when users can seamlessly navigate through the implemented modules, register and monitor incidents, visualize dashboards and reports, and validate the usability and responsiveness of the application across desktop and mobile devices. |
| Sprint n Velocity | 120 SP |
| Sum of Story Points | 115 SP |

#### 5.2.2.2. Aspect Leaders and Collaborators.
En este Sprint, los aspectos corresponden a los principales Bounded Contexts desarrollados para la aplicación RiskGuard. Se asignaron roles de liderazgo y colaboración para cada módulo con el fin de mejorar la organización, distribución de tareas y coordinación entre los integrantes del equipo durante el desarrollo del frontend.

| Miembro del equipo (Apellido, Nombre) | Usuario GitHub | Account Generation and Authentication BC (L/C) | Site / Area and Industrial Asset BC (L/C) | Inspection / Unsafe Condition BC (L/C) | Risk Assessment (IPERC) BC (L/C) | Mitigation BC (L/C) | Monitoring / Dashboard BC (L/C) | Reports / Compliance BC (L/C) |
|--------------------------------------|---------------|-----------------------------------------------|-------------------------------------------|----------------------------------------|----------------------------------|---------------------|----------------------------------|-------------------------------|
| Aponte Pablo, Isabel Luisa | IsabelAponte234 | C | C | C | C | C | C | L |
| Laura Acosta, Victor Jhosef | Zatrynox | C | C| C | L | L | C | C |
| Blancas Chávez, Carlos Franco | CarlosBlancas969 | C | L | L | C | C | C | C |
| Flores Eusebio, Angel Thyago | angelfdevs | L | C | C | C | C | L | C |

#### 5.2.2.3. Sprint Backlog 2.

En esta sección se presenta el Sprint Backlog correspondiente al Sprint 2 del proyecto, el cual tuvo como objetivo principal implementar el frontend completo de la plataforma RiskGuard con integración a una Fake API. Durante este Sprint, el equipo desarrolló User Stories relacionadas con el dashboard ejecutivo de seguridad, la visualización de tendencias de accidentabilidad, la exportación de reportes de auditoría para SUNAFIL, el seguimiento del plan anual de SST, los indicadores predictivos de riesgo, el mapa de calor operativo, la gestión de tickets correctivos con SLA, el mantenimiento preventivo de activos y la generación de reportes de cumplimiento. Asimismo, se realizó la descomposición de cada User Story en tareas técnicas específicas (Work-items/Tasks), permitiendo organizar el trabajo de manera incremental, asignar responsabilidades y realizar el seguimiento del avance del Sprint mediante la herramienta de gestión del proyecto.

**Tablero Trello:** https://trello.com/invite/b/6a33807f046587a11bd72763/ATTId192c77528e7fa368154cbd580aa20c0312D01B0/riskguard

![Trello Sprint 2](images/trello-sprint-2.png)

| User Story ID | Título | Task ID | Descripción | Estimación (hrs) | Asignado a | Status |
|---|---|---|---|---|---|---|
| US01 | Autenticación de Operario | T01 | Implementar pantalla de inicio de sesión RiskGuard con formulario de correo y contraseña | 4 | Flores Eusebio, Angel Thyago | Done |
| US01 | Autenticación de Operario | T02 | Validar formato de correo antes de procesar el inicio de sesión | 4 | Flores Eusebio, Angel Thyago | Done |
| US01 | Autenticación de Operario | T03 | Validar credenciales preconfiguradas del operario desde la Fake API | 5 | Flores Eusebio, Angel Thyago | Done |
| US01 | Autenticación de Operario | T04 | Implementar mensaje de error para correo o contraseña incorrectos | 4 | Flores Eusebio, Angel Thyago | Done |
| US01 | Autenticación de Operario | T05 | Implementar contador de intentos fallidos y bloqueo temporal después de 5 intentos | 5 | Flores Eusebio, Angel Thyago | Done |
| US01 | Autenticación de Operario | T06 | Redirigir al operario autenticado hacia su panel correspondiente según su rol | 4 | Flores Eusebio, Angel Thyago | Done |
| US02 | Cierre de Sesión del Operario | T07 | Implementar botón de cierre de sesión dentro del panel autenticado | 4 | Flores Eusebio, Angel Thyago | Done |
| US02 | Cierre de Sesión del Operario | T08 | Limpiar la sesión activa del usuario al cerrar sesión y redirigir al login | 5 | Flores Eusebio, Angel Thyago | Done |
| US02 | Cierre de Sesión del Operario | T09 | Implementar cierre automático de sesión por inactividad luego de 30 segundos | 5 | Flores Eusebio, Angel Thyago | Done |
| US03 | Registro Rápido de Casi-Accidente | T10 | Implementar formulario completo de inspección con validaciones y envío a fake API | 6 | Blancas Chávez, Carlos Franco | Done |
| US04 | Adjuntar Evidencia Fotográfica al Reporte | T11 | Implementar carga de foto con previsualización y validación de tamaño máximo 5MB | 5 | Blancas Chávez, Carlos Franco | Done |
| US05 | Selección de Sector al Registrar Incidente | T12 | Implementar dropdown de áreas activas filtrado por sede en el formulario de inspección | 5 | Blancas Chávez, Carlos Franco | Done |
| US07 | Selección del Tipo de Incidente | T13 | Implementar dropdown de tipos de incidente con opción "Otro" y campo adicional | 5 | Blancas Chávez, Carlos Franco | Done |
| US08 | Registro de Condición Insegura Vinculada a un Activo | T14 | Implementar dropdown de activos filtrado por área seleccionada | 5 | Blancas Chávez, Carlos Franco | Done |
| US10 | Confirmación de Recepción del Reporte | T15 | Implementar pantalla de detalle de inspección con ticket generado automáticamente | 4 | Blancas Chávez, Carlos Franco | Done |
| US12 | Historial de Reportes del Operario | T16 | Implementar lista de inspecciones con filtros por estado y contador de estadísticas | 5 | Blancas Chávez, Carlos Franco | Done |
| US13 | Consulta del Detalle de un Reporte Enviado | T17 | Implementar vista de detalle de inspección con estado, acción correctiva y foto | 5 | Blancas Chávez, Carlos Franco | Done |
| US14 | Visualización de Alertas Activas en el Sector | T18 | Implementar lista de inspecciones pendientes y en progreso con badges de urgencia | 4 | Blancas Chávez, Carlos Franco | Done |
| US16 | Visualización de Métricas de Impacto Predictivo | T19 | Implementar sección de la Landing Page con tarjetas visuales de indicadores de siniestralidad (50%, 83%, 90.7%) usando PrimeVue y diseño responsive | 6 | Laura Acosta, Victor Jhosef | Done |
| US16 | Visualización de Métricas de Impacto Predictivo | T20 | Consumir endpoint GET /api/v1/predictive_metrics para obtener indicadores de siniestralidad y sincronizarlos reactivamente en el store | 5 | Laura Acosta, Victor Jhosef | Done |
| US16 | Visualización de Métricas de Impacto Predictivo | T21 | Implementar validaciones de carga en menos de 3 segundos, diseño responsive para desktop y móvil, y asegurar visibilidad sin autenticación | 5 | Laura Acosta, Victor Jhosef | Done |
| US17 | Interacción con Botones de Conversión | T22 | Implementar botones "Iniciar prueba gratuita" y "Hablar con ventas" con redirección a formularios y diseño responsive | 5 | Laura Acosta, Victor Jhosef | Done |
| US17 | Interacción con Botones de Conversión | T23 | Consumir endpoint POST /api/v1/conversion_events para registrar clics en botones de conversión y sincronizar con el store | 5 | Laura Acosta, Victor Jhosef | Done |
| US17 | Interacción con Botones de Conversión | T24 | Validar que los botones permitan múltiples clics sin errores y funcionen correctamente en desktop y dispositivos móviles | 4 | Laura Acosta, Victor Jhosef | Done |
| US18 | Visualización de Alerta por Riesgo Recurrente en sector | T25 | Implementar componente de alerta de patrón recurrente con detalle de tipo de riesgo, sector afectado, número de ocurrencias y fecha del primer reporte | 6 | Laura Acosta, Victor Jhosef | Done |
| US18 | Visualización de Alerta por Riesgo Recurrente en sector | T26 | Consumir endpoint GET /api/v1/recurrent_risk_alerts para detectar patrones con más de 3 ocurrencias en 30 días y mostrar en dashboard principal | 5 | Laura Acosta, Victor Jhosef | Done |
| US18 | Visualización de Alerta por Riesgo Recurrente en sector | T27 | Implementar validación del motor de recurrencia: conteo de ocurrencias por tipo y sector en ventana de 30 días, sin generar alertas para menos de 3 ocurrencias | 5 | Laura Acosta, Victor Jhosef | Done |
| US19 | Visualización de Mapa de Calor de Riesgos de la Planta | T28 | Implementar mapa de calor con sectores coloreados por intensidad según concentración de riesgos activos, usando PrimeVue y design tokens | 8 | Laura Acosta, Victor Jhosef | Done |
| US19 | Visualización de Mapa de Calor de Riesgos de la Planta | T29 | Consumir endpoint GET /api/v1/risk_heatmap para obtener concentración de riesgos por sector con actualización automática al registrar o resolver riesgos | 5 | Laura Acosta, Victor Jhosef | Done |
| US19 | Visualización de Mapa de Calor de Riesgos de la Planta | T30 | Implementar vista de detalle al hacer clic en un sector del mapa mostrando lista de riesgos activos con tipo, criticidad y estado; volver al mapa con un clic | 5 | Laura Acosta, Victor Jhosef | Done |
| US19 | Visualización del Mapa de Calor Operativo | T31 | Implementar dashboard principal con KPIs de tickets pendientes, tickets en progreso y mapa de calor por sectores | 6 | Flores Eusebio, Angel Thyago | Done |
| US20 | Notificación de Riesgo Crítico Sin Atender | T32 | Implementar componente de notificación de escalamiento para riesgos críticos sin acción correctiva asignada por más de 24 horas | 5 | Laura Acosta, Victor Jhosef | Done |
| US20 | Notificación de Riesgo Crítico Sin Atender | T33 | Consumir endpoint GET /api/v1/critical_unattended_risks para evaluar periódicamente riesgos críticos sin acción correctiva y sincronizar notificaciones en el store | 5 | Laura Acosta, Victor Jhosef | Done |
| US20 | Notificación de Riesgo Crítico Sin Atender | T34 | Implementar lógica de validación de tiempo transcurrido desde registro del riesgo y evaluar si supera 24 horas sin acción correctiva asignada | 4 | Laura Acosta, Victor Jhosef | Done |
| US21 | Filtrado de Patrones de Riesgo por Tipo de Peligro | T35 | Implementar panel de patrones de riesgo con filtros por tipo de peligro (físico, químico, ergonómico, otros) combinable con selector de sector | 6 | Laura Acosta, Victor Jhosef | Done |
| US21 | Filtrado de Patrones de Riesgo por Tipo de Peligro | T36 | Consumir endpoint GET /api/v1/risk_patterns con parámetros de filtro por tipo de peligro y sector, actualizando resultados reactivamente | 5 | Laura Acosta, Victor Jhosef | Done |
| US21 | Filtrado de Patrones de Riesgo por Tipo de Peligro | T37 | Validar filtros combinados de tipo de peligro y sector, mostrar mensaje informativo cuando no hay patrones para la categoría seleccionada | 4 | Laura Acosta, Victor Jhosef | Done |
| US22 | Visualización de Resumen de Riesgos del Día | T38 | Implementar dashboard de resumen diario con tarjetas de riesgos nuevos, en progreso y resueltos agrupados por sector | 6 | Laura Acosta, Victor Jhosef | Done |
| US22 | Visualización de Resumen de Riesgos del Día | T39 | Consumir endpoint GET /api/v1/daily_risk_summary para obtener conteo de riesgos del día actual agrupados por sector con estado | 5 | Laura Acosta, Victor Jhosef | Done |
| US22 | Visualización de Resumen de Riesgos del Día | T40 | Validar datos del resumen diario y mostrar mensaje "No se han reportado riesgos hoy" cuando no hay registros en el día actual | 4 | Laura Acosta, Victor Jhosef | Done |
| US23 | Marcar Alerta de Patrón Recurrente como Revisada | T41 | Implementar botón "Marcar como revisada" en cada alerta de patrón recurrente del dashboard con transición a sección de revisadas | 4 | Laura Acosta, Victor Jhosef | Done |
| US23 | Marcar Alerta de Patrón Recurrente como Revisada | T42 | Consumir endpoint PATCH /api/v1/recurrent_risk_alerts/:id para actualizar estado de alerta a revisada y recargar panel principal | 5 | Laura Acosta, Victor Jhosef | Done |
| US23 | Marcar Alerta de Patrón Recurrente como Revisada | T43 | Implementar sección de historial de alertas revisadas accesible desde la misma pantalla y mostrar mensaje cuando no hay pendientes | 4 | Laura Acosta, Victor Jhosef | Done |
| US24 | Autenticación Segura de Supervisor | T44 | Implementar pantalla de inicio de sesión RiskGuard con formulario de correo y contraseña | 4 | Flores Eusebio, Angel Thyago | Done |
| US24 | Autenticación Segura de Supervisor | T45 | Validar formato de correo antes de procesar el inicio de sesión | 4 | Flores Eusebio, Angel Thyago | Done |
| US24 | Autenticación Segura de Supervisor | T46 | Validar credenciales preconfiguradas del supervisor desde la Fake API | 5 | Flores Eusebio, Angel Thyago | Done |
| US24 | Autenticación Segura de Supervisor | T47 | Implementar mensaje de error para correo o contraseña incorrectos | 4 | Flores Eusebio, Angel Thyago | Done |
| US24 | Autenticación Segura de Supervisor | T48 | Redirigir al supervisor autenticado hacia su panel correspondiente según su rol | 4 | Flores Eusebio, Angel Thyago | Done |
| US24 | Autenticación Segura de Supervisor | T49 | Implementar pantalla de inicio de sesión para supervisor con formulario de correo y contraseña, diseño RiskGuard y PrimeVue | 5 | Laura Acosta, Victor Jhosef | Done |
| US24 | Autenticación Segura de Supervisor | T50 | Validar formato de correo, consumir endpoint POST /api/v1/auth/login para validar credenciales, implementar contador de 5 intentos fallidos y bloqueo de 15 minutos | 6 | Laura Acosta, Victor Jhosef | Done |
| US24 | Autenticación Segura de Supervisor | T51 | Implementar generación de token de seguridad post-autenticación y redirigir al supervisor a su panel de funciones según su rol | 5 | Laura Acosta, Victor Jhosef | Done |
| US25 | Configuración de Sectores y Áreas Operativas | T52 | Implementar sección Mapa de Sectores con listado, contador de sectores y contador de activos relacionados | 6 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración de Sectores y Áreas Operativas | T53 | Implementar formulario de creación y edición de sectores con código automático, descripción y estado activo/inactivo | 6 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración y Gestión de Activos Industriales | T54 | Implementar sección Gestión de Activos con listado, contador total y acciones por estado operativo | 6 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración y Gestión de Activos Industriales | T55 | Implementar formulario de creación y edición de activos industriales con código automático y campos bloqueados cuando corresponde | 6 | Flores Eusebio, Angel Thyago | Done |
| US25 | Configuración de Sectores y Áreas Operativas | T56 | Implementar módulo de gestión de sectores con tabla de listado, formulario de creación y edición con nombre y descripción, y opción de desactivación | 6 | Laura Acosta, Victor Jhosef | Done |
| US25 | Configuración de Sectores y Áreas Operativas | T57 | Consumir endpoints CRUD /api/v1/sectors para listar, crear, actualizar y desactivar sectores con sincronización en store | 5 | Laura Acosta, Victor Jhosef | Done |
| US25 | Configuración de Sectores y Áreas Operativas | T58 | Validar unicidad de nombre de sector antes de crear, restringir eliminación si tiene historial asociado permitiendo solo desactivación, mostrar mensajes de error | 4 | Laura Acosta, Victor Jhosef | Done |
| US26 | Configuración y Gestión de Activos Industriales | T59 | Implementar módulo de gestión de activos industriales con tabla de listado, formulario de creación/edición vinculado a sector activo y estado operativo | 6 | Laura Acosta, Victor Jhosef | Done |
| US26 | Configuración y Gestión de Activos Industriales | T60 | Consumir endpoints CRUD /api/v1/industrial_assets para gestionar activos con código único, reubicación entre sectores y actualización de estado | 5 | Laura Acosta, Victor Jhosef | Done |
| US26 | Configuración y Gestión de Activos Industriales | T61 | Validar unicidad de código identificador, rechazar registro si sector destino está inactivo, desactivar en lugar de eliminar si tiene historial de inspecciones | 4 | Laura Acosta, Victor Jhosef | Done |
| US27 | Gestión y Administración de Personal Técnico | T62 | Implementar Directorio Técnico con listado de técnicos, especialidad, estado y acción de detalle | 6 | Flores Eusebio, Angel Thyago | Done |
| US27 | Gestión y Administración de Personal Técnico | T63 | Implementar formulario de registro y edición de técnicos con código automático y estado activo/inactivo | 6 | Flores Eusebio, Angel Thyago | Done |
| US27 | Gestión y Administración de Personal Técnico | T64 | Integrar técnicos activos con el formulario de asignación de tickets correctivos | 5 | Flores Eusebio, Angel Thyago | Done |
| US27 | Gestión y Administración de Personal Técnico | T65 | Implementar directorio de personal técnico con listado, formulario de registro y edición con DNI, nombres, especialidad y estado activo/inactivo | 6 | Laura Acosta, Victor Jhosef | Done |
| US27 | Gestión y Administración de Personal Técnico | T66 | Consumir endpoints CRUD /api/v1/technicians para gestionar personal técnico con validación de DNI único y filtro de solo activos para asignación | 5 | Laura Acosta, Victor Jhosef | Done |
| US27 | Gestión y Administración de Personal Técnico | T67 | Validar unicidad de DNI, inhabilitar técnicos con estado "Inactivo" preservando historial de tickets y ocultarlos del selector de asignación | 4 | Laura Acosta, Victor Jhosef | Done |
| US28 | Asignación de Tickets de Acción Correctiva | T68 | Implementar bandeja de tickets con acciones para asignar técnico o visualizar detalle de asignación | 6 | Flores Eusebio, Angel Thyago | Done |
| US28 | Asignación de Tickets de Acción Correctiva | T69 | Implementar formulario de asignación y reasignación de técnico responsable a un ticket | 6 | Flores Eusebio, Angel Thyago | Done |
| US28 | Asignación de Tickets de Acción Correctiva | T70 | Implementar bandeja de tickets con formulario de asignación de técnico responsable, selector de técnicos activos y transición visual de estado | 6 | Laura Acosta, Victor Jhosef | Done |
| US28 | Asignación de Tickets de Acción Correctiva | T71 | Consumir endpoint PATCH /api/v1/tickets/:id/assign para asignar técnico, actualizar estado a "En Progreso" y registrar trazabilidad de reasignaciones | 5 | Laura Acosta, Victor Jhosef | Done |
| US28 | Asignación de Tickets de Acción Correctiva | T72 | Validar selección obligatoria de técnico activo, registrar fecha/hora de asignación y permitir reasignación con historial de cambios | 4 | Laura Acosta, Victor Jhosef | Done |
| US29 | Exploración Sectorizada y Filtrado de Alertas Activas | T73 | Implementar filtros de tickets por sector, nivel de riesgo y estado dentro de la bandeja de tickets | 6 | Flores Eusebio, Angel Thyago | Done |
| US29 | Exploración Sectorizada y Filtrado de Alertas Activas | T74 | Implementar visualización de alertas activas con selector de sector obligatorio y filtros secundarios por nivel de riesgo y estado | 6 | Laura Acosta, Victor Jhosef | Done |
| US29 | Exploración Sectorizada y Filtrado de Alertas Activas | T75 | Consumir endpoint GET /api/v1/sectors/:id/alerts con parámetros de filtro secundario para obtener tickets de incidentes del sector seleccionado | 5 | Laura Acosta, Victor Jhosef | Done |
| US29 | Exploración Sectorizada y Filtrado de Alertas Activas | T76 | Validar selección obligatoria de sector antes de desplegar alertas, mostrar mensaje informativo cuando el sector no tiene alertas activas o filtros sin coincidencias | 4 | Laura Acosta, Victor Jhosef | Done |
| US30 | Verificación y Cierre de Medidas de Control | T77 | Implementar vista de verificación con selección de veredicto (Aprobación/Rechazo), campo de comentario obligatorio en rechazo y diseño de formulario | 6 | Laura Acosta, Victor Jhosef | Done |
| US30 | Verificación y Cierre de Medidas de Control | T78 | Consumir endpoint PATCH /api/v1/tickets/:id/verify para aprobar (estado "Cerrado") o rechazar (revertir a "En Progreso") con registro de marca de tiempo | 5 | Laura Acosta, Victor Jhosef | Done |
| US30 | Verificación y Cierre de Medidas de Control | T79 | Validar que solo tickets en estado "Medida Implementada" puedan verificarse, exigir comentario de justificación en caso de rechazo, actualizar nivel de riesgo del sector | 4 | Laura Acosta, Victor Jhosef | Done |
| US31 | Visualización del Mapa de Calor Operativo | T80 | Implementar mapa de calor operativo con indicadores de criticidad IPERC por sector, clasificación visual por nivel de riesgo y selección de sector para ver tickets activos | 8 | Laura Acosta, Victor Jhosef | Done |
| US31 | Visualización del Mapa de Calor Operativo | T81 | Consumir endpoint GET /api/v1/operational_heatmap para obtener niveles de criticidad IPERC por sector y actualizar indicadores automáticamente al cerrar tickets | 5 | Laura Acosta, Victor Jhosef | Done |
| US31 | Visualización del Mapa de Calor Operativo | T82 | Implementar lógica de disminución automática del nivel de alerta de un sector cuando todos los tickets críticos alcanzan estado "Cerrado" | 5 | Laura Acosta, Victor Jhosef | Done |
| US32 | Notificación Externa Automática por Incidentes Críticos | T83 | Implementar configuración de notificación por correo electrónico con alerta de incidentes críticos y formulario de dirección de destino | 5 | Laura Acosta, Victor Jhosef | Done |
| US32 | Notificación Externa Automática por Incidentes Críticos | T84 | Consumir endpoint POST /api/v1/critical_alerts/notify para enviar notificación por correo al supervisor con ID de ticket, clasificación, sector y marca de tiempo | 5 | Laura Acosta, Victor Jhosef | Done |
| US32 | Notificación Externa Automática por Incidentes Críticos | T85 | Validar que solo incidentes con nivel de riesgo "Crítico" disparen la notificación externa, omitiendo el envío para niveles inferiores | 4 | Laura Acosta, Victor Jhosef | Done |
| US33 | Escalamiento Automático por Incumplimiento de SLA | T86 | Mostrar estado SLA incumplido en tickets vencidos y adaptar el tiempo restante como tiempo excedido | 5 | Flores Eusebio, Angel Thyago | Done |
| US33 | Escalamiento Automático por Incumplimiento de SLA | T87 | Implementar etiqueta "SLA Incumplido" en tickets vencidos, contador de tiempo excedido y notificación de escalamiento a gerencia | 6 | Laura Acosta, Victor Jhosef | Done |
| US33 | Escalamiento Automático por Incumplimiento de SLA | T88 | Consumir endpoint GET /api/v1/tickets/sla_breach para monitorear tickets que superaron su SLA por nivel de riesgo y sincronizar estado en store | 5 | Laura Acosta, Victor Jhosef | Done |
| US33 | Escalamiento Automático por Incumplimiento de SLA | T89 | Implementar asignación de SLA por nivel de riesgo, monitoreo en segundo plano del tiempo transcurrido, registro inmutable de incumplimiento y disparo de notificación gerencial | 6 | Laura Acosta, Victor Jhosef | Done |
| US34 | Programación de Mantenimiento Preventivo de Activos | T90 | Implementar formulario para programar mantenimiento preventivo sobre un activo y actualizar su estado a mantenimiento | 6 | Flores Eusebio, Angel Thyago | Done |
| US34 | Programación de Mantenimiento Preventivo de Activos | T91 | Implementar reactivación de activos en mantenimiento y actualización de la fecha de última revisión | 5 | Flores Eusebio, Angel Thyago | Done |
| US34 | Programación de Mantenimiento Preventivo de Activos | T92 | Implementar formulario de programación de mantenimiento preventivo con selección de activo, técnico responsable, descripción y ventana de tiempo futura | 6 | Laura Acosta, Victor Jhosef | Done |
| US34 | Programación de Mantenimiento Preventivo de Activos | T93 | Consumir endpoints POST /api/v1/preventive_maintenance y PATCH para crear, actualizar estado y cerrar mantenimientos con actualización de estado del activo | 5 | Laura Acosta, Victor Jhosef | Done |
| US34 | Programación de Mantenimiento Preventivo de Activos | T94 | Validar bloqueo de alertas predictivas mientras activo está "En Mantenimiento", reactivación automática al cierre del ticket y registro de fecha de última revisión | 5 | Laura Acosta, Victor Jhosef | Done |
| US35 | Generación y Exportación de Reportes de Cumplimiento | T95 | Implementar sección Reportes y Cumplimiento con reportes por sector, estado y rango de fechas | 6 | Flores Eusebio, Angel Thyago | Done |
| US35 | Generación y Exportación de Reportes de Cumplimiento | T96 | Implementar filtros de reportes por sector, opción Todos, fechas y botón para limpiar filtros | 5 | Flores Eusebio, Angel Thyago | Done |
| US35 | Generación y Exportación de Reportes de Cumplimiento | T97 | Implementar sección de reportes con filtros por rango de fechas, selector de sector, y botones de exportación en PDF y Excel | 6 | Laura Acosta, Victor Jhosef | Done |
| US35 | Generación y Exportación de Reportes de Cumplimiento | T98 | Consumir endpoint GET /api/v1/compliance_reports para obtener datos consolidados de incidentes, nivel de riesgo promedio y tasa de cumplimiento SLA con filtros | 5 | Laura Acosta, Victor Jhosef | Done |
| US35 | Generación y Exportación de Reportes de Cumplimiento | T99 | Validar consistencia del rango de fechas, bloquear consulta si fecha inicio es posterior a fecha fin, generar archivo descargable en PDF con jsPDF y Excel | 6 | Laura Acosta, Victor Jhosef | Done |
| US36 | Autenticación Segura de Gerente o Administrador | T100 | Configurar usuarios demo para administrador, supervisor y operario en db.json | 4 | Flores Eusebio, Angel Thyago | Done |
| US36 | Autenticación Segura de Gerente o Administrador | T101 | Implementar validación de credenciales para usuarios de alta dirección | 5 | Flores Eusebio, Angel Thyago | Done |
| US36 | Autenticación Segura de Gerente o Administrador | T102 | Mostrar panel simple según el rol autenticado: administración, supervisor u operario | 5 | Flores Eusebio, Angel Thyago | Done |
| US37 | Visualización del Dashboard Ejecutivo de Seguridad | T103 | Implementar tarjetas de indicadores clave: incidentes activos, resueltos, sectores críticos y cumplimiento SST | 4 | Aponte Pablo, Isabel Luisa | Done |
| US37 | Visualización del Dashboard Ejecutivo de Seguridad | T104 | Al hacer clic en un KPI, mostrar dialog con listado de sectores y alertas activas; cerrar con un solo clic para volver al dashboard | 4 | Aponte Pablo, Isabel Luisa | Done |
| US38 | Visualización de Tendencias de Accidentabilidad | T105 | Implementar gráfica de línea con evolución mensual de incidentes diferenciada por tipo | 4 | Aponte Pablo, Isabel Luisa | Done |
| US38 | Visualización de Tendencias de Accidentabilidad | T106 | Implementar descarga de la gráfica de tendencias en formato PNG con un solo clic | 4 | Aponte Pablo, Isabel Luisa | Done |
| US39 | Exportación de Formatos de Auditoría para SUNAFIL | T107 | Implementar formulario de exportación con selección de rango de fechas y formato, generación de documento de auditoría en PDF y Excel | 4 | Aponte Pablo, Isabel Luisa | Done |
| US39 | Exportación de Formatos de Auditoría para SUNAFIL | T108 | Implementar historial de reportes generados | 4 | Aponte Pablo, Isabel Luisa | Done |
| US40 | Seguimiento del Cumplimiento del Plan Anual de SST | T109 | Diseñar tarjetas de cumplimiento de actividades del plan anual de SST con indicador de color por porcentaje | 4 | Aponte Pablo, Isabel Luisa | Done |
| US40 | Seguimiento del Cumplimiento del Plan Anual de SST | T110 | Implementar vista con cumplimiento global, actividades completadas, gráfica de evolución mensual, exportación de informe anual PDF y generación de reporte de cumplimiento en PDF o Excel | 5 | Aponte Pablo, Isabel Luisa | Done |
| US41 | Visualización de Indicadores Predictivos de Riesgo | T111 | Diseñar tarjetas de indicadores predictivos | 4 | Aponte Pablo, Isabel Luisa | Done |
| US41 | Visualización de Indicadores Predictivos de Riesgo | T112 | Mostrar indicadores predictivos: sectores con tendencia creciente, tipos recurrentes y tiempo promedio de resolución | 4 | Aponte Pablo, Isabel Luisa | Done |
| US41 | Visualización de Indicadores Predictivos de Riesgo | T113 | Implementar generación y descarga del resumen ejecutivo en PDF | 4 | Aponte Pablo, Isabel Luisa | Done |
| US42 | Notificación de Alerta Crítica No Resuelta a Gerencia | T114 | Implementar tabla con acciones marcar como resuelto y eliminar, con tags de severidad por tipo y estado | 4 | Aponte Pablo, Isabel Luisa | Done |
| US43 | Registro Histórico de Incidentes para Trazabilidad Legal | T115 | Implementar tabla inmutable de incidentes sin opciones de edición para garantizar trazabilidad legal ante SUNAFIL | 5 | Aponte Pablo, Isabel Luisa | Done |
| US43 | Registro Histórico de Incidentes para Trazabilidad Legal | T116 | Implementar filtros de búsqueda por sector, tipo de incidente y rango de fechas con actualización del contador de resultados filtrados | 4 | Aponte Pablo, Isabel Luisa | Done |
| US45 | Generación de Reporte Mensual de Gestión de SST | T117 | Implementar generación y descarga automática del reporte mensual consolidado en PDF con jsPDF | 4 | Aponte Pablo, Isabel Luisa | Done |
| US45 | Generación de Reporte Mensual de Gestión de SST | T118 | Implementar historial de reportes mensuales generados con previsualización en historial, re-descarga y eliminación con confirmación | 5 | Aponte Pablo, Isabel Luisa | Done |
| TS08 | Endpoint para Obtener Indicadores del Dashboard Ejecutivo | T119 | Consumir el endpoint GET /api/v1/kpi_dashboard para obtener los cuatro indicadores KPI y sincronizarlos reactivamente en el store mediante syncKPIs | 5 | Aponte Pablo, Isabel Luisa | Done |
| TS08 | Endpoint para Obtener Tendencias Históricas de Accidentabilidad | T120 | Consumir el endpoint GET /api/v1/historical_trends para obtener la evolución mensual de incidentes y aplicar filtro por sector y por tipo en el frontend | 4 | Aponte Pablo, Isabel Luisa | Done |
| TS10 | Endpoint para Gestión de Reportes Generados | T121 | Consumir los endpoints de reportes generados para listar, registrar y eliminar reportes; la generación del documento PDF o Excel se realiza en el cliente con jsPDF | 4 | Aponte Pablo, Isabel Luisa | Done |
| TS11 | Endpoint para Gestión de Alertas Críticas | T122 | Consumir los endpoints de alertas críticas para listar, actualizar estado y eliminar alertas, con recálculo automático del KPI de sectores críticos tras cada operación | 5 | Aponte Pablo, Isabel Luisa | Done |
| TS12 | Endpoint para Obtener el Plan Anual de SST y su Cumplimiento | T123 | Consumir el endpoint GET /api/v1/annual_ohs_plan para obtener el porcentaje de cumplimiento global y el desglose por sector, y alimentar la vista de seguimiento SST y el KPI del dashboard | 5 | Aponte Pablo, Isabel Luisa | Done |
| - | BC Sede — CRUD completo | T124 | Implementar lista, formulario y detalle de sedes con create, update y delete | 6 | Blancas Chávez, Carlos Franco | Done |
| - | BC Área — CRUD completo | T125 | Implementar lista, formulario y detalle de áreas vinculadas a sede con nivel de riesgo | 6 | Blancas Chávez, Carlos Franco | Done |
| - | BC Activo Industrial — CRUD completo | T126 | Implementar lista, formulario y detalle de activos vinculados a área y sede | 6 | Blancas Chávez, Carlos Franco | Done |
| - | Fake API — db.json | T127 | Crear base de datos fake con datos de sedes, áreas, activos e inspecciones para json-server | 4 | Blancas Chávez, Carlos Franco | Done |
| - | Arquitectura DDD | T128 | Estructurar cada BC con capas domain, infrastructure, application y presentation siguiendo el patrón del curso | 5 | Blancas Chávez, Carlos Franco | Done |
| - | i18n ES/EN | T129 | Implementar internacionalización con vue-i18n para español e inglés con botón de cambio en sidebar | 4 | Blancas Chávez, Carlos Franco | Done |
| - | Diseño dark theme RiskGuard | T130 | Implementar estilos globales con paleta de colores #060D1A, #E8460A usando PrimeVue y PrimeFlex | 5 | Blancas Chávez, Carlos Franco | Done |
| - | Fake API — json-server | T131 | Crear y ajustar db.json con sectores, tickets, técnicos, activos, mantenimientos preventivos y reportes archivados | 5 | Flores Eusebio, Angel Thyago | Done |
| - | Arquitectura DDD del BC Monitoring | T132 | Estructurar el bounded context monitoring-dashboard con capas application, domain, infrastructure y presentation | 6 | Flores Eusebio, Angel Thyago | Done |
| - | Modelos de Dominio y Assemblers | T133 | Crear entidades y assemblers para tickets, sectores, técnicos, activos, mapa de calor y mantenimientos preventivos | 6 | Flores Eusebio, Angel Thyago | Done |
| - | Integración API e Infraestructura | T134 | Implementar MonitoringApi usando BaseApi, BaseEndpoint y variables de entorno para endpoints del fake API | 5 | Flores Eusebio, Angel Thyago | Done |
| - | Navegación y Rutas | T135 | Configurar rutas del bounded context para dashboard, tickets, sectores, técnicos, activos, mantenimiento y reportes | 5 | Flores Eusebio, Angel Thyago | Done |
| - | i18n ES/EN | T136 | Implementar textos principales en español e inglés usando vue-i18n, incluyendo navegación y footer | 5 | Flores Eusebio, Angel Thyago | Done |
| - | Diseño dark theme RiskGuard | T137 | Ajustar estilos globales con tema oscuro, acento naranja, tablas PrimeVue, formularios, sidebar y footer | 6 | Flores Eusebio, Angel Thyago | Done |
| - | Configuración para Deploy | T138 | Preparar variables de entorno para Vercel y API desplegada en Render | 4 | Flores Eusebio, Angel Thyago | Done |
| - | Identity Access — Arquitectura DDD | T139 | Estructurar el bounded context con capas application, domain, infrastructure y presentation | 5 | Flores Eusebio, Angel Thyago | Done |
| - | Identity Access — Entidades de Dominio | T140 | Crear entidades User, Session y AccessLog con nomenclatura en inglés y atributos neutros | 5 | Flores Eusebio, Angel Thyago | Done |
| - | Identity Access — Infrastructure | T141 | Implementar BaseApi, BaseEndpoint, IdentityAccessApi y assemblers siguiendo el estilo de learning-center | 6 | Flores Eusebio, Angel Thyago | Done |
| - | Fake API — Identity Access | T142 | Crear datos fake de roles, usuarios, sesiones y registros de acceso usando uuid | 5 | Flores Eusebio, Angel Thyago | Done |
| - | i18n ES/EN | T143 | Implementar textos en español e inglés para login, validaciones, panel y cierre de sesión | 4 | Flores Eusebio, Angel Thyago | Done |
| - | Diseño RiskGuard | T144 | Adaptar el diseño visual al tema oscuro de RiskGuard con color principal naranja | 5 | Flores Eusebio, Angel Thyago | Done |
| - | Deploy y Configuración | T145 | Configurar variables de entorno para desarrollo y producción con envDir en Vite | 4 | Flores Eusebio, Angel Thyago | Done |
| - | Fake API — json-server | T146 | Crear y ajustar db.json con datos fake de sectores, activos industriales, técnicos, tickets, alertas de recurrencia, mapa de calor, SLA, mantenimientos preventivos y reportes de cumplimiento | 5 | Laura Acosta, Victor Jhosef | Done |
| - | Arquitectura DDD del BC Risk Assessment | T147 | Estructurar el bounded context risk-assessment con capas application, domain, infrastructure y presentation para el motor predictivo y análisis de riesgos | 5 | Laura Acosta, Victor Jhosef | Done |
| - | Arquitectura DDD del BC Incident Mitigation | T148 | Estructurar el bounded context incident-mitigation con capas application, domain, infrastructure y presentation para la gestión de alertas y mitigación | 5 | Laura Acosta, Victor Jhosef | Done |
| - | Modelos de Dominio y Assemblers | T149 | Crear entidades y assemblers para patrones de riesgo, mapa de calor por sector, alertas críticas, SLA, mantenimiento preventivo y reportes de cumplimiento | 5 | Laura Acosta, Victor Jhosef | Done |
| - | Integración API e Infraestructura | T150 | Implementar AssessmentMitigationApi usando BaseApi, BaseEndpoint y variables de entorno para endpoints del fake API en ambos bounded contexts | 4 | Laura Acosta, Victor Jhosef | Done |
| - | Navegación y Rutas | T151 | Configurar rutas de los bounded contexts para landing, dashboard supervisor, sectores, activos, técnicos, tickets, alertas, mantenimiento y reportes con lazy loading | 4 | Laura Acosta, Victor Jhosef | Done |
| - | i18n ES/EN | T152 | Implementar textos en español e inglés usando vue-i18n para todos los módulos de assessment y mitigation | 4 | Laura Acosta, Victor Jhosef | Done |
| - | Diseño dark theme RiskGuard | T153 | Ajustar estilos globales con tema oscuro RiskGuard (#060D1A, #E8460A) y PrimeVue para las nuevas vistas de assessment y mitigation | 4 | Laura Acosta, Victor Jhosef | Done |
| - | Configuración para Deploy | T154 | Preparar variables de entorno para Vercel y API desplegada en Render, configurar envDir en Vite para los bounded contexts de assessment y mitigation | 4 | Laura Acosta, Victor Jhosef | Done |


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
      <th>Evidence URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>4066cfd</td>
      <td>Create index</td>
      <td>Creación del archivo índice del proyecto</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/4066cfd">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>8a88511</td>
      <td>add inspection and headquarters BC</td>
      <td>Agregado bounded context de inspección y sede central</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/8a88511">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>8aa1c72</td>
      <td>fix: rename in english</td>
      <td>Corrección de nombres de archivos y variables al inglés</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/8aa1c72">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>0ebc3b5</td>
      <td>Merge pull request #1 from upc-web-applications/feature/inspection_headquarters</td>
      <td>Fusión de la rama feature/inspection_headquarters al flujo principal</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/0ebc3b5">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>41a4aa4</td>
      <td>feat: upload bc</td>
      <td>Subida del bounded context de evaluación de riesgos</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/41a4aa4">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>b8e45b7</td>
      <td>fix: add</td>
      <td>Corrección y adición de archivos faltantes en el módulo</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/b8e45b7">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/assessment_mitigation</td>
      <td>3570ff1</td>
      <td>fix: add</td>
      <td>Segunda corrección de archivos faltantes en el módulo</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/3570ff1">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/monitoring-dashboard</td>
      <td>5034b80</td>
      <td>monitoring-dashboard bc</td>
      <td>Agregado bounded context del dashboard de monitoreo del supervisor</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/5034b80">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/monitoring-dashboard</td>
      <td>2f1d68a</td>
      <td>update feature/monitoring-dashboard</td>
      <td>Actualización de componentes y vistas del panel de monitoreo</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/2f1d68a">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>b1cc4de</td>
      <td>Merge branch 'main' of Frontend-RiskGuard</td>
      <td>Sincronización con la rama main del repositorio personal</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/b1cc4de">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>f9d6a2c</td>
      <td>feat: add es and en</td>
      <td>Agregado archivos de internacionalización en español e inglés</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/f9d6a2c">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>03a43ab</td>
      <td>feat: add database db</td>
      <td>Agregado archivo de base de datos json-server</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/03a43ab">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>b6b23eb</td>
      <td>feat: add env</td>
      <td>Agregado archivo de variables de entorno del proyecto</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/b6b23eb">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>b3ec027</td>
      <td>feat: add shared</td>
      <td>Agregado componentes y recursos compartidos del módulo</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/b3ec027">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>3415ec1</td>
      <td>feat: add entities</td>
      <td>Agregado entidades del dominio de reportes y cumplimiento SST</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/3415ec1">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>42e7dcf</td>
      <td>feat: add assemblers and api</td>
      <td>Agregado assemblers y servicios de consumo de API</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/42e7dcf">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>4f10c4e</td>
      <td>feat: add store</td>
      <td>Agregado store  para gestión de estado del módulo</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/4f10c4e">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>70fdeae</td>
      <td>feat: add presentation reports styles</td>
      <td>Agregado estilos y estructura visual de las vistas de reportes</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/70fdeae">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>3fcc99b</td>
      <td>feat: add configuration</td>
      <td>Agregado configuración del módulo de reportes y cumplimiento</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/3fcc99b">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>dbeea7d</td>
      <td>fix: correct position</td>
      <td>Corrección de posicionamiento de elementos en la interfaz</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/dbeea7d">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>297db99</td>
      <td>feat: add service pdf and excel</td>
      <td>Agregado servicio de generación de documentos PDF y Excel con jsPDF</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/297db99">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>e0cf4ad</td>
      <td>feat: add new presentation</td>
      <td>Agregado nueva vista de presentación del módulo de reportes</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/e0cf4ad">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>de75928</td>
      <td>feat: update routes</td>
      <td>Actualización del enrutamiento para las vistas de reportes</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/de75928">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/reports_cumplimiento</td>
      <td>3b0f309</td>
      <td>feat: reports updates</td>
      <td>Actualización de componentes y lógica del módulo de reportes</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/3b0f309">Ver commit</a></td>
    </tr>
    <tr>
      <td>Frontend</td>
      <td>feature/user-authentication</td>
      <td>8116699</td>
      <td>authentication bc</td>
      <td>Agregado bounded context de autenticación de usuarios</td>
      <td><a href="https://github.com/upc-web-applications/Frontend/commit/8116699">Ver commit</a></td>
    </tr>
  </tbody>
</table>

#### 5.2.2.5.Execution Evidence for Sprint Review.

Durante el Sprint se lograron avances significativos en la visualización y navegación de la aplicación, incluyendo interfaces de identificación, Dashboard del operador, del supervisor y del gerente

#### Account Generation and Authentication BC

<h5 align="center">Inicio de autenticación</h5>

<p align="center">
  <img src="images/ch5-img-10.jpg" width="500"/>
</p>

*Pantalla de autenticación del sistema donde el usuario ingresa sus credenciales para acceder a la plataforma.*

#### Site / Area and Industrial Asset BC

<h5 align="center">1. Visualización Gestión de sedes</h5>

<img src="images/Operario-sedes.png" width="500">

*Vista orientada al registro de las sedes activos o inactivos.*

<h5 align="center">1. Visualización de las Areas </h5>

<img src="images/operario-areas.png" width="500">

*Vista orientada al registro del estado de las areas y su nivel de riesgo.*


#### Inspection / Unsafe Condition BC

<h5 align="center">1. Visualización de las Inspecciones</h5>

<img src="images/Operario-inspecciones.png" width="500">

*Este conexto maneja el registro de incidentes.*


<h5 align="center">1. Visualización de los activos</h5>

<img src="images/operario-activos.png" width="500">

*Vista orientada al registro de los activos industriales como máquinas y equipos vinculados a cada área.*


#### Risk Assessment BC
<h5 align="center">Lista de Peligros</h5>
<p align="center">Registro y gestión de peligros identificados en planta.</p>
<p align="center">
  <img src="images/bc/hazard-list.png" width="500"/>
</p>
<h5 align="center">Detalle de Peligro</h5>
<p align="center">Información detallada de un peligro específico.</p>
<p align="center">
  <img src="images/bc/hazard-detail.png" width="500"/>
</p>
<h5 align="center">Formulario de Peligro</h5>
<p align="center">Creación y edición de peligros.</p>
<p align="center">
  <img src="images/bc/hazard-form.png" width="500"/>
</p>
<h5 align="center">Evaluaciones de Riesgo</h5>
<p align="center">Lista de evaluaciones con probabilidad, severidad y nivel de riesgo.</p>
<p align="center">
  <img src="images/bc/risk-assessment-list.png" width="500"/>
</p>
<h5 align="center">Detalle de Evaluación</h5>
<p align="center">Vista completa de una evaluación de riesgo.</p>
<p align="center">
  <img src="images/bc/risk-assessment-detail.png" width="500"/>
</p>
<h5 align="center">Formulario de Evaluación</h5>
<p align="center">Registro de nueva evaluación de riesgo.</p>
<p align="center">
  <img src="images/bc/risk-assessment-form.png" width="500"/>
</p>
<h5 align="center">Mapa de Calor</h5>
<p align="center">Visualización de niveles de criticidad por área de la planta.</p>
<p align="center">
  <img src="images/bc/heat-map.png" width="500"/>
</p>
<h5 align="center">Patrones de Riesgo</h5>
<p align="center">Detección de patrones recurrentes de incidentes por sector.</p>
<p align="center">
  <img src="images/bc/patterns.png" width="500"/>
</p>
<h5 align="center">Alertas de Patrón</h5>
<p align="center">Alertas generadas por patrones de riesgo detectados.</p>
<p align="center">
  <img src="images/bc/pattern-alerts.png" width="500"/>
</p>
<h5 align="center">Resumen Diario</h5>
<p align="center">Reporte diario de nuevos riesgos, en progreso y resueltos por sector.</p>
<p align="center">
  <img src="images/bc/daily-summary.png" width="500"/>
</p>

#### Mitigation BC
<h5 align="center">Lista de Mitigaciones</h5>
<p align="center">Seguimiento de medidas de control implementadas.</p>
<p align="center">
  <img src="images/bc/mitigation-list.png" width="500"/>
</p>
<h5 align="center">Detalle de Mitigación</h5>
<p align="center">Información completa de una medida de mitigación.</p>
<p align="center">
  <img src="images/bc/mitigation-detail.png" width="500"/>
</p>

<h5 align="center">Tickets de Acción Correctiva</h5>
<p align="center">Gestión de tickets correctivos con SLA y técnicos asignados.</p>
<p align="center">
  <img src="images/bc/tickets-list.png" width="500"/>
</p>
<h5 align="center">Detalle de Ticket</h5>
<p align="center">Vista completa de un ticket de acción correctiva.</p>
<p align="center">
  <img src="images/bc/ticket-detail.png" width="500"/>
</p>
<h5 align="center">Formulario de Ticket</h5>
<p align="center">Creación y asignación de tickets correctivos.</p>
<p align="center">
  <img src="images/bc/ticket-form.png" width="500"/>
</p>
<h5 align="center">Verificaciones de Medida</h5>
<p align="center">Supervisión y verificación de medidas implementadas.</p>
<p align="center">
  <img src="images/bc/verification-list.png" width="500"/>
</p>
<h5 align="center">Formulario de Verificación</h5>
<p align="center">Registro de veredicto de verificación.</p>
<p align="center">
  <img src="images/bc/verification-form.png" width="500"/>
</p>
<h5 align="center">Historial de Tickets</h5>
<p align="center">Línea de tiempo con eventos de cada ticket.</p>
<p align="center">
  <img src="images/bc/ticket-history.png" width="500"/>
</p>

#### Monitoring / Dashboard BC 
<h5 align="center">1. Visualización de Mapa de Calor para Supervisores</h5>

<p align="center">
  <img src="images/mapa de calor.png" width="500"/>
</p>

*Vista principal del supervisor con acceso al mapa de calor por sectores*

<h5 align="center">1. Visualización de la bandeja de tickets</h5>

<p align="center">
  <img src="images/bandeja-tickets.png" width="500"/>
</p>

*Vista principal del supervisor en la bandeja de tickets*

<h5 align="center">1. Visualización de gestión de activos</h5>

<p align="center">
  <img src="images/gestion-activos.png" width="500"/>
</p>

*Vista principal del supervisor en la gestión de activos*

<h5 align="center">1. Visualización del mapa de sectores</h5>

<p align="center">
  <img src="images/mapa-sectores.png" width="500"/>
</p>

*Vista principal del supervisor en los reportes y cumplimiento*

<h5 align="center">1. Visualización del directorio tecnico</h5>

<p align="center">
  <img src="images/reportes.png" width="500"/>
</p>

*Vista principal del supervisor en los reportes y cumplimiento*


#### Reports / Compliance BC
<h5 align="center">1. Visualización de Inicio del Gerente</h5>

<p align="center">
  <img src="images/ch5-img-11.jpg" width="500"/>
</p>

*Vista principal del gerente con acceso al resumen general del sistema y métricas de seguridad.*

<h5 align="center">2. Visualización de Nuevo Reporte del Gerente</h5>

<p align="center">
  <img src="images/ch5-img-12.jpg" width="500"/>
</p>

*Vista orientada al registro de nuevos reportes de incidentes y condiciones inseguras.*

<h5 align="center">3. Visualización de Mis Reportes del Gerente</h5>

<p align="center">
  <img src="images/ch5-img-13.jpg" width="500"/>
</p>

*Vista para la consulta y administración de reportes generados dentro del sistema.*

<h5 align="center">4. Visualización del Historial de Incidentes del Gerente</h5>

<p align="center">
  <img src="images/ch5-img-14.jpg" width="500"/>
</p>
*Vista enfocada en el seguimiento y análisis del historial de incidentes registrados.*

<h5 align="center">5. Visualización de Alertas Críticas del Gerente</h5>

<p align="center">
  <img src="images/ch5-img-15.jpg" width="500"/>
</p>

*Vista de alertas críticas para supervisar eventos de riesgo y estados de atención.*

<h5 align="center">6. Visualización de Indicadores Predictivos del Gerente</h5>

<p align="center">
  <img src="images/ch5-img-16.jpg" width="500"/>
</p>
*Vista de indicadores predictivos con métricas y tendencias relacionadas a seguridad industrial.*

<h5 align="center">7. Visualización del Plan SST del Gerente</h5>

<p align="center">
  <img src="images/ch5-img-17.jpg" width="500"/>
</p>

* Video de la Ejecución del Web app Dashboard Gerente

https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQBALHFNZT8gT4yDbhrSrY9UAZIWLt8aMd3C8mnHjEJcOPc?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=3vniTW

* Video de la Ejecución del Web app Dashboard Operario
  
https://1drv.ms/v/c/7E97073B2DC02368/IQC8p3wmcttLTKSZG68RWUqIAZ49lfz4UNWr2nqnkEUgzXg?e=kB406n

* Video de la Ejecución del Web app Mitigación de accidentes y cuidado de riesgos
  
https://upcedupe-my.sharepoint.com/:v:/g/personal/u202418655_upc_edu_pe/IQC_6i5BsOJGTLdzmhEy1SD0ARj-GwAq0GY5e8ZuEKii3Xw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=PbxdK8

* Video de la Ejecución del Web app Monitoreo/Dashboard
  
https://upcedupe-my.sharepoint.com/:v:/g/personal/u20231b781_upc_edu_pe/IQACbrvx365gSrZiZgk9H0ZPAYetdnOFpNdsz9cGPKd72Hw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=K9zxK1

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
  <img src="images/ch5-img-18.png" width="500"/>
</p>

*Respuesta del endpoint con los cuatro indicadores KPI. Los estados `alert` y `danger` se visualizan en el dashboard mediante tags de color.*

<h5 align="center">GET /api/v1/historical_trends</h5>

<p align="center">
  <img src="images/ch5-img-19.png" width="500"/>
</p>

*Retorno de la evolución mensual de incidentes. Los datos se filtran por sector en el frontend para construir los datasets de la gráfica de línea.*

<h5 align="center">GET /api/v1/critical_alerts</h5>

<p align="center">
  <img src="images/ch5-img-20.png" width="500"/>
</p>

*Listado de alertas críticas con estado `unresolved`. El frontend calcula el KPI de sectores críticos a partir de estos registros.*

<h5 align="center">PATCH /api/v1/critical_alerts/ALERT_001</h5>

<p align="center">
  <img src="images/ch5-img-21.jpg" width="500"/>
</p>

*Actualización del estado de la alerta a `resolved`. El store recalcula automáticamente los KPIs tras recibir la respuesta.*

<h5 align="center">DELETE /api/v1/critical_alerts/ALERT_001</h5>

<p align="center">
  <img src="images/ch5-img-22.jpg" width="500"/>
</p>

*Eliminación de la alerta. Respuesta HTTP 200 con body vacío `{}`.*

<h5 align="center">GET /api/v1/annual_ohs_plan</h5>

<p align="center">
  <img src="images/ch5-img-23.jpg" width="500"/>
</p>

*Plan anual con cumplimiento global del 72%, por debajo de la meta del 80%. El frontend muestra el indicador en amarillo con etiqueta "Aceptable".*

<h5 align="center">GET /api/v1/predictive_indicators</h5>

<p align="center">
  <img src="images/ch5-img-24.jpg" width="500"/>
</p>

*Indicadores predictivos con sectores de tendencia creciente. `WAREHOUSE_B` aparece con tag rojo (`critical`) y `GAS_PLANT` con tag amarillo (`warning`).*

<h5 align="center">GET /api/v1/historical_incident_records</h5>

<p align="center">
  <img src="images/ch5-img-25.jpg" width="500"/>
</p>

*Historial de incidentes de solo lectura. El frontend aplica filtros por sector, tipo y rango de fechas sobre los datos ya cargados.*

<h5 align="center">GET /api/v1/generated_reports</h5>

<p align="center">
  <img src="images/ch5-img-26.jpg" width="500"/>
</p>

*Listado de reportes generados con tipo `monthly` y formato PDF.*

<h5 align="center">POST /api/v1/generated_reports</h5>

<p align="center">
  <img src="images/ch5-img-27.jpg" width="500"/>
</p>

*Registro de un nuevo reporte. El servidor retorna HTTP 201 con el id generado automáticamente. El store agrega el registro al historial sin recargar la página.*

<h5 align="center">DELETE /api/v1/generated_reports/Z4PRqZP</h5>

<p align="center">
  <img src="images/ch5-img-28.jpg" width="500"/>
</p>

*Eliminación del reporte con id `Z4PRqZP`. Respuesta HTTP 200 con body vacío `{}`.*

*Operario* 

Para este Sprint no se cuenta con un repositorio independiente de Web Services ni con servicios backend desplegados. La aplicación consume una API local simulada basada en json-server, definida dentro del mismo repositorio frontend mediante los archivos `server/db.json` y `server/routes.json`. Por este motivo, el repositorio de Servicios Web corresponde al repositorio frontend del proyecto RiskGuard, donde se encuentran definidos y versionados los endpoints mock.

Se documentan los endpoints simulados utilizados para validar las funcionalidades desarrolladas durante el sprint.

**Repositorio API/local:** https://github.com/upc-web-applications/Frontend.git

**URL base local:** `http://localhost:3000/api/v1`  
**Archivo de datos simulado:** `server/db.json`  
**Archivo de rutas simulado:** `server/routes.json`

**Commits relacionados con Documentación e implementación de endpoints:**

| Commit Id | Mensaje |
|---|---|
| - | feat: add inspection and headquarters BC |

**Tabla de Endpoints**

| Endpoint | Acciones implementadas | Verbo HTTP | Parámetros | Explicación |
|---|---|---|---|---|
| `/sedes` | Obtener todas las sedes | `GET` | No requiere | Retorna el listado completo de sedes registradas |
| `/sedes` | Crear nueva sede | `POST` | Body: `{ nombre, direccion, telefono, email, estado, fechaCreacion }` | Registra una nueva sede en el sistema |
| `/sedes/{id}` | Obtener sede por ID | `GET` | `id` en la URL | Retorna los datos de una sede específica |
| `/sedes/{id}` | Actualizar sede | `PUT` | `id` en la URL. Body con los datos actualizados | Actualiza todos los campos de una sede existente |
| `/sedes/{id}` | Eliminar sede | `DELETE` | `id` en la URL | Elimina la sede del sistema |
| `/areas` | Obtener todas las áreas | `GET` | No requiere | Retorna el listado completo de áreas registradas |
| `/areas?sedeId={id}` | Obtener áreas por sede | `GET` | `sedeId` como query param | Filtra las áreas pertenecientes a una sede específica |
| `/areas` | Crear nueva área | `POST` | Body: `{ nombre, código, descripción, sedeId, estado, nivelRiesgo, fechaCreacion }` | Registra una nueva área vinculada a una sede |
| `/areas/{id}` | Actualizar área | `PUT` | `id` en la URL. Body con los datos actualizados | Actualiza los datos de un área existente |
| `/areas/{id}` | Eliminar área | `DELETE` | `id` en la URL | Elimina el área del sistema |
| `/activos` | Obtener todos los activos | `GET` | No requiere | Retorna el listado completo de activos industriales |
| `/activos?areaId={id}` | Obtener activos por área | `GET` | `areaId` como query param | Filtra los activos pertenecientes a un área específica |
| `/activos` | Crear nuevo activo | `POST` | Body: `{ código, nombre, descripción, tipo, areaId, sedeId, estado, fechaAdquisicion, ultimoMantenimiento }` | Registra un nuevo activo vinculado a un área y sede |
| `/activos/{id}` | Actualizar activo | `PUT` | `id` en la URL. Body con los datos actualizados | Actualiza los datos de un activo existente |
| `/activos/{id}` | Eliminar activo | `DELETE` | `id` en la URL | Elimina el activo del sistema |
| `/inspecciones` | Obtener todas las inspecciones | `GET` | No requiere | Retorna el listado completo de inspecciones registradas |
| `/inspecciones` | Crear nueva inspección | `POST` | Body: `{ ticket, tipoIncidente, areaId, sedeId, activoId, nivelUrgencia, descripción, estado, fotoUrl, operarioId, fechaReporte, fechaActualizacion, accionCorrectiva }` | Registra una nueva inspección con ticket generado automáticamente |
| `/inspecciones/{id}` | Obtener inspección por ID | `GET` | `id` en la URL | Retorna el detalle completo de una inspección |
| `/inspecciones/{id}` | Eliminar inspección | `DELETE` | `id` en la URL | Elimina la inspección del sistema |




#### 5.2.2.7.Software Deployment Evidence for Sprint Review.

Durante el Sprint 2 se realizó el despliegue completo de la aplicación RiskGuard, tanto del frontend como del backend simulado. El frontend, desarrollado en Vue 3 con Vite, fue desplegado  en  Vercel y Firebase

#### Despliegue de Firebase + render  para Reportes y Cumplimiento
Firebase Hosting. El backend simulado con json-server fue desplegado en **Render**, exponiendo los endpoints REST consumidos por la aplicación.
Backend – Render
Se creó un repositorio independiente con el archivo `db.json` y el `package.json` configurado con el comando de inicio:

<p align="center">
  <img src="images/ch5-img-29.jpg" width="500"/>
</p>

El servicio fue desplegado como un Web Service en Render, obteniendo la URL base:
`https://db-server-risk-2.onrender.com`
Los endpoints disponibles incluyen: `/kpi_dashboard`, `/critical_alerts`, `/predictive_indicators`, `/generated_reports`, `/monthly_reports`, `/historical_incident_records`, `/historical_trends` y `/annual_ohs_plan`.

<p align="center">
  <img src="images/ch5-img-30.jpg" width="500"/>
</p>

Luego creamos nuestro proyecto en firebase 
<p align="center">
  <img src="images/ch5-img-31.jpg" width="500"/>
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
  <img src="images/ch5-img-32.jpg" width="500"/>
</p>

El directorio de publicación fue configurado como `dist` en `firebase.json`, y la aplicación fue configurada como Single Page App (SPA). La URL de producción obtenida fue:
Boundend context : Reportes y cumplimiento

https://riskguard-7fe11.web.app

#### Despliegue de Vercel + My Json Server para Usuario/Autenticacion
Para el bounded context de User Authentication se realizó el despliegue del frontend utilizando Vercel, debido a su integración directa con GitHub y su capacidad para desplegar ramas específicas del repositorio. Asimismo, el backend simulado fue desplegado mediante My JSON Server, utilizando un archivo `db.json` publicado en un repositorio independiente.

<p align="center">
  <img src="images/api-authentication.png" width="500"/>
</p>

Posteriormente, se configuró el archivo de entorno de producción del frontend para consumir la URL pública de My JSON Server. En el archivo `src/.env.production` se actualizó la variable `VITE_RISKGUARD_API_URL`, reemplazando la URL local por la URL pública del backend simulado.

<p align="center">
  <img src="images/my-json-server-api.png" width="500"/>
</p>

Para el despliegue del frontend se creó un proyecto en Vercel llamado `riskguard-user-authentication`. Este proyecto fue conectado al repositorio `upc-web-applications/Frontend`, configurando como rama de producción `feature/user-authentication`.

<p align="center">
  <img src="images/vercel-deploy.png" width="500"/>
</p>

FrontEnd: https://riskguard-user-authentication.vercel.app/login

Backend (My Json Server): https://my-json-server.typicode.com/upc-web-applications/riskguard-user-authentication-api

#### Despliegue de Vercel + Render para Monitoreo/Dashboard

Para el bounded context de **Monitoring Dashboard** se realizó el despliegue del frontend utilizando **Vercel**, debido a su integración directa con GitHub y su soporte para aplicaciones desarrolladas con **Vite + Vue.js**.

<p align="center">
  <img src="images/deploy-monitoreo.png" width="500"/>
</p>

Para el backend simulado se creó un repositorio independiente llamado:`riskguard-monitoring-dashboard-api`. Este repositorio contiene los archivos necesarios para levantar la fake API:

<p align="center">
  <img src="images/db-json-monitoreo.png" width="500"/>
</p>

Asimismo, el backend simulado fue desplegado mediante **Render** utilizando `json-server`. Inicialmente se evaluó el uso de **My JSON Server**, sin embargo, durante la validación del endpoint `/assets` se presentó una limitación al exponer los datos del archivo `db.json`. Por ello, se optó por desplegar una fake API en Render, permitiendo conservar la estructura completa de datos requerida por el dashboard.

<p align="center">
  <img src="images/json-srver-monitoreo.png" width="500"/>
</p>

FrontEnd: https://riskguard-monitoring-dashboard.vercel.app

Backend (Render): https://riskguard-monitoring-dashboard-api.onrender.com (Primero cargar la Fake API)

#### Despliegue de Firebase + Render para Risk Guard

El frontend fue desplegado en **Firebase Hosting** y el backend simulado con **json-server** fue desplegado en **Render**, exponiendo los endpoints REST consumidos por la aplicación.

##### Backend – Render

Se creó la carpeta `copy/` con los archivos `db.json` y `package.json` configurado con el comando de inicio:

```json
{
  "scripts": {
    "start": "json-server --host 0.0.0.0 --watch db.json"
  },
  "dependencies": {
    "json-server": "0.17.4"
  }
}
```

El servicio fue desplegado como un Web Service en Render, obteniendo la URL base:

```
https://db-server-risk-0r34.onrender.com
```

<p align="center">
  <img src="images/bc/reder-bc-mi.png" width="500"/>
</p>

Los endpoints disponibles incluyen: `/peligros`, `/evaluaciones-riesgo`, `/mitigaciones`, `/patrones-riesgo`, `/niveles-criticidad-area`, `/alertas-patron`, `/resumenes-diarios`, `/tickets-accion-correctiva`, `/verificaciones-medida`, `/historiales-ticket`, `/alertas-sla`, `/notificaciones-criticas` y `/tecnicos`.

##### Frontend – Firebase Hosting

Se creó el proyecto en Firebase Console:

```
risk-guard-u202418655
```

Luego se ejecutaron los siguientes comandos para el despliegue:

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
npm run build
firebase deploy
```

<p align="center">
  <img src="images/bc/pa-bc-mi.png" width="500"/>
</p>

El directorio de publicación fue configurado como `dist` en `firebase.json`, y la aplicación fue configurada como Single Page App (SPA) con rewrites para que todas las rutas apunten a `index.html`.

##### Configuración de variables de entorno

En los archivos `.env.production` y `.env.development` se configuró la URL base de la API:

```
VITE_RISKGUARD_API_URL="https://db-server-risk-0r34.onrender.com/api/v1/"
```

Además, en `src/shared/infrastructure/base-api.js` se actualizó para consumir la variable de entorno en lugar del URL hardcodeado:

```js
baseURL: import.meta.env.VITE_RISKGUARD_API_URL,
```

<p align="center">
  <img src="images/bc/des-bc-mi.png" width="500"/>
</p>

##### URLs de producción

- **Frontend (Firebase Hosting):** https://risk-guard-u202418655.web.app
- **Backend (Render):** https://db-server-risk-0r34.onrender.com

*Operario*

Durante el Sprint 2 se realizó el despliegue completo del Bounded Context de Sede/Área e Inspección. El frontend fue desplegado en **Vercel** y el backend simulado con **json-server** fue desplegado mediante **My JSON Server**, utilizando un repositorio independiente con el archivo `db.json`.

##### Backend – My JSON Server

Se creó un repositorio independiente en la organización `upc-web-applications` con el nombre `riskguard-inspection-headquarters-api`, que contiene el archivo `db.json` con los datos simulados de sedes, áreas, activos e inspecciones.

El repositorio fue publicado en:
```
https://github.com/upc-web-applications/riskguard-inspection-headquarters-api
```

La URL base del backend simulado obtenida fue:

```
https://my-json-server.typicode.com/upc-web-applications/riskguard-inspection-headquarters-api
```

Los endpoints disponibles incluyen: `/sedes`, `/areas`, `/activos` e `/inspecciones`.

##### Frontend – Vercel

Se configuró el archivo de entorno de producción del frontend para consumir la URL pública de My JSON Server. En el archivo `src/.env.production` se actualizó la variable `VITE_RISKGUARD_API_URL` reemplazando la URL local por la URL pública del backend simulado:

VITE_RISKGUARD_API_URL="https://my-json-server.typicode.com/upc-web-applications/riskguard-inspection-headquarters-api"

Para el despliegue del frontend se conectó el repositorio `upc-web-applications/Frontend` a Vercel, configurando como rama de producción `feature/inspection_headquarters`.

##### URL de producción

- **Frontend (Vercel):** https://frontend-git-feature-inspecti-0997ce-carlosblancas969s-projects.vercel.app
- **Backend (My JSON Server):** https://my-json-server.typicode.com/upc-web-applications/riskguard-inspection-headquarters-api
- 
#### 5.2.2.8.Team Collaboration Insights during Sprint

Durante el Sprint 2, el equipo colaboró activamente en el desarrollo de la Web Application RiskGuard. Cada integrante trabajó en su respectivo bounded context mediante ramas feature independientes, integrando los cambios al repositorio compartido a través de pull requests. A continuación se presentan los analíticos de colaboración y el historial de commits obtenidos desde el repositorio `upc-web-applications/Frontend`.

El repositorio cuenta con 7 ramas activas: `main`, `develop`, `feature/reports_cumplimiento`, `feature/monitoring-dashboard`, `feature/inspection_headquarters`, `feature/assessment_mitigation` y `feature/user-authentication`, reflejando la separación por bounded context adoptada por el equipo.


**Capturas de analíticos y commits en GitHub:**

*Estructura de ramas del repositorio utilizada durante el Sprint 2.*

<h5 align="center">Ramas creadas</h5>

<p align="center">
  <img src="images/ch5-img-33.jpg" width="600"/>
</p>

*Historial de commits organizado por cada integrante del equipo.*

<h5 align="center">Commits de cada autor</h5>

<p align="center">
  <img src="images/ch5-img-34.jpg" width="600"/>
</p>

*Resumen estadístico del repositorio con cantidad de commits y contribuciones por autor.*

<h5 align="center">Estadísticas</h5>

<p align="center">
  <img src="images/ch5-img-35.jpg" width="600"/>
</p>


### 5.2.3. Sprint 3

#### 5.2.3.1. Sprint Planning 3

En este Sprint 3, el equipo se enfocó en el desarrollo del Backend para la aplicación web RiskGuard, con el objetivo de construir la base funcional que permita procesar la información registrada por los usuarios, aplicar reglas de negocio y exponer servicios consumibles desde el frontend. A diferencia de los sprints anteriores, centrados principalmente en la presentación visual y la interacción del usuario, este sprint priorizó la implementación de la lógica interna del sistema, la organización del código bajo una arquitectura orientada a DDD y la definición de endpoints REST para los principales flujos de la plataforma.

| **Campo** | **Detalle** |
|----------|------------|
| Sprint # | 3 |
| Date | 2026-06-15 |
| Time | 4:00 PM |
| Location | Reunión virtual (Google Meet) |
| Prepared By | Flores Eusebio, Angel Thyago |
| Attendees (to planning meeting) | Aponte Pablo, Isabel Luisa / Laura Acosta, Victor Jhosef / Blancas Chávez, Carlos Franco / Flores Eusebio, Angel Thyago |
| Sprint n – 2 Review Summary | Durante el Sprint 2, el equipo completó el desarrollo del frontend de RiskGuard con 154 tareas implementadas, cubriendo los 7 bounded contexts planificados. Se logró la integración con Fake API (json-server) para simular operaciones CRUD, autenticación por roles (operario, supervisor, gerente), dashboards con indicadores KPI, mapas de calor, gestión de tickets con SLA, mantenimiento preventivo de activos y generación de reportes en PDF/Excel. El Product Owner validó la navegación completa de la aplicación y la experiencia responsive en desktop y móvil. La aplicación fue desplegada en Vercel con la API mock en Render. |
| Sprint n – 2 Retrospective Summary | El equipo destacó como acierto la adopción de GitFlow con ramas feature por bounded context, lo que facilitó el trabajo paralelo y redujo conflictos de merge. Se valoró positivamente la implementación de i18n (español/inglés) y el diseño dark theme consistente en todos los módulos. Como oportunidades de mejora, se identificó la necesidad de definir contratos de API más formales antes del desarrollo para facilitar la transición al backend real, y se acordó implementar revisiones de código cruzadas (code reviews) mediante pull requests para el Sprint 3. |
| Sprint Goal | Our focus is on developing the backend Web Services for RiskGuard using C# (.NET) with Domain-Driven Design architecture, implementing RESTful API endpoints for the bounded contexts of Account Generation and Authentication, Site / Area and Industrial Asset, Inspection / Unsafe Condition, Risk Assessment (IPERC) and Mitigation, and Reports / Compliance. We believe it delivers a robust, secure and scalable server-side foundation that replaces the current json-server mock with real business logic, data persistence and JWT-based authentication. This will be confirmed when the frontend application can consume all implemented endpoints, perform CRUD operations with validated data, and authenticate users with role-based access control across the three user profiles (operator, supervisor and manager). |
| Sprint n Velocity | 80 SP |
| Sum of Story Points | 80 SP |

#### 5.2.3.2. Aspect Leaders and Collaborators

En este Sprint, los aspectos corresponden a los Bounded Contexts del backend de RiskGuard, implementados como Web Services con C# / ASP.NET Core y arquitectura DDD. Se asignaron roles de liderazgo y colaboración para cada módulo con el fin de mejorar la organización, distribución de tareas y coordinación entre los integrantes del equipo durante el desarrollo de los servicios REST.

| Miembro del equipo (Apellido, Nombre) | Usuario GitHub | Account Generation and Authentication BC (L/C) | Site / Area and Industrial Asset BC (L/C) | Inspection / Unsafe Condition BC (L/C) | Risk Assessment (IPERC) BC (L/C) | Mitigation BC (L/C) | Monitoring / Dashboard BC (L/C) | Reports / Compliance BC (L/C) |
|--------------------------------------|---------------|-----------------------------------------------|-------------------------------------------|----------------------------------------|----------------------------------|---------------------|----------------------------------|-------------------------------|
| Aponte Pablo, Isabel Luisa | IsabelAponte234 | C | C | C | C | C | C | L |
| Laura Acosta, Victor Jhosef | Zatrynox | C | C | C | L | L | C | C |
| Blancas Chávez, Carlos Franco | CarlosBlancas969 | C | L | L | C | C | C | C |
| Flores Eusebio, Angel Thyago | angelfdevs | L | C | C | C | C | L | C |

#### 5.2.3.3. Sprint Backlog 3

En esta sección se presenta el Sprint Backlog correspondiente al Sprint 3 del proyecto, el cual tuvo como objetivo principal implementar los Web Services (Backend) de RiskGuard utilizando C# / ASP.NET Core con arquitectura Domain-Driven Design (DDD). Durante este Sprint, el equipo desarrolló las Technical Stories correspondientes a los endpoints REST de los bounded contexts: IAM, OrganizationAssets, Inspections, RiskAssessments, Mitigations, Hazards, Technicians, MonitoringDashboard y ReportsCompliance.

**Tablero Trello:** https://trello.com/invite/b/6a33807f046587a11bd72763/ATTId192c77528e7fa368154cbd580aa20c0312D01B0/riskguard

![Trello Sprint 3](images/trello-sprint-3.png)

| User Story ID | Título | Task ID | Descripción | Estimación (hrs) | Asignado a | Status |
|---|---|---|---|---|---|---|
| TS01 | Servicio de Notificaciones Push | T01 | Implementar endpoint POST /api/v1/notificaciones/push con entidad Notification y autorización JWT | 5 | Laura Acosta, Victor Jhosef | Done |
| TS02 | Endpoint para Obtener Patrones de Riesgo Recurrentes | T02 | Implementar RiskPatternsController con endpoints CRUD en /api/v1/risk-patterns con filtro por sector | 5 | Laura Acosta, Victor Jhosef | Done |
| TS03 | Endpoint para Obtener Datos del Mapa de Calor | T03 | Implementar AreaCriticalityLevelsController con endpoints CRUD en /api/v1/area-criticality-levels con filtro por sector | 5 | Laura Acosta, Victor Jhosef | Done |
| TS04 | Endpoint para Obtener Riesgos Críticos Sin Atender | T04 | Implementar RiskAssessmentsController con endpoints CRUD en /api/v1/risk-assessments con filtro por sector | 5 | Laura Acosta, Victor Jhosef | Done |
| TS05 | Endpoint para Marcar Alerta de Patrón como Revisada | T05 | Implementar PatternAlertsController con endpoints CRUD en /api/v1/pattern-alerts con filtro por sector | 5 | Laura Acosta, Victor Jhosef | Done |
| TS06 | Endpoint para Obtener Resumen Diario de Riesgos por Sector | T06 | Implementar DailySummariesController con endpoints CRUD en /api/v1/daily-summaries con filtro por sector y fecha | 5 | Laura Acosta, Victor Jhosef | Done |
| TS07 | Endpoint de Cálculo de Matriz IPERC | T07 | Implementar lógica de cálculo IPERC integrada en RiskAssessmentsController con campos probability y severity | 4 | Laura Acosta, Victor Jhosef | Done |
| TS07 | Endpoint de Cálculo de Matriz IPERC | T08 | Implementar CorrectiveActionTicketsController, MitigationsController y SlaAlertsController en /api/v1/ del BC Mitigations | 5 | Laura Acosta, Victor Jhosef | Done |
| TS07 | Endpoint de Cálculo de Matriz IPERC | T09 | Implementar MeasureVerificationsController, CriticalNotificationsController y TicketHistoriesController del BC Mitigations | 5 | Laura Acosta, Victor Jhosef | Done |
| TS07 | Endpoint de Cálculo de Matriz IPERC | T10 | Implementar HazardsController en /api/v1/hazards y TechniciansController en /api/v1/technicians del proyecto assessment | 4 | Laura Acosta, Victor Jhosef | Done |
| TS08 | Endpoint para Obtener Indicadores del Dashboard Ejecutivo | T11 | Implementar KpiDashboardController con endpoints GET all y GET by id en /api/v1/kpi_dashboard | 4 | Aponte Pablo, Isabel Luisa | Done |
| TS09 | Endpoint para Obtener Tendencias Históricas | T12 | Implementar HistoricalTrendsController con endpoints GET all y GET by id en /api/v1/historical_trends | 4 | Aponte Pablo, Isabel Luisa | Done |
| TS10 | Endpoint para Gestión de Reportes Generados | T13 | Implementar GeneratedReportsController con endpoints GET all, GET by id, POST y DELETE en /api/v1/generated_reports | 5 | Aponte Pablo, Isabel Luisa | Done |
| TS11 | Endpoint para Gestión de Alertas Críticas | T14 | Implementar CriticalAlertsController con endpoints GET all, GET by id, PUT y DELETE en /api/v1/critical_alerts | 5 | Aponte Pablo, Isabel Luisa | Done |
| TS12 | Endpoint para Obtener el Plan Anual de SST | T15 | Implementar AnnualOhsPlanController con endpoints GET all, GET by id y PUT en /api/v1/annual_ohs_plan | 4 | Aponte Pablo, Isabel Luisa | Done |
| TS12 | Endpoint para Obtener el Plan Anual de SST | T16 | Implementar MonthlyReportsController con endpoints GET all, GET by id, GET by year, POST y PUT en /api/v1/monthly_reports | 5 | Aponte Pablo, Isabel Luisa | Done |
| TS12 | Endpoint para Obtener el Plan Anual de SST | T17 | Implementar CumulativeStIndicatorsController en /api/v1/cumulative_st_indicators y HistoricalIncidentRecordsController en /api/v1/historical_incident_records | 5 | Aponte Pablo, Isabel Luisa | Done |
| TS12 | Endpoint para Obtener el Plan Anual de SST | T18 | Implementar PredictiveIndicatorsController con endpoints GET all y GET by id en /api/v1/predictive_indicators | 4 | Aponte Pablo, Isabel Luisa | Done |
| TS13 | Endpoint para Registro y Consulta de Inspecciones por Operario | T19 | Implementar InspeccionesController con POST personalizado y GET /mine/{operarioId} con filtro por estado en /api/v1/inspecciones | 5 | Blancas Chávez, Carlos Franco | Done |
| TS14 | Endpoint para Gestión de Catálogo de Peligros | T20 | Implementar PeligrosController con endpoints  heredados de CrudController en /api/v1/dangers | 4 | Blancas Chávez, Carlos Franco | Done |
| TS15 | Endpoint para Gestión de Sedes Operativas | T21 | Implementar SedesController con endpoints  heredados de CrudController en /api/v1/sedes | 4 | Blancas Chávez, Carlos Franco | Done |
| TS16 | Endpoint para Gestión de Áreas y Activos Industriales | T22 | Implementar AreasController con endpoints  y GET /active en /api/v1/areas filtrando por Estado="Activo" | 5 | Blancas Chávez, Carlos Franco | Done |
| TS16 | Endpoint para Gestión de Áreas y Activos Industriales | T23 | Implementar ActivosController con endpoints  y GET /by-area/{areaId} en /api/v1/activos filtrando por AreaId y Estado="Activo" | 5 | Blancas Chávez, Carlos Franco | Done |
| TS16 | Endpoint para Gestión de Áreas y Activos Industriales | T24 | Configurar DbContext con EF Core, MySQL, CrudController genérico y Swagger/OpenAPI del proyecto inspection | 4 | Blancas Chávez, Carlos Franco | Done |
| TS17 | Endpoint para Autenticación y Generación de Token JWT | T25 | Implementar AuthenticationController con POST /sign-in (JWT) y POST /sign-up en /api/v1/authentication | 5 | Flores Eusebio, Angel Thyago | Done |
| TS18 | Endpoint para Gestión de Usuarios, Roles y Sesiones | T26 | Implementar UsersController  y PUT personalizado en /api/v1/users y RolesController en /api/v1/roles | 5 | Flores Eusebio, Angel Thyago | Done |
| TS18 | Endpoint para Gestión de Usuarios, Roles y Sesiones | T27 | Implementar SessionsController en /api/v1/sessions y AccessLogsController en /api/v1/access-logs | 4 | Flores Eusebio, Angel Thyago | Done |
| TS19 | Endpoint para Gestión de Tickets, Técnicos y Mantenimiento Preventivo | T28 | Implementar TicketsController en /api/v1/tickets y TechniciansController en /api/v1/dashboard-technicians con CrudController | 4 | Flores Eusebio, Angel Thyago | Done |
| TS19 | Endpoint para Gestión de Tickets, Técnicos y Mantenimiento Preventivo | T29 | Implementar AssetsController en /api/v1/assets y PreventiveMaintenancesController en /api/v1/preventiveMaintenances | 4 | Flores Eusebio, Angel Thyago | Done |
| TS20 | Endpoint para Gestión de Zonas del Mapa de Calor y Reportes Archivados | T30 | Implementar HeatMapZonesController en /api/v1/heatMapZones y ArchivedReportsController en /api/v1/archived-reports | 4 | Flores Eusebio, Angel Thyago | Done |
| TS20 | Endpoint para Gestión de Zonas del Mapa de Calor y Reportes Archivados | T31 | Configurar DbContext con EF Core, MySQL, CrudController genérico, JWT middleware y Swagger/OpenAPI del proyecto auth_monitoring | 5 | Flores Eusebio, Angel Thyago | Done |


#### 5.2.3.4. Development Evidence for Sprint Review

En esta sección se presentan los commits realizados durante el Sprint 3, los cuales reflejan el avance en la implementación de los Web Services del backend de RiskGuard. El desarrollo se organizó en ramas independientes por bounded context: feature/reports para el módulo de reportes y cumplimiento SST (KPI dashboard, tendencias históricas, alertas críticas, reportes generados, plan anual SST), feature/assessment_mitigation para evaluación de riesgos, mitigaciones, peligros y técnicos, feature/inspection_headquarters para inspecciones, sedes, áreas y activos industriales, y feature/user-authentication-monitoring-dashboard para autenticación JWT, gestión de usuarios/roles/sesiones y el dashboard de monitoreo del supervisor. Cada rama fue integrada  mediante pull requests revisadas por el equipo.

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Repository</th>
      <th>Branch</th>
      <th>Commit Id</th>
      <th>Commit Message</th>
      <th>Commit Body</th>
      <th>Evidence URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Backend</td>
      <td>develop</td>
      <td>caefcf9</td>
      <td>first commit</td>
      <td>Creación inicial del repositorio backend</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/caefcf9">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>develop</td>
      <td>3150c55</td>
      <td>Fix: update</td>
      <td>Corrección y actualización de archivos del proyecto</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/3150c55">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>767c91a</td>
      <td>chore: initial project setup with ASP.NET Core Web API</td>
      <td>Configuración inicial del proyecto con ASP.NET Core Web API</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/767c91a">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>b14dc11</td>
      <td>feat: add Shared module</td>
      <td>Agregado módulo Shared con CrudController genérico, DbContext y UnitOfWork</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/b14dc11">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>a911b0b</td>
      <td>feat(reports): add monthly_reports endpoint</td>
      <td>Agregado MonthlyReportsController con endpoints GET all, GET by id, GET by year, POST y PUT</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/a911b0b">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>a85af2b</td>
      <td>feat(reports): add cumulative_st_indicators endpoint</td>
      <td>Agregado CumulativeStIndicatorsController con endpoints GET all y GET by id</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/a85af2b">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>0e92be4</td>
      <td>feat(reports): add historical_incident_records and annual_ohs_plan endpoints</td>
      <td>Agregado HistoricalIncidentRecordsController y AnnualOhsPlanController</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/0e92be4">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>7b6ea0b</td>
      <td>feat(reports): add predictive_indicators and critical_alerts endpoints</td>
      <td>Agregado PredictiveIndicatorsController y CriticalAlertsController con GET, PUT y DELETE</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/7b6ea0b">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>2027f26</td>
      <td>feat(reports): add generated_reports, kpi_dashboard and historical_trends endpoints</td>
      <td>Agregado GeneratedReportsController, KpiDashboardController y HistoricalTrendsController</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/2027f26">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>eea1ccd</td>
      <td>feat(reports): configure Program</td>
      <td>Configuración del Program.cs con DbContext, Swagger y servicios de inyección de dependencias</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/eea1ccd">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>75c61aa</td>
      <td>feat(reports): add Resources and Transform</td>
      <td>Agregado Resources y Transform assemblers para el BC ReportsCompliance</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/75c61aa">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>f2fd93a</td>
      <td>feat(reports): integrate CQRS with Resources and Transform in controllers</td>
      <td>Integración del patrón CQRS con Resources y Transform en todos los controllers de ReportsCompliance</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/f2fd93a">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>550eb6c</td>
      <td>feat(reports): add all endpoints matching frontend usage (GET id, PUT, DELETE)</td>
      <td>Agregado endpoints adicionales GET by id, PUT y DELETE para coincidir con el consumo del frontend</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/550eb6c">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>24f36ec</td>
      <td>feat: add elements</td>
      <td>Agregado elementos adicionales del dominio de reportes</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/24f36ec">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/reports</td>
      <td>c91df25</td>
      <td>Merge pull request #1 from IsabelAponte234/feature/reports-refactor</td>
      <td>Fusión de la rama feature/reports-refactor con refactorización de controllers</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/c91df25">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/assessment_mitigation</td>
      <td>560fa99</td>
      <td>feat: add to my feature</td>
      <td>Agregado bounded contexts RiskAssessments, Mitigations, Hazards y Technicians con todos los controllers</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/560fa99">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/assessment_mitigation</td>
      <td>8d2b036</td>
      <td>Merge pull request #2 from upc-web-applications/feature/reports</td>
      <td>Fusión de la rama feature/reports al flujo de assessment_mitigation</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/8d2b036">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/inspection_headquarters</td>
      <td>5ab61d6</td>
      <td>feat: add inspection and headquarters BC</td>
      <td>Agregado bounded contexts Inspections y OrganizationAssets con InspeccionesController, PeligrosController, SedesController, AreasController y ActivosController</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/5ab61d6">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/inspection_headquarters</td>
      <td>1ce5310</td>
      <td>chore: add project configuration files</td>
      <td>Agregado archivos de configuración del proyecto inspection con EF Core y MySQL</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/1ce5310">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/user-authentication-monitoring-dashboard</td>
      <td>d35638c</td>
      <td>feat(iam): add authentication and identity access context</td>
      <td>Agregado AuthenticationController con sign-in/sign-up JWT, UsersController, RolesController, SessionsController y AccessLogsController</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/d35638c">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/user-authentication-monitoring-dashboard</td>
      <td>4eb6a26</td>
      <td>feat(monitoring): add monitoring dashboard context</td>
      <td>Agregado HeatMapZonesController, TicketsController, TechniciansController, AssetsController, PreventiveMaintenancesController y ArchivedReportsController</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/4eb6a26">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/user-authentication-monitoring-dashboard</td>
      <td>c11d837</td>
      <td>feat(shared): add shared backend infrastructure</td>
      <td>Agregado módulo Shared con CrudController genérico, DbContext, UnitOfWork y configuración EF Core</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/c11d837">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/user-authentication-monitoring-dashboard</td>
      <td>27877fd</td>
      <td>chore: add backend project configuration</td>
      <td>Agregado archivos de configuración del proyecto auth_monitoring con Swagger y MySQL</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/27877fd">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>feature/user-authentication-monitoring-dashboard</td>
      <td>c4ce846</td>
      <td>chore: add gitignore for .NET artifacts</td>
      <td>Agregado .gitignore para artefactos de compilación .NET</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/c4ce846">Ver commit</a></td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>develop</td>
      <td>fecc5e9</td>
      <td>feat: merge all branches</td>
      <td>Fusión de todas las ramas feature al branch main del repositorio backend</td>
      <td><a href="https://github.com/upc-web-applications/Backend/commit/fecc5e9">Ver commit</a></td>
    </tr>
  </tbody>
</table>

#### 5.2.3.5. Execution Evidence for Sprint Review

Durante el Sprint 3 se implementó y ejecutó la primera versión de los Web Services de RiskGuard utilizando C# y ASP.NET Core. El backend fue organizado como un monolito modular basado en Domain-Driven Design, separando las responsabilidades de la solución mediante bounded contexts. Las operaciones fueron verificadas desde Swagger UI utilizando datos de prueba y comprobando los códigos de respuesta HTTP.

##### Account Generation and Authentication BC

<p align="center">
  <img src="images/accesslog-swagger.png" width="750"/>
</p>

<p align="center">
  <img src="images/authentication-swagger.png" width="750"/>
</p>

<p align="center">
  <img src="images/roles-swagger.png" width="750"/>
</p>

<p align="center">
  <img src="images/sessions-swagger.png" width="750"/>
</p>

<p align="center">
  <img src="images/user-swagger.png" width="750"/>
</p>

*Vista general de los recursos y endpoints correspondientes al bounded context Account Generation and Authentication.*

##### Site / Area and Industrial Asset BC

<p align="center">
  <img src="images/image1-area.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image2-area.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image3-area.png"
       width="750"/>
</p>


*Vista general de los recursos y endpoints correspondientes al bounded context Site, Area and Industrial Asset.*

##### Inspection / Unsafe Condition BC

<p align="center">
  <img src="images/image4-area.png"
       width="750"/>
</p>

*Vista general de los recursos y endpoints correspondientes al bounded context Inspection and Unsafe Condition.*

##### Risk Assessment BC

<p align="center">
  <img src="images/image1-risk.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image2-risk.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image3-risk.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/hazard.png"
       width="750"/>
</p>


*Vista general de los recursos y endpoints correspondientes al bounded context Risk Assessment.*

#### Mitigation BC

<p align="center">
  <img src="images/image1-mitigation.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image2-mitigation.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image3-mitigation.png"
       width="750"/>
</p>

*Vista general de los recursos y endpoints correspondientes al bounded context Mitigation.*

##### Monitoring / Dashboard BC

<p align="center">
  <img src="images/archivedreports-swagger.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/assets-swagger.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/heatmapzones-swagger.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/preventive-swagger.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/technicians-swagger.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/tickets-swagger.png"
       width="750"/>
</p>


<p align="center">
  <img src="images/postimage-screenshot-005106.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/postimage-screenshot-005003.png"
       width="750"/>
</p>

*Vista general de los recursos y endpoints correspondientes al bounded context Monitoring and Dashboard.*

##### Reports / Compliance BC

<p align="center">
  <img src="images/image1-reports.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image2-reports.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image3-reports.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/image4-reports.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/postimage-screenshot-005106.png"
       width="750"/>
</p>

<p align="center">
  <img src="images/postimage-screenshot-005003.png"
       width="750"/>
</p>

*Vista general de los recursos y endpoints correspondientes al bounded context Reports and Compliance.*

*Video de demostración:* https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQAll8gqH1OTSZBfmPtTGWADARPeg5vTnz514xeDGxJ4mhQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=6RRLJw


#### 5.2.3.6. Services Documentation Evidence for Sprint Review

Durante este Sprint se lograron avances significativos en el desarrollo y documentación de los Web Services que soportan las funcionalidades principales de la plataforma RiskGuard. Se implementaron y documentaron múltiples endpoints REST relacionados con la autenticación de usuarios, gestión de inspecciones, evaluación de riesgos, medidas de mitigación, tickets correctivos, monitoreo por mapa de calor, mantenimientos preventivos, gestión de sedes, áreas y activos industriales, así como reportes de cumplimiento normativo SST.

Asimismo, se integró la persistencia de datos mediante una base de datos MySQL, permitiendo el almacenamiento y recuperación de la información gestionada por los distintos servicios implementados. La documentación de los endpoints fue generada utilizando OpenAPI y publicada a través de Swagger UI, facilitando la visualización de las operaciones disponibles, la determinación de parámetros, la revisión de los modelos de datos y la ejecución de pruebas utilizando datos de ejemplo.

A continuación, se presenta la relación de endpoints desarrollados durante el Sprint, incluyendo las acciones soportadas, la sintaxis de llamada y ejemplos de respuesta obtenidos a través de la documentación interactiva.

**Repositorio de Web Services:** https://github.com/upc-web-applications/Backend

**URL local de la documentación Swagger:** http://localhost:5175/swagger

**Base de datos utilizada:** MySQL

**Commits relacionados con Documentación e implementación de endpoints:**

| Commit Id | Mensaje |
|---|---|
| 767c91a | chore: initial project setup with ASP.NET Core Web API |
| 2027f26 | feat(reports): add generated_reports, kpi_dashboard and historical_trends endpoints |
| 560fa99 | feat: add to my feature |
| 5ab61d6 | feat: add inspection and headquarters BC |
| d35638c | feat(iam): add authentication and identity access context |
| 4eb6a26 | feat(monitoring): add monitoring dashboard context |

<table>
  <thead>
    <tr>
      <th>Bounded Context</th>
      <th>Recurso</th>
      <th>Endpoint base</th>
      <th>Acciones Implementadas</th>
      <th>Descripción</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5"> Account Generation and Authentication (IAM)</td>
      <td>Autenticación</td>
      <td>/api/v1/authentication</td>
      <td>POST (sign-in), POST (sign-up)</td>
      <td>Registro de usuarios con BCrypt y autenticación con generación de token JWT</td>
    </tr>
    <tr>
      <td>Usuarios</td>
      <td>/api/v1/users</td>
      <td>GET, GET {id}</td>
      <td>Consulta de usuarios registrados. El campo passwordHash se excluye por seguridad</td>
    </tr>
    <tr>
      <td>Roles</td>
      <td>/api/v1/roles</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Gestión de roles del sistema (supervisor, administrador, operario)</td>
    </tr>
    <tr>
      <td>Sesiones</td>
      <td>/api/v1/sessions</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Gestión de sesiones activas con control de validez y motivo de cierre</td>
    </tr>
    <tr>
      <td>Registros de acceso</td>
      <td>/api/v1/access-logs</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Auditoría de intentos de autenticación con IP, resultado y motivo de fallo</td>
    </tr>
    <tr>
      <td rowspan="3">Site / Area and Industrial (Organization Assets)</td>
      <td>Sedes</td>
      <td>/api/v1/headquarters</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Gestión de sedes operativas con nombre, dirección y estado (Active/Inactive)</td>
    </tr>
    <tr>
      <td>Áreas</td>
      <td>/api/v1/areas</td>
      <td>GET, GET {id}, GET /active, POST, PUT, DELETE</td>
      <td>Áreas vinculadas a una sede con nivel de riesgo. El endpoint /active filtra por estado activo</td>
    </tr>
    <tr>
      <td>Activos</td>
      <td>/api/v1/assets</td>
      <td>GET, GET {id}, GET /by-area/{areaId}, POST, PUT, DELETE</td>
      <td>Activos industriales por área. El endpoint /by-area filtra por areaId y estado activo</td>
    </tr>
    <tr>
      <td rowspan="2">Inspection</td>
      <td>Inspecciones</td>
      <td>/api/v1/inspections</td>
      <td>POST, GET /mine/{operatorId}</td>
      <td>Registro de inspecciones de condiciones inseguras. El endpoint /mine filtra por operario</td>
    </tr>
    <tr>
      <td>Peligros</td>
      <td>/api/v1/dangers</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Catálogo de peligros identificados en planta con nombre y categoría</td>
    </tr>
    <tr>
      <td rowspan="5">Risk Assessment</td>
      <td>Evaluaciones de riesgo</td>
      <td>/api/v1/risk-assessments</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Evaluaciones con probabilidad, severidad y nivel de riesgo. Filtrable por sector</td>
    </tr>
    <tr>
      <td>Patrones de riesgo</td>
      <td>/api/v1/risk-patterns</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Detección de patrones recurrentes de incidentes por sector</td>
    </tr>
    <tr>
      <td>Resúmenes diarios</td>
      <td>/api/v1/daily-summaries</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Resumen diario de riesgos nuevos, en progreso y resueltos. Filtrable por sector y fecha</td>
    </tr>
    <tr>
      <td>Alertas de patrón</td>
      <td>/api/v1/pattern-alerts</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Alertas generadas por patrones de riesgo recurrentes detectados</td>
    </tr>
    <tr>
      <td>Niveles de criticidad</td>
      <td>/api/v1/area-criticality-levels</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Niveles de criticidad por área que alimentan el mapa de calor</td>
    </tr>
    <tr>
      <td rowspan="6">Mitigation</td>
      <td>Mitigaciones</td>
      <td>/api/v1/mitigations</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Medidas de control implementadas para reducir el nivel de riesgo</td>
    </tr>
    <tr>
      <td>Tickets correctivos</td>
      <td>/api/v1/corrective-action-tickets</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Tickets correctivos con prioridad, SLA y técnico asignado</td>
    </tr>
    <tr>
      <td>Alertas SLA</td>
      <td>/api/v1/sla-alerts</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Alertas de cumplimiento de SLA para tickets próximos a vencer</td>
    </tr>
    <tr>
      <td>Notificaciones críticas</td>
      <td>/api/v1/critical-notifications</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Notificaciones enviadas cuando un ticket excede su SLA</td>
    </tr>
    <tr>
      <td>Verificaciones de medida</td>
      <td>/api/v1/measure-verifications</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Verificación de medidas de mitigación con veredicto de aprobación</td>
    </tr>
    <tr>
      <td>Historial de tickets</td>
      <td>/api/v1/ticket-histories</td>
      <td>GET, GET {id}, POST</td>
      <td>Línea de tiempo con eventos de cada ticket correctivo</td>
    </tr>
    <tr>
      <td rowspan="6">Monitoring / Dashboard</td>
      <td>Zonas mapa de calor</td>
      <td>/api/v1/heat-map-zones</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Zonas de criticidad para la visualización del mapa de calor del supervisor</td>
    </tr>
    <tr>
      <td>Tickets dashboard</td>
      <td>/api/v1/dashboard-tickets</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Bandeja de tickets del panel de monitoreo del supervisor</td>
    </tr>
    <tr>
      <td>Técnicos dashboard</td>
      <td>/api/v1/dashboard-technicians</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Directorio de técnicos disponibles para asignación de tickets</td>
    </tr>
    <tr>
      <td>Activos dashboard</td>
      <td>/api/v1/dashboard-assets</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Gestión de activos industriales desde el panel del supervisor</td>
    </tr>
    <tr>
      <td>Mantenimientos preventivos</td>
      <td>/api/v1/preventive-maintenances</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Programación de mantenimientos preventivos para activos industriales</td>
    </tr>
    <tr>
      <td>Reportes archivados</td>
      <td>/api/v1/archived-reports</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Reportes archivados del sistema de monitoreo</td>
    </tr>
    <tr>
      <td rowspan="9">Reports / Compliance</td>
      <td>Reportes mensuales</td>
      <td>/api/v1/monthly_reports</td>
      <td>GET, GET {id}, GET /year/{year}, POST, PUT</td>
      <td>Reportes mensuales de seguridad con filtro por año</td>
    </tr>
    <tr>
      <td>Indicadores acumulados ST</td>
      <td>/api/v1/cumulative_st_indicators</td>
      <td>GET, GET {id}</td>
      <td>Indicadores acumulados de Seguridad en el Trabajo</td>
    </tr>
    <tr>
      <td>Registros históricos</td>
      <td>/api/v1/historical_incident_records</td>
      <td>GET, GET {id}, POST, PUT</td>
      <td>Historial de incidentes para trazabilidad ante auditorías SUNAFIL</td>
    </tr>
    <tr>
      <td>Plan anual SST</td>
      <td>/api/v1/annual_ohs_plan</td>
      <td>GET, GET {id}, PUT</td>
      <td>Plan anual SST con cumplimiento global y desglose de actividades</td>
    </tr>
    <tr>
      <td>Indicadores predictivos</td>
      <td>/api/v1/predictive_indicators</td>
      <td>GET, GET {id}</td>
      <td>Indicadores predictivos de riesgo con tendencia</td>
    </tr>
    <tr>
      <td>Alertas críticas</td>
      <td>/api/v1/critical_alerts</td>
      <td>GET, GET {id}, PUT, DELETE</td>
      <td>Alertas críticas con estado (unresolved, in_review, resolved)</td>
    </tr>
    <tr>
      <td>Reportes generados</td>
      <td>/api/v1/generated_reports</td>
      <td>GET, GET {id}, POST, DELETE</td>
      <td>Registro de reportes generados en formato pdf o xlsx</td>
    </tr>
    <tr>
      <td>Dashboard KPI</td>
      <td>/api/v1/kpi_dashboard</td>
      <td>GET, GET {id}</td>
      <td>Indicadores KPI del dashboard ejecutivo con meta y estado visual</td>
    </tr>
    <tr>
      <td>Tendencias históricas</td>
      <td>/api/v1/historical_trends</td>
      <td>GET, GET {id}</td>
      <td>Evolución mensual de incidentes para gráficas de tendencia</td>
    </tr>
    <tr>
      <td>Shared</td>
      <td>Peligros (Hazards)</td>
      <td>/api/v1/hazards</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Catálogo de peligros identificados en planta</td>
    </tr>
    <tr>
      <td>Shared</td>
      <td>Técnicos</td>
      <td>/api/v1/technicians</td>
      <td>GET, GET {id}, POST, PUT, DELETE</td>
      <td>Directorio de técnicos para asignación a tickets y mantenimientos</td>
    </tr>
  </tbody>
</table>

##### Evidencia de interacción con Swagger UI


<p align="center">
  <img src="images/ch5-img-36.png" width="500"/>
</p>

*Ejecución del endpoint GET /api/v1/monthly_reports en Swagger UI, mostrando la respuesta exitosa (HTTP 200) con los reportes mensuales almacenados en la base de datos, incluyendo campos id, month, year, status y creationDate.*

<p align="center">
  <img src="images/ch5-img-37.png" width="500"/>
</p>

*Ejecución del endpoint DELETE /api/v1/critical_alerts/CA_001 en Swagger UI, mostrando la eliminación exitosa con respuesta HTTP 204 (The alert was deleted) y la documentación del código 404 (The alert was not found).*

<p align="center">
  <img src="images/ch5-img-38.png" width="500"/>
</p>

*Ejecución del endpoint GET /api/v1/critical_alerts en Swagger UI, mostrando la respuesta exitosa (HTTP 200) con un arreglo vacío tras la eliminación previa, junto con el schema del modelo que incluye los campos id, type, sector, riskType, message, elapsedHours y status.*


<p align="center">
  <img src="images/ch5-img-39.png" width="500"/>
</p>

*Ejecución del endpoint POST /api/v1/technicians en el backend desplegado en Render, mostrando el registro de un nuevo técnico con los campos id, documentNumber, fullName, specialty, phone, email y status.*

<p align="center">
  <img src="images/ch5-img-40.png" width="500"/>
</p>

*Ejecución del endpoint GET /api/v1/technicians/TEC_002 en el backend desplegado en Render, mostrando la consulta exitosa (HTTP 200) del técnico registrado con su información completa.*


#### 5.2.3.7. Software Deployment Evidence for Sprint Review

En esta sección se presenta la evidencia del despliegue de los distintos servicios de la plataforma RiskGuard durante el Sprint 3, incluyendo el frontend, backend real, base de datos simulada y Landing Page.

**Servicios desplegados:**

| Servicio | URL |
|---|---|
| Landing Page | https://riskguard-landingpage.vercel.app/ |
| Frontend (Firebase) | https://riskguard-a146d.web.app/login |
| Backend Real (Render) | https://riskguard-platform.onrender.com/swagger/index.html |
| Base de datos simulada (json-server en Render) | https://db-server-risk-0r34.onrender.com |

**Stack tecnológico:**

| Componente | Tecnología |
|---|---|
| Frontend | Vue 3 + PrimeVue 4 |
| Hosting Frontend | Firebase Hosting |
| Backend Real | ASP.NET Core / C# (Render) |
| Base de datos simulada | json-server con db.json (Render) |
| Base de datos real | MySQL |

**Cómo desplegar**

**Frontend (Firebase) — Paso a paso**

1. **Crear proyecto en Firebase Console**
   - Ir a https://console.firebase.google.com
   - Click en "Crear un proyecto"
   - Asignar nombre (ej: riskguard)
   - Desactivar Google Analytics
   - Esperar a que se cree

2. **Inicializar Firebase en el proyecto local**

   
   firebase login
   firebase init hosting
   
   Responder:
   - Seleccionar proyecto → elegir el proyecto creado
   - Directorio público → `dist`
   - Configurar como aplicación de una sola página → `Yes`
   - Configurar compilaciones automáticas → `No`
   - El archivo index.html ya existe → `No`

3. **Compilación y despliegue manual (primera vez)**
   
  - npm run build
  - firebase deploy


**Backend Real (Render) — Paso a paso**

1. Ir a https://dashboard.render.com
2. Click en *New +** → **Web Service*

<p align="center">
  <img src="images/postimage-screenshot-205339.png"
       width="500"/>
</p>

4. Conectar el repositorio de GitHub del backend
  
6. Configurar:
   - *Nombre:* riskguard-platform
   - *Region:* la más cercana
   - *Rama:*  main
   - *Runtime:* Docker o .NET
   - *Build Command:* `dotnet publish -c Release -o out`
   - *Start Command:* `dotnet out/RiskGuard-Platform.dll`
   - *Plan:* Free
7. Click en *Create Web Service*

<p align="center">
  <img src="images/postimage-screenshot-205902.png"
       width="455"/>
</p>

<p align="center">
  <img src="images/postimage-screenshot-210013.png"
       width="500"/>
</p>

<p align="center">
  <img src="images/postimage-screenshot-210218.png"
       width="500"/>
</p>

*Despliegue automático:* Render se configura con auto-deploy por defecto. Cada `git push` a main:
- Render detecta el cambio
- Reconstruye y redespliega automáticamente

https://riskguard-platform.onrender.com/swagger/index.html

**Mock DB (json-server en Render) — Paso a paso**

1. Ir a https://dashboard.render.com
2. Click en *New +** → **Web Service*
3. Conectar el repositorio del frontend
4. Configurar:
   - *Nombre:* db-server-risk
   - *Region:* la más cercana
   - *Rama:* main
   - *Runtime:* Node
   - *Start Command:* `npx json-server --watch server/db.json --routes server/routes.json --port $PORT`
   - *Plan:* Free
5. Click en *Create Web Service*

*Importante:* Usar `$PORT` en el Start Command, no un puerto fijo como 3000.


**Alcance del despliegue en Sprint 3**

| Producto | Estado de despliegue | Observación |
|---|---|---|
| Landing Page | https://riskguard-landingpage.vercel.app/  | Se actualizará desde la rama principal. |
| Frontend (Web App) | Desplegado en Firebase Hosting con integración continua  | La aplicación está disponible en https://riskguard-a146d.web.app |
| Backend / Web Services | Desplegado en Render | Los endpoints fueron validados mediante Swagger UI, accesible en https://riskguard-platform.onrender.com/swagger/index.html. Base de datos MySQL. |
| Base de datos simulada | Desplegada en Render como json-server | Disponible en https://db-server-risk-0r34.onrender.com. Requiere activación manual por inactividad de Render Free. |

**Landing Page desplegada**

Evidencia de Ladin page publicada:

<p align="center">
  <img src="images/EvidenciaLading1.png" width="500"/>
</p>

**Fronted desplegado**

Evidencia del fronteed publicado:

<p align="center">
  <img src="images/EvidenciaFront2.png" width="500"/>
</p>

**Backend  desplegado**

<p align="center">
  <img src="images/ch5-img-45.png" width="500"/>
</p>

<p align="center">
  <img src="images/ch5-img-46.png" width="500"/>
</p>

#### 5.2.3.8. Team Collaboration Insights during Sprint

Durante el Sprint 3, el equipo colaboró activamente en el desarrollo del Backend de RiskGuard con ASP.NET Core y arquitectura DDD. Cada integrante trabajó en su respectivo bounded context mediante ramas feature independientes, integrando los cambios al repositorio compartido a través de pull requests. A continuación se presentan los analíticos de colaboración y el historial de commits obtenidos desde el repositorio upc-web-applications/Backend.

El repositorio cuenta con 6 ramas activas: main, develop, feature/reports, feature/assessment_mitigation, feature/inspection_headquarters y feature/user-authentication-monitoring-dashboard, reflejando la separación por bounded context adoptada por el equipo.

**Capturas de analíticos y commits en GitHub:**

*Estructura de ramas del repositorio utilizada durante el Sprint 3.*

<h5 align="center">Ramas creadas</h5>

<p align="center">
  <img src="images/sprint3-branches.png" width="600"/>
</p>

*Historial de commits organizado cronológicamente en el repositorio.*

<h5 align="center">Orden de commits</h5>

<p align="center">
  <img src="images/sprint3-commits-order.png" width="600"/>
</p>

*Resumen estadístico del repositorio con cantidad de commits y contribuciones por autor.*

<h5 align="center">Commits por usuario</h5>

<p align="center">
  <img src="images/sprint3-commits-per-user.png" width="600"/>
</p>

*Network graph del repositorio mostrando el flujo de ramas y merges del equipo.*

<h5 align="center">Network graph</h5>

<p align="center">
  <img src="images/sprint3-network-graph.png" width="600"/>
</p>

*Registro completo de todos los commits realizados durante el Sprint 3.*

<h5 align="center">Todos los commits</h5>

<p align="center">
  <img src="images/sprint3-all-commits.png" width="600"/>
</p>


### 5.2.4. Sprint 4

#### 5.2.4.1. Sprint Planning 4.

En el Sprint 4, el equipo se enfocará en integrar el frontend desarrollado en Vue 3 con los Web Services implementados en ASP.NET Core durante el sprint anterior. El propósito principal será reemplazar el consumo de datos simulados de json-server por los endpoints reales del backend, de modo que los principales flujos de RiskGuard funcionen de extremo a extremo..

La integración se realizará progresivamente por bounded context. Para cada módulo se revisarán y alinearán los contratos de la API, las rutas, los modelos de datos y los códigos de respuesta; después se adaptarán los servicios y stores del frontend, se configurarán las variables de entorno y CORS, y se validarán las operaciones de consulta, registro, actualización y eliminación. También se corregirán incompatibilidades entre ambas aplicaciones y se incorporará un manejo consistente de estados de carga, validaciones, errores y sesiones expiradas.

El sprint priorizará los flujos críticos de los tres perfiles de usuario. El operario deberá poder autenticarse, registrar inspecciones o condiciones inseguras y consultar su seguimiento; el supervisor podrá gestionar riesgos, mitigaciones, tickets, técnicos, sedes, áreas y activos; y el gerente visualizará indicadores, tendencias y reportes construidos con información obtenida del backend real. La integración se considerará terminada cuando estos recorridos puedan ejecutarse desde la interfaz desplegada sin depender de información mock y los datos creados o modificados se mantengan correctamente en la base de datos.

| **Campo** | **Detalle** |
|---|---|
| Sprint # | 4 |
| Date | 2026-03-07 |
| Time | 4:00 PM |
| Location | Reunión virtual (Google Meet) |
| Prepared By |Flores Eusebio, Angel Thyago |
| Attendees (to planning meeting) | Aponte Pablo, Isabel Luisa / Laura Acosta, Victor Jhosef / Blancas Chávez, Carlos Franco / Flores Eusebio, Angel Thyago |
| Sprint n – 3 Review Summary | Durante el Sprint 3 se implementaron los Web Services de RiskGuard con C# y ASP.NET Core, organizados mediante Domain-Driven Design y bounded contexts. Se desarrollaron endpoints REST para autenticación y generación de cuentas, sedes, áreas, activos industriales, inspecciones, evaluación y mitigación de riesgos, técnicos, monitoreo y reportes. Asimismo, se incorporaron persistencia en MySQL, autenticación JWT y documentación con Swagger. Los servicios fueron integrados en la rama principal, desplegados en Render y validados individualmente mediante solicitudes HTTP; sin embargo, el frontend todavía no consume de forma completa el backend real. |
| Sprint n – 3 Retrospective Summary | El equipo logró distribuir el desarrollo del backend por bounded context y consolidar los módulos mediante ramas feature y pull requests. Como principal oportunidad de mejora se identificó que algunos contratos, nombres de campos y estructuras de respuesta no coinciden completamente con los modelos utilizados por el frontend. Para este sprint se acordó validar primero cada contrato con Swagger, integrar módulo por módulo, mantener una configuración centralizada de la URL base y del token JWT, y realizar pruebas de extremo a extremo antes de considerar terminada cada funcionalidad. |
| Sprint Goal | Our focus is on integrating the RiskGuard frontend with the real ASP.NET Core backend across the prioritized bounded contexts. We believe it delivers a functional end-to-end product that replaces mock data with persistent information, secure JWT authentication and role-based access for operators, supervisors and managers. This will be confirmed when users can complete the main business flows from the deployed web application, the frontend can successfully execute the required CRUD operations through the REST API, data changes persist in MySQL, and loading, validation and error states are handled consistently without relying on json-server. |
| Sprint n Velocity |  SP |
| Sum of Story Points |  SP |

#### 5.2.4.2. Aspect Leaders and Collaborators.
#### 5.2.4.3. Sprint Backlog 4.
#### 5.2.4.4. Development Evidence for Sprint Review.
#### 5.2.4.5. Execution Evidence for Sprint Review.
#### 5.2.4.6. Services Documentation Evidence for Sprint Review.
#### 5.2.4.7. Software Deployment Evidence for Sprint Review.
#### 5.2.4.8. Team Collaboration Insights during Sprint.

## 5.3. Validation Interviews

En esta sección se registran las entrevistas de validación del proyecto. A diferencia de las entrevistas de la sección 2.2, donde se buscaba descubrir problemas y necesidades, aquí el objetivo es verificar si lo que construimos realmente funciona para los usuarios y si les resulta fácil de usar.

### 5.3.1. Diseño de Entrevistas

Al inicio de cada sesión se le explica al participante que el objetivo es probar la aplicación, no sus conocimientos, por lo que puede interactuar con total libertad. La sesión se divide en tres momentos: exploración del Landing Page, ejecución de tareas en la aplicación y cuestionario final.

**Datos de registro del participante**

- Nombre completo
- Edad
- Distrito de residencia
- Cargo actual y empresa (o sector industrial)
- Años de experiencia en el sector

**Segmento objetivo 1: Operarios de Planta**

*Elementos a validar: Landing Page y Web Application (registro de incidentes y seguimiento de reportes).*

**User Flows a validar (sección 4.4.4):**

- User Flow 1 – Registro y seguimiento de incidente. Acceder al dashboard del operario, presionar "Registrar inspección", completar el formulario de reporte rápido (tipo de incidente, sector, urgencia, descripción y foto opcional), enviar el reporte y recibir la confirmación con número de ticket. Luego consultar el estado del reporte desde la sección "Inspecciones" y recibir notificaciones de cambio de estado.

**Tareas asignadas:**

- Navegar el Landing Page, revisar las secciones de características, metodología y estadísticas, y acceder a la aplicación.
- Iniciar sesión con sus credenciales de operario.
- Desde el dashboard, identificar el botón "Registrar inspección" y acceder al formulario de reporte rápido.
- Completar todos los campos obligatorios del formulario: seleccionar tipo de incidente, sector, nivel de urgencia (usando los botones de color) e ingresar una descripción.
- Adjuntar una foto de evidencia (opcional) y enviar el reporte.
- Verificar que el sistema muestre la confirmación con el número de ticket asignado.
- Navegar a la sección "Inspecciones" y localizar el reporte recién enviado para revisar su estado actual.
- Consultar el detalle de un reporte anterior y verificar el historial de cambios de estado.

**Preguntas de validación:**

1. ¿El Landing Page le ayudó a entender para qué sirve RiskGuard? ¿Qué sección le llamó más la atención?
2. Al ver el dashboard del operario, ¿pudo identificar rápidamente dónde registrar un nuevo reporte? ¿Le pareció intuitivo?
3. Los campos del formulario de reporte (tipo de incidente, sector, urgencia, descripción y foto), ¿le parecieron suficientes para describir una situación de riesgo? ¿Sobra o falta algún campo?
4. ¿Los botones de color para seleccionar el nivel de urgencia (verde, naranja, rojo) le resultaron claros? ¿Entendió la diferencia entre cada nivel?
5. Al enviar el reporte, ¿la confirmación con el número de ticket le generó confianza de que su reporte fue recibido?
6. En la sección "Inspecciones", ¿le resultó fácil encontrar su reporte y entender en qué estado se encuentra?
7. ¿Hubo algún botón o pantalla donde no supiera qué hacer?
8. En una escala del 1 al 5, ¿qué tan fácil le resultó completar el proceso de registro de un incidente?
9. Comparado con el proceso actual de reporte en su planta, ¿considera que este sistema representaría una mejora real? ¿Por qué?
10. Si pudiera cambiarle una sola cosa a la aplicación, ¿cuál sería?

**Segmento objetivo 2: Supervisores de Seguridad y Mantenimiento**

*Elementos a validar: Landing Page y Web Application (gestión de tickets, cierre de acciones correctivas y configuración de planta).*

**User Flows a validar (sección 4.4.4):**

- User Flow 2 – Gestión de tickets y cierre de acciones correctivas. Acceder al dashboard del supervisor con el mapa de calor y el panel de alertas activas, seleccionar una alerta crítica, revisar el detalle del ticket, asignar un técnico de mantenimiento, verificar la implementación de la medida correctiva y aprobar o rechazar el cierre del ticket.
- User Flow 4 – Configuración de planta. Acceder al módulo de configuración, crear una nueva sede con nombre y descripción, registrar un nuevo activo vinculado a un sector activo, e intentar desactivar un sector con historial de incidentes.

**Tareas asignadas:**

- Navegar el Landing Page, revisar las secciones de características y metodología, y acceder a la aplicación.
- Iniciar sesión con sus credenciales de supervisor.
- En el dashboard, interpretar el mapa de calor e identificar qué sectores requieren atención inmediata.
- Revisar el panel de alertas activas ordenadas por criticidad y seleccionar una alerta crítica.
- Acceder al detalle del ticket y revisar la información completa
- Asignar un técnico de mantenimiento activo al ticket y confirmar la asignación.
- Identificar un ticket con etiqueta "SLA Incumplido" y verificar su señalización visual.
- Navegar al módulo de configuración y crear una nueva sede.

**Preguntas de validación:**

1. ¿El Landing Page le transmitió confianza sobre la plataforma? ¿Le quedó claro cómo RiskGuard ayudaría en su rol de supervisor?
2. Al ver el dashboard con el mapa de calor y las alertas activas, ¿la disposición de la información le permitió identificar rápidamente qué sectores requieren atención?
3. ¿Los badges de color  le resultaron claros para diferenciar la urgencia de cada ticket?
4. En el detalle del ticket, ¿la información presentada  es suficiente para tomar una decisión sobre la acción correctiva?
5. ¿El proceso de asignar un técnico al ticket le pareció directo y eficiente? ¿Cambiaría algo del selector de técnicos?
6. La etiqueta "SLA Incumplido", ¿le ayuda a priorizar sus acciones? ¿Agregaría alguna otra señal visual?
7. En el módulo de configuración, ¿el flujo de crear sedes y registrar activos le pareció sencillo y completo?
8. En una escala del 1 al 5, ¿qué tan completo considera el flujo de gestión de tickets para sus necesidades diarias?
9. ¿Este sistema le permitiría reducir el tiempo que actualmente dedica a gestionar incidentes de manera manual?
10. Si pudiera cambiarle una sola cosa a la aplicación, ¿cuál sería?

**Segmento objetivo 3: Gerentes y Administradores**

*Elementos a validar: Landing Page y Web Application (dashboard ejecutivo, indicadores predictivos y exportación de reportes).*

**User Flows a validar (sección 4.4.4):**

- User Flow 3 – Dashboard ejecutivo y exportación de reportes. Iniciar sesión como gerente y acceder al dashboard ejecutivo, revisar los cuatro indicadores clave (incidentes activos, resueltos en el mes, sectores críticos, cumplimiento del plan anual de SST), hacer clic en el indicador de sectores críticos para ver el detalle, acceder a la sección de tendencias de accidentabilidad, filtrar por sector, exportar la gráfica en PNG, navegar al módulo de reportes, seleccionar tipo de reporte y período, y generar el PDF

**Tareas asignadas:**

- Navegar el Landing Page, revisar las secciones de estadísticas y soluciones por rol, y acceder a la aplicación.
- Iniciar sesión con sus credenciales de gerente.
- En el dashboard ejecutivo, interpretar los cuatro indicadores clave 
- Hacer clic sobre el indicador de "Sectores críticos" y revisar el detalle desplegado con las alertas activas por sector.
- Acceder a la sección de tendencias de accidentabilidad y revisar la gráfica de evolución mensual diferenciada por tipo de incidente.
- Aplicar el filtro por sector en la gráfica de tendencias y exportar la gráfica en formato PNG.
- Navegar al módulo de reportes y generar un reporte mensual: seleccionar el tipo "Reporte mensual", elegir mes y año, y hacer clic en "Generar reporte".
- Generar un reporte de auditoría para SUNAFIL: seleccionar rango de fechas, elegir formato (PDF o Excel) y generar.
- Revisar el historial de reportes generados: filtrar, previsualizar y re-descargar un reporte anterior.
- Revisar los indicadores predictivos y su interpretación.

**Preguntas de validación:**

1. ¿El Landing Page le ayudó a entender el valor de RiskGuard para su gestión? ¿Qué sección le pareció más relevante?
2. Los cuatro indicadores del dashboard ejecutivo (incidentes activos, resueltos, sectores críticos, cumplimiento SST), ¿son los que necesita ver en primera instancia? ¿Falta o sobra alguno?
3. Al hacer clic en "Sectores en estado crítico", ¿el detalle con el listado de sectores y alertas activas le proporcionó información suficiente para tomar decisiones?
4. La gráfica de tendencias, ¿le resultó clara y útil para identificar patrones? ¿El filtro por sector le pareció práctico?
5. ¿La exportación de la gráfica en PNG le resulta útil para sus presentaciones al directorio?
6. El proceso de generar un reporte mensual (seleccionar tipo, período, formato), ¿le pareció directo y sin pasos innecesarios?
7. ¿Los formatos de auditoría exportables serían suficientes para responder ante una inspección de SUNAFIL sin preparar reportes adicionales manualmente?
8. El historial de reportes con opciones de filtrar, previsualizar, re-descargar y eliminar, ¿cubre sus necesidades de gestión documental?
9. Los indicadores predictivos que anticipan posibles accidentes, ¿le resultarían útiles para justificar inversiones preventivas ante el directorio?
10. En una escala del 1 al 5, ¿qué tan alineado está este dashboard ejecutivo con lo que necesita para su gestión diaria de SST?
11. ¿Cuánto tiempo estima que le ahorraría mensualmente el uso de este sistema comparado con su proceso actual de reportería?
12. Si pudiera cambiarle una sola cosa al módulo gerencial, ¿cuál sería?

### 5.3.2. Registro de Entrevistas

**Segmento objetivo #1: Operarios de Planta**


| **Entrevista Nro. 1** |
|---|
| <img src="images/bc/Operario.png" width="330" hspace="230"> |
| **Entrevistado N°1:** Fabrizio Vacca <br> **Edad:** 28 años<br>**Ubicación:** Los Olivos<br>**Cargo:** Operario de Planta — Sector Manufactura<br><br> **Entrevista:** https://1drv.ms/v/c/7E97073B2DC02368/IQAE46rrHvs3QJDtniYrXsG0AR8jxBw5mSr1altIVn-HNBA?e=eYUCdP <br>**Instante del que inicia:** 00:00<br> **Duración:** 12:27 <br><br> **Resumen:** <br><br> El participante indicó que el Landing Page le transmitió confianza al ver el mensaje principal "Predice los riesgos antes de que ocurran", señalando que refleja una necesidad real en su planta donde los incidentes muchas veces no se reportan a tiempo. Destacó la sección de estadísticas, especialmente el dato de 83% de trabajadores que mejoran cuando sus supervisores usan herramientas de seguimiento, considerándolo muy cercano a su realidad. Al ingresar a la aplicación, identificó rápidamente el botón de Registrar Inspección sin necesidad de orientación, calificando el dashboard como intuitivo y directo. Respecto al formulario, indicó que los campos son suficientes para describir una situación de riesgo real, valorando especialmente los botones de color para el nivel de urgencia, asociando el rojo con situaciones que requieren atención inmediata. La confirmación con el número de ticket le generó confianza de que su reporte fue recibido correctamente, algo que destacó como una diferencia clave frente al proceso actual en su planta donde el reporte se hace en papel y no hay forma de hacer seguimiento. En la sección de Inspecciones, encontró fácilmente su reporte y comprendió los estados Pendiente, En Progreso y Resuelto sin necesidad de explicación. Calificó la facilidad de uso con un 5 de 5, afirmando que el sistema representaría una mejora real ya que actualmente el proceso de reporte es lento, manual y muchas veces los reportes se pierden. Como única sugerencia, mencionó que agregaría la opción de reportar la ubicación exacta dentro del área mediante un mapa simple. |


| **Entrevista Nro. 2** |
|---|
| <img src="images/ch5-img-47.png" width="330" hspace="230"> |
| **Entrevistado N°2:** Rocío Acosta <br> **Edad:** 21 años<br>**Ubicación:** Pueblo Libre<br>**Cargo:** Operaria de Producción<br><br>**Entrevista:** https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQDzCVuI3MO7Qq7Q2wM__nhIAXxVlF9JemhOtM5P4NV_WjA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0% <br>**Instante del que inicia:** 00:00<br> **Duración:** 5:51 <br><br> **Resumen:** <br><br> La participante indicó que el Landing Page le permitió entender rápidamente que RiskGuard es una plataforma para reportar riesgos en planta. Destacó la sección de estadísticas como la que más le llamó la atención, señalando que los números reales de incidentes reducidos le parecen importantes y generan credibilidad. Al ingresar a la aplicación, identificó rápidamente el botón de Registrar Inspección, calificándolo como intuitivo y visible desde el dashboard. Respecto al formulario, consideró que los campos son completos y suficientes para describir un incidente, valorando especialmente la opción de adjuntar una foto como muy útil para estos casos. Los botones de color para el nivel de urgencia le resultaron muy claros, asociándolos con un semáforo: verde es leve, naranja es medio y rojo es urgente. La confirmación con el número de ticket le generó confianza y tranquilidad de que su reporte queda registrado y puede hacer seguimiento. En la sección de Inspecciones, encontró su reporte rápidamente, destacando que los estados con colores y la organización facilitan la navegación. No identificó ninguna pantalla o botón donde no supiera qué hacer, señalando que todo fue directo y guiado paso a paso. Calificó la facilidad de uso con un 5 de 5, afirmando que los pasos son claros y no solicitan información innecesaria. Confirmó que el sistema representaría una mejora real ya que actualmente usan papel, los reportes se pierden y no hay forma de verificar si alguien los está atendiendo. Como única sugerencia, mencionó que haría las letras del formulario más grandes y claras, ya que en pantallas con fondo oscuro cuesta leer textos pequeños, especialmente desde el celular. |


**Segmento objetivo #2: Supervisores de Seguridad y Mantenimiento**

| **Entrevista Nro. 1** |
|---|
| <img src="images/ch5-img-48.png" width="330" hspace="230"> |
| **Entrevistado N°2:** Álvaro Pablo <br> **Edad:** 25 años<br>**Ubicación:** Barranca<br>**Cargo:** Supervisor de seguridad y mantenimiento<br><br> **Entrevista:** https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQB1uHcy34fvSqQwXjrQbD-iAe9CaOKMJZslPIPAD3BTcko <br>**Instante del que inicia:** 00:00<br> **Duración:** 7:18 <br><br> **Resumen:** <br><br> El participante indicó que el Landing Page le transmitió confianza porque identifica los procesos de planta relacionados con seguridad industrial, destacando que los colores son intuitivos y que la plataforma aplica la metodología IPERC, la cual utiliza en su campo de ingeniería industrial. Al ver el dashboard con el mapa de calor, identificó rápidamente qué sectores requieren atención gracias a la diferenciación por colores, asociando el rojo con criticidad grave. Los badges de color le resultaron claros para diferenciar la urgencia de cada ticket. Respecto al detalle del ticket, consideró que la información presentada es suficiente para tomar una decisión sobre la acción correctiva, ya que identifica el sector y muestra el estado actual del problema. El proceso de asignar un técnico le pareció directo y eficiente. La etiqueta "SLA Incumplido" le resultó entendible para priorizar acciones y no sugirió agregar otra señal visual. En el módulo de configuración, el flujo de crear sedes y registrar activos le pareció sencillo y completo, valorando los nombres claros y las descripciónes rápidas de cada proceso. Calificó la completitud del flujo de gestión de tickets con un 4 de 5, señalando que el sistema ayuda a identificar lo que ocurre de manera rápida y centralizada. Confirmó que el sistema reduciría el tiempo dedicado a gestionar incidentes, ya que actualmente debe llenar documentos físicos, hacer llamadas y registrar en bases de datos manuales. Como única sugerencia, mencionó que cambiaría los colores del fondo en la sección de alertas, haciendo que el rojo sea más llamativo para destacar mejor las alertas críticas. |


### 5.3.3. Evaluaciones según heurísticas

<table>
<tr><td><strong>CARRERA</strong></td><td> Ingeniería de Software</td></tr>
<tr><td><strong>CURSO</strong></td><td> Aplicaciones Web</td></tr>
<tr><td><strong>SECCIÓN</strong></td><td> 12190</td></tr>
<tr><td><strong>PROFESORES</strong></td><td> Todos</td></tr>
<tr><td><strong>AUDITOR</strong></td><td> RiskGuard Team</td></tr>
<tr><td><strong>CLIENTE(S)</strong></td><td>  Fabrizio Vacca, Rocío Acosta, Jorge Surco, Álvaro Pablo, Tiziano Nicoletti </td></tr>
</table>

**Usability – Inclusive Design – Information Architecture**

**SITE o APP A EVALUAR:** RiskGuard Web Application

**TAREAS A EVALUAR:**

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Inicio de sesión y redirección por rol (Operario, Supervisor, Gerente)
2. Registro de un incidente desde el dashboard del operario
3. Seguimiento de reportes desde la sección "Inspecciones"
4. Visualización del mapa de calor y panel de alertas del supervisor
5. Asignación de técnico a un ticket desde el detalle
7. Creación de sedes y registro de activos en el módulo de configuración
8. Visualización del dashboard ejecutivo con indicadores clave
9. Exportación de gráficas de tendencias en PNG
10. Generación de reportes mensuales y de auditoría SUNAFIL

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Gestión de contraseñas y recuperación de cuentas
2. Administración de roles y permisos de usuario
4. Integración con sistemas externos de nómina o ERP

**ESCALA DE SEVERIDAD:**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

| Nivel | Descripción |
|-------|-------------|
| 1 | **Problema superficial:** puede ser fácilmente superado por el usuario u ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo. |
| 2 | **Problema menor:** puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente release. |
| 3 | **Problema mayor:** ocurre frecuentemente o los usuarios no son capaces de resolverlo. Es importante que sea corregido y se le debe asignar una prioridad alta. |
| 4 | **Problema muy grave:** un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento. |


**TABLA RESUMEN:**

| # | Problema | Escala de severidad | Heurística/Principio violada(o) |
|---|----------|:-------------------:|-------------------------------|
| 1 | El formulario de reporte no permite adjuntar más de una foto de evidencia | 2 | Usability: Flexibilidad y eficiencia de uso |
| 2 | El campo de descripción del incidente no incluye texto de ejemplo o placeholder orientativo | 2 | Usability: Ayuda y documentación |
| 3 | La sección "Inspecciones" no ofrece filtros por estado del reporte (pendiente, en progreso, cerrado) | 3 | Information Architecture: Is it findable? |
| 4 | El selector de técnicos no muestra la carga de trabajo actual de cada técnico | 2 | Usability: Visibilidad del estado del sistema |
| 5 | Al exportar gráficas de tendencias, solo se ofrece formato PNG sin opción de tabla con datos numéricos | 2 | Usability: Flexibilidad y eficiencia de uso |
| 6 | El dashboard ejecutivo no incluye un indicador de "días sin accidentes" | 2 | Information Architecture: Is it useful? |
| 7 | No existe la opción de configurar alertas personalizadas por correo electrónico cuando los indicadores superan umbrales definidos | 3 | Usability: Flexibilidad y eficiencia de uso |
| 8 | El flujo de cierre de ticket no permite al técnico adjuntar fotos de evidencia de la medida implementada | 3 | Usability: Correspondencia entre el sistema y el mundo real |
| 9 | No se incluyen notas internas visibles solo para el supervisor en el detalle del ticket | 2 | Usability: Flexibilidad y eficiencia de uso |
| 10 | Las etiquetas de urgencia por color no incluyen texto alternativo descriptivo para accesibilidad | 3 | Inclusive Design: Proporciona experiencias comparables |

**DESCRIPCIÓN DE PROBLEMAS:**

**PROBLEMA #01:** Los colores del panel de alertas activas no generan suficiente contraste visual para destacar las alertas críticas

**Severidad:** 2

**Heurística violada:** Usability – Visibilidad del estado del sistema

**Problema:**

En el panel de "Alertas activas" del dashboard del supervisor, el badge "Crítico" se muestra en un tono rojo sobre fondo oscuro que no genera el contraste suficiente para captar la atención de manera inmediata. Aunque el mapa de calor operativo sí diferencia los sectores con colores llamativos (rojo para crítico, amarillo para alto, verde para bajo), el panel lateral de alertas no replica esa misma intensidad visual. Esto puede provocar que el supervisor no perciba una alerta crítica con la urgencia que requiere al revisar rápidamente el dashboard.

<p align="center">
  <img src="images/ch5-img-49.png" width="600">
</p>

**Recomendación:**
Aplicar un fondo con tinte rojo sutil en las filas de alertas críticas dentro del panel lateral, de modo que se distingan visualmente de las alertas de menor prioridad.


**PROBLEMA #02:** Las letras del formulario de registro de incidentes son pequeñas y difíciles de leer en fondo oscuro

**Severidad:** 2

**Heurística violada:** Inclusive Design – Proporciona experiencias comparables

**Problema:**

En el formulario de registro de inspección del operario, las etiquetas de los campos y el texto dentro de los inputs se muestran en un tamaño de fuente reducido sobre un fondo oscuro, lo que dificulta la lectura rápida, especialmente cuando el usuario accede desde un dispositivo móvil. Este problema fue reportado directamente por la operaria entrevistada, quien señaló que en planta se consulta el celular de forma rápida y los textos pequeños con fondo oscuro dificultan la interacción. Esto puede provocar errores al completar los campos o que el usuario desista de registrar el incidente.

<p align="center">
  <img src="images/ch5-img-50.png" width="600">
</p>

**Recomendación:**
Aumentar el tamaño de fuente de las etiquetas y campos del formulario a un mínimo, y mejorar el contraste entre el texto y el fondo oscuro utilizando tonos más claros o blancos para las letras. Considerar también un espaciado mayor entre campos para facilitar la interacción táctil en dispositivos móviles.


**PROBLEMA #03:** El formulario de reporte no permite indicar la ubicación exacta del incidente dentro del área

**Severidad:** 2

**Heurística violada:** Usability – Correspondencia entre el sistema y el mundo real

**Problema:**

El operario puede seleccionar la planta y el área general del incidente, pero no existe una opción para señalar la ubicación exacta dentro de dicha área. En plantas grandes, un mismo sector tiene múltiples zonas de trabajo, lo que dificulta al técnico localizar el problema reportado.

<p align="center">
  <img src="images/ch5-img-51.png" width="600">
</p>

**Recomendación:**
Incorporar un mapa simple o selector visual que permita al operario marcar el punto aproximado donde ocurrió el incidente.




## 5.4. Video About-the-Product


El video About-the-Product presenta RiskGuard como una plataforma web de seguridad industrial predictiva dirigida a empresas manufactureras y logísticas del Perú. El contenido está orientado a los visitantes del Landing Page que desean conocer el modelo de negocio y las características principales de la solución, así como a los usuarios de la aplicación que buscan comprender los procesos soportados por el sistema.

El video muestra las funcionalidades clave de RiskGuard organizadas por rol de usuario: el registro rápido de inspecciones y condiciones inseguras por parte del operario, la gestión de alertas activas y asignación de técnicos por parte del supervisor mediante el mapa de calor operativo, y la visualización de indicadores predictivos, gráficas de tendencias y generación de reportes de cumplimiento normativo por parte del gerente. El tono de comunicación es técnico, directo y orientado a resultados, consistente con la identidad visual y verbal del producto.

El video incluye el testimonio positivo de Rocío Acosta, operaria de producción que participó en las entrevistas de validación, quien señaló: *"RiskGuard me parece una solución viable para nosotros en planta, 
porque ahora usamos una decoumentacion basica y los reportes se pierden. Con esto puedo 
reportar rápido y saber si alguien lo está atendiendo."*

<p align="center">
  <img src="https://i.postimg.cc/hjPhggWj/Captura-de-pantalla-2026-07-07-212302.png" width="600">
</p>

**Duración:** 3:02

**Publicación en Microsoft Stream:** https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQDS3kUSnobBSYNlDg4pDzxSAXNcqLYT66AZhYrsAVPt7_E?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJ

**Publicación en YouTube:** https://youtu.be/ZD5rg0QELU0


## Video About The Team

El video About-the-Team resume el proceso de trabajo realizado por el equipo RiskGuard Solutions durante el ciclo de desarrollo del proyecto. El contenido incluye escenas de sesiones de trabajo real del equipo, complementadas con narración en voz en off que describe el proceso de ingeniería aplicado a lo largo de los sprints. Además, incluye el testimonio ante cámara de cada integrante del equipo describiendo las actividades realizadas, el logro de outcomes y el desarrollo de competencias alcanzados.

**Pauta de secuencias de contenido:**

| Sección | Inicio | Descripción |
|---|---|---|
| Introducción | 00:00:00 | Presentación del equipo RiskGuard Solutions y objetivo del proyecto |
| Contexto del problema | 00:00:35 | Problemática de seguridad industrial en el Perú y propuesta de solución |
| Avance 1 - Sprint 1 | 00:01:26 | Documentación, Event Storming, diseño en Figma y despliegue de Landing Page |
| Sprint 2 | 00:02:07 | Desarrollo del frontend, flujos por rol de usuario |
| Sprint 3 | 00:03:21 | Desarrollo del backend |
| Sprint 4 | 00:03:46 | Desarrollo del backend |
| Reflexión del equipo | 00:04:029 | Retos enfrentados, aprendizajes y dinámica de trabajo |
| Testimonio - Isabel Aponte | 00:05:05 | Actividades, outcomes y competencias desarrolladas |
| Testimonio - Angel Flores | 00:06:18 | Actividades, outcomes y competencias desarrolladas |
| Testimonio - Carlos Blancas | 00:06:18 | Actividades, outcomes y competencias desarrolladas |
| Testimonio - Angel Flores | 00:08:06 | Actividades, outcomes y competencias desarrolladas |
| Testimonio - Victor Laura | 00:09:22 | Actividades, outcomes y competencias desarrolladas |

[![Captura-de-pantalla-2026-07-08-135341.png](https://i.postimg.cc/DZqGm37y/Captura-de-pantalla-2026-07-08-135341.png)](https://postimg.cc/62pq1S7D)

**Duración:** 10:43

**Publicación en Microsoft Stream:** https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241e158_upc_edu_pe/IQC62MWXlu3BSrX6BPSJ10IbAU8bJK86j_s47jJrOM_iphI?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=YnZe0R

**Publicación en YouTube:** https://youtu.be/-lwwjGcMRxY?si=OqaPV_xGQ6MjG0Fw
