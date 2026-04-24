
# Capítulo IV: Product Design


## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines

**Logo:**

El logo de RiskGuard combina robustez visual y autoridad técnica a través de un diseño que evoca un escudo de protección integrado con elementos industriales. La tipografía fuerte y geométrica transmite precisión y control, mientras que el uso del color naranja sobre fondo oscuro genera un contraste inmediato que comunica alerta y acción. La disposición compacta del logotipo junto al nombre asegura reconocimiento rápido en entornos de alta densidad informativa como dashboards industriales.

  <div align="center">
  <p>
    <b>Grafico 12</b>: RiskGuard Logo
  </p>
    
![Foto](images/icon.png)
  
  <p>
    <i><b>Fuente</b>: Elaboración propia en Figma </i>
  </p>
</div>

**Branding:**

RiskGuard busca transmitir autoridad, precisión y prevención activa. El sistema de identidad visual emplea una estética "sala de control": fondos oscuros profundos, acentos naranjas intensos y tipografía bold geométrica. El tono visual debe inspirar confianza técnica y urgencia operativa sin generar pánico. Toda comunicación visual refuerza la idea de que los riesgos son detectables, medibles y controlables antes de que ocurran.

---

**Typography:**

Toda la aplicación utiliza la tipografía **Geist** (o alternativa: **Inter**) para mantener consistencia visual y una apariencia técnica moderna, alineada con entornos industriales digitales.

- **Encabezados / Display:** Geist Bold, tamaño entre 48 a 72 px. Usados en el hero y títulos de sección principales. Permite mezcla de color blanco y naranja dentro del mismo heading para jerarquía de impacto.
- **Títulos de sección (H2):** Geist SemiBold, entre 28 a 32 px, color blanco `#FFFFFF`.
- **Subtítulos / Labels de card (H3):** Geist Medium, entre 16 a 18 px, color blanco `#FFFFFF`.
- **Texto de párrafo / Descripción:** Geist Regular, 13 a 15 px, color gris `#8A8F9A`. Interlineado de 1.6x para garantizar legibilidad sobre fondos oscuros.
- **Botones y etiquetas:** Geist SemiBold, 14 a 16 px. Texto en blanco sobre fondo naranja primario.
- **Tags / Badges de categoría:** Geist Regular Uppercase, 10 a 11 px, letter-spacing 0.05em. Usados como indicadores de tipo de feature (ej. "CRÍTICO", "NUEVO", "IA").

El interlineado general se mantiene en 1.5x–1.6x para textos de cuerpo, asegurando lectura cómoda en pantallas de alto contraste.

---

**Colors:**

La paleta de RiskGuard refuerza el concepto de vigilancia industrial activa y control de riesgos en tiempo real:

- `#0A0C0F` → Fondo principal de la aplicación. Tono casi negro que maximiza el contraste con los elementos de interfaz y simula el ambiente de una sala de control nocturna.
- `#111418` → Fondo secundario. Utilizado en secciones de contenido alternadas para crear separación visual sin romper la coherencia oscura.
- `#1A1E24` → Superficies de cards y componentes. Aporta profundidad y diferenciación entre capas de UI sin generar ruido visual.
- `#2A2F38` → Bordes y separadores. Delimita componentes de forma sutil manteniendo la cohesión visual del tema oscuro.
- `#FF5B00` **(Primario)** → Naranja de acción y alerta. Es el color de identidad central de RiskGuard: representa urgencia, precisión y acción preventiva. Se usa en CTAs, highlights y elementos interactivos clave.
- `#FF7A2F` → Naranja hover / variante clara. Estado activo de botones e interacciones. Complementa el naranja primario aportando feedback visual inmediato.
- `#FFFFFF` → Texto principal. Máximo contraste sobre fondos oscuros. Usado en headings, títulos de card y etiquetas destacadas.
- `#8A8F9A` → Texto secundario / descriptivo. Aporta jerarquía textual sin competir visualmente con los elementos de acción.
- `#00C97B` → Verde de éxito / estado operativo. Indica sistemas activos, alertas resueltas o métricas positivas.
- `#FF3B30` → Rojo de peligro / estado crítico. Señala riesgos no atendidos, fallos de sistema o incidentes activos.

> El color primario `#FF5B00` simboliza alerta controlada y acción industrial. Se usa de forma estratégica sobre una interfaz predominantemente oscura, logrando máximo impacto visual con mínima saturación cromática.

---

**Spacing:**

Se aplican espacios amplios entre secciones para evitar la sensación de saturación en interfaces de alta densidad informativa. Margen mínimo de contenido: **16 px**. Espaciado base entre elementos internos de componentes: **8 px**. Padding interno de cards y secciones: **24 a 32 px**. El espaciado generoso entre secciones del landing (mínimo **80 px** vertical) refuerza la jerarquía de contenido y facilita la lectura progresiva.

---

**Tono:**

El tono de comunicación de RiskGuard es técnico, directo y orientado a resultados. Se dirige a profesionales industriales —operarios, supervisores y gerencia— que necesitan información precisa y accionable. El lenguaje transmite autoridad y confianza técnica sin ser intimidante, y refuerza constantemente la idea de control y anticipación del riesgo.

---

**Lenguaje:**

El lenguaje será claro, conciso y orientado a la acción operativa. Se priorizarán mensajes breves que comuniquen valor inmediato. Por ejemplo, se usará **"Predice los riesgos antes de que ocurran"** en lugar de "Sistema de análisis predictivo de riesgos industriales", para generar impacto directo y reducir la carga cognitiva del usuario en entornos de alta presión.

---

### 4.1.2. Web Style Guidelines

**Estructura:**

La interfaz web de RiskGuard está diseñada con un enfoque *responsive*, garantizando adaptación fluida entre desktop, laptop y tablet sin perder la identidad visual definida por la paleta institucional (`#0A0C0F`, `#FF5B00`, `#1A1E24`, `#00C97B`, `#FF3B30`).

- **Desktop:**
  Se emplea una grilla de 12 columnas con áreas de contenido centradas a un máximo de 1200 px. El navbar superior es fijo e incluye a la izquierda el logotipo y a la derecha los links de navegación principales: Características, Metodología, Sectores, Estadísticas, y un botón CTA naranja destacado ("Contáctanos"). El hero ocupa el 100% del viewport con layout de dos columnas: copy izquierdo y widget de panel de seguridad a la derecha. Las secciones de features usan grillas de 3 columnas para las cards.

- **Tablet:**
  La grilla se ajusta a 2 columnas. El navbar se condensa y los botones incrementan su área táctil mínima a 44 px para facilitar interacción. Las grillas de 3 columnas se colapsan a 2 columnas.

- **Móvil (versión web):**
  La estructura se simplifica a una sola columna. Los elementos se apilan verticalmente con separación consistente. El navbar se convierte en menú tipo hamburguesa. El hero muestra el copy en full-width y el widget de panel se oculta o se muestra colapsado debajo del CTA.

**Componentes básicos de UI:**

- **Botones:**
  Primarios con fondo naranja `#FF5B00` y texto blanco, border-radius de 6 px, sin sombra. Estados: normal (naranja pleno), hover (naranja claro `#FF7A2F` con ligera escala 1.02), activo (reducción de escala 0.98), deshabilitado (gris `#2A2F38` con texto `#8A8F9A`).
  Secundarios con fondo transparente, borde naranja `#FF5B00` y texto naranja.

- **Formularios:**
  Inputs minimalistas con fondo `#1A1E24`, borde `#2A2F38` y texto blanco. Enfocado: borde naranja `#FF5B00`. Error: borde rojo `#FF3B30`. Placeholder en gris `#8A8F9A`.

- **Feature Cards:**
  Diseño rectangular con border-radius de 12 px, fondo `#1A1E24` y borde sutil `#2A2F38` de 0.5 px. Estructura interna: badge de categoría (tag uppercase de color), ícono pequeño, título en blanco y descripción en gris. Hover: borde naranja tenue.

- **Dashboard Widget (Hero):**
  Card oscura `#111418` con tabla de niveles de alerta, badges de estado (verde/rojo/naranja), y porcentaje de cobertura destacado en verde `#00C97B`. Simula una vista real del panel de control del producto.

- **Stats / Métricas:**
  Número destacado en naranja `#FF5B00` o verde `#00C97B` a 48–64 px bold, con label descriptivo en gris debajo a 13 px.

- **Navbar links:**
  Texto en gris `#8A8F9A`, sin subrayado por defecto. Hover: texto blanco `#FFFFFF`. El link activo muestra texto blanco.

**Tipografía en Web:**

- Títulos display (Hero H1): 48–72 px, Bold, blanco + naranja en mismo bloque.
- Títulos de sección (H2): 28–32 px, SemiBold, color `#FFFFFF`.
- Subtítulos de card (H3): 16–18 px, Medium, color `#FFFFFF`.
- Texto de párrafo / descripción: 13–15 px, Regular, color `#8A8F9A`.
- Botones: 14–16 px, SemiBold, blanco sobre naranja.
- Tags / Badges: 10–11 px, Regular Uppercase, con color según categoría.

**Interacción:**

- **Hover:** Botones primarios aclaran su fondo a `#FF7A2F`. Cards muestran borde naranja tenue. Links de nav cambian a blanco.
- **Clic:** Botones aplican escala `0.98` con transición de 100 ms confirmando la acción.
- **Scroll:** Navbar fijo para navegación rápida en todo momento.
- **Feedback:** Estados activos resaltados con cambio de borde o intensidad de color. Sin uso de sombras decorativas.

 <div align="center">
  <p>
    <b>Grafico 13</b>: Web Styles Guidlines - RiskGuard
  </p>
    
![Foto](images/Exhibición.png)
  
  <p>
    <i><b>Fuente</b>: Elaboración propia en Figma </i>
  </p>
</div>

---

## 4.2. Information Architecture

La arquitectura de información de RiskGuard está organizada para que operarios, supervisores y gerencia puedan acceder, monitorear y gestionar alertas de seguridad industrial de forma rápida y consistente en web y móvil. La estructura se apoya en cuatro sistemas: Organization, Labeling, Searching y Navigation.

### 4.2.1. Organization Systems

**Aplicación Web / Dashboard:**

La organización visual del dashboard está diseñada para guiar al usuario a través de un flujo de monitoreo claro y ordenado según su rol:

- **Pantalla de Inicio / Login:**
  Los usuarios acceden con credenciales de empresa. Se diferencia entre:
  - _Operario:_ Acceso al módulo de reporte de incidencias y visualización de protocolos asignados.
  - _Supervisor:_ Acceso al panel de monitoreo de zonas, gestión de alertas y reportes de equipo.
  - _RRHH / Gerencia:_ Acceso al panel ejecutivo con métricas consolidadas, reportes PERC y análisis de tendencias.

- **Panel principal (post-login):**
  Una vez autenticado, el usuario accede al dashboard principal con las siguientes secciones:
  - _Panel de Seguridad:_ Vista en tiempo real del estado de zonas, alertas activas y nivel de cobertura.
  - _Alertas Multi-Canal:_ Listado de alertas clasificadas por severidad y canal de origen (SMS, app, SMTP).
  - _Informes PERC:_ Acceso a informes generados automáticamente con análisis de cumplimiento ICC.
  - _Predicción de Tendencias:_ Módulo de IA que muestra patrones de riesgo detectados por algoritmos predictivos.
  - _Control por Zonas:_ Mapa digital de la planta con acceso segmentado por zona y nivel de riesgo.
  - _Protocolos LOTO Digital:_ Gestión de protocolos de bloqueo y etiquetado para mantenimiento seguro.

- **Menú lateral (sidebar):**
  Permite al usuario acceder a configuraciones y vistas adicionales:
  - Ver perfil y rol asignado.
  - Gestión de usuarios y permisos (solo Gerencia).
  - Configuración de notificaciones y canales de alerta.
  - Historial de incidencias y auditoría.

<div align="center">
  <img src="images/diagramaA.drawio.png" width="500"/>

  <p>
    <i><b>Fuente</b>: Elaboración propia en Draw.io</i>
  </p>
</div>

**Landing Page:**

La landing page sigue una estructura de bloques verticales con jerarquía visual clara orientada a la conversión:

- Hero: Propuesta de valor central + widget demo del panel de seguridad.
- Features: Grid de 6 features con cards de producto (Digitalización 337, Alertas Multi-Canal, Informes PERC, Predicción de Tendencias, Control por Zonas, Protocolos LOTO Digital).
- Sección "Diseñado para el piso industrial": 3 pasos del flujo operativo (Operarios reportan → Sistema analiza → Supervisores actúan).
- Stats: 4 métricas de impacto de la industria peruana.
- Soluciones por rol: 3 cards diferenciadas por perfil de usuario (Operarios, Supervisores, RRHH/Gerencia).
- CTA final: Llamada a la acción con dos botones (iniciar prueba / hablar con ventas).
- Footer: Links institucionales, contacto y créditos.

<div align="center">
  <img src="images/diagramaB.drawio.png" width="500"/>

  <p>
    <i><b>Fuente</b>: Elaboración propia en Draw.io</i>
  </p>
</div>

---

### 4.2.2. Labeling Systems

**Aplicación Web / Dashboard:**

El sistema de etiquetado está diseñado para ser inmediatamente comprensible en entornos de alta presión operativa:

- **Íconos con propósito:** Cada módulo del menú lateral y del panel principal está acompañado por un ícono representativo que facilita la identificación visual instantánea sin necesidad de leer el texto completo.
- **Etiquetas de nivel de alerta:** Badges de color codificado — Rojo (`CRÍTICO`), Naranja (`ADVERTENCIA`), Verde (`OPERATIVO`) — visibles en todas las vistas del panel para comunicar estado de riesgo de forma unívoca.
- **Etiquetas de rol:** Las vistas y módulos accesibles se etiquetan claramente según el rol del usuario (Operario, Supervisor, Gerencia) para evitar confusión en interfaces compartidas.
- **Coherencia visual:** Se mantiene un estilo uniforme de etiquetado en el menú lateral, las cards de alerta y la barra inferior de navegación móvil, reforzando una experiencia operativa consistente.

Etiquetas principales del sistema:

- _Barra de navegación:_ Panel, Alertas, Informes, Zonas, Configuración.
- _Botones de acción principal:_ "Reportar incidencia", "Ver protocolo", "Generar informe", "Escalar alerta".
- _Secciones del dashboard:_ "Alertas activas", "Cobertura de zona", "Tendencias de riesgo", "Protocolos pendientes".
- _Tags de features en landing:_ "NUEVO", "IA", "CRÍTICO", "MULTI-CANAL" en uppercase con color de acento según categoría.

### 4.2.3. SEO Tags and Meta Tags

En esta sección se definen los SEO Tags y Meta Tags implementados en RiskGuard, tanto en la Landing Page como en la Web Application. Estas etiquetas permiten mejorar la indexación en motores de búsqueda, optimizar la visibilidad del sitio y comunicar el contenido de cada página.

La Landing Page utiliza la directiva `index, follow` para permitir su posicionamiento en buscadores, mientras que la Web Application emplea `noindex, nofollow` para proteger información privada. En ambos casos se incluyen etiquetas esenciales como Title, Description, Keywords y Author.

**Implementación de Meta Tags**
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#FF5B00">

<title>RiskGuard — Plataforma de Seguridad Industrial Predictiva para Empresas del Perú</title>

<meta name="description" content="Plataforma que registra incidentes, analiza riesgos y genera alertas predictivas para prevenir accidentes laborales.">
<meta name="keywords" content="seguridad industrial Perú, riesgos laborales, alertas predictivas, SST digital">
<meta name="author" content="RiskGuard Solutions — UPC">
<meta name="robots" content="index, follow">

<link rel="canonical" href="https://ris-guard-lading.vercel.app/">

<meta property="og:title" content="RiskGuard — Seguridad Industrial Predictiva">
<meta property="og:description" content="Previene riesgos antes de que ocurran.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://ris-guard-lading.vercel.app/">
<meta property="og:image" content="https://ris-guard-lading.vercel.app/preview.png"> 
```

Estas etiquetas permiten que la página sea correctamente indexada, mejore su posicionamiento en motores de búsqueda y tenga una presentación adecuada al compartirse en redes sociales.

Por otro lado, en la Web Application las páginas son de acceso restringido, por lo que utilizan la directiva noindex, nofollow para evitar la indexación de contenido privado o sensible. Sin embargo, mantienen los elementos básicos como Title, Description, Keywords y Author para asegurar coherencia en la estructura del sistema.

### 4.2.4. Searching Systems

En RiskGuard, el sistema de búsqueda está diseñado para brindar acceso rápido y eficiente a incidencias, protocolos, zonas y reportes, evitando que el usuario pierda tiempo navegando en entornos de urgencia operativa.

**Dashboard Web:**

- **Barra de búsqueda global:** Ubicada en el header superior del dashboard, permite buscar incidencias por ID, zona, tipo de riesgo o fecha. Resultados aparecen en tiempo real con filtros rápidos aplicables.
- **Filtros contextuales por módulo:**
  - _Panel de Alertas:_ Filtros por severidad (Crítico / Advertencia / Operativo), zona, turno y fecha.
  - _Informes PERC:_ Filtros por período, área y tipo de cumplimiento.
  - _Control por Zonas:_ Selector visual de zona en mapa interactivo de planta.
  - _Historial de incidencias:_ Búsqueda por operario, tipo de evento y resultado del protocolo aplicado.
- **Menú lateral desplegable:** Acceso rápido a módulos principales sin necesidad de búsqueda: Panel de seguridad, Alertas Multi-Canal, Informes PERC, Predicción de Tendencias, Control por Zonas, Protocolos LOTO Digital, Gestión de usuarios (Gerencia).

**Aplicación Móvil:**

- **Barra de búsqueda superior:** Ícono de lupa en el header de la app. Al activarse, despliega un campo de texto y un teclado optimizado para ingreso rápido de términos operativos.
- **Menú hamburguesa:** Acceso a módulos secundarios: Ver perfil, Ajustes de notificaciones, Preferencias de zona asignada, Historial personal de reportes.
- **Filtros en listado de alertas:** Selector rápido por nivel de riesgo y turno actual, optimizado para uso con guantes industriales (áreas táctiles mínimas de 48 px).

### 4.2.5. Navigation Systems

RiskGuard ha sido diseñada como una plataforma de monitoreo industrial que ofrece una experiencia de navegación fluida, técnica y profesional. La plataforma transmite control y precisión a través de un diseño oscuro y minimalista donde predominan los colores negro profundo, naranja de acción y verde operativo, evitando excesos visuales y manteniendo una identidad moderna y de alta confiabilidad. La tipografía geométrica refuerza esta estética aportando legibilidad en condiciones de alta densidad informativa.

El sistema de navegación ha sido implementado tanto en la versión web (landing + dashboard) como en la aplicación móvil, asegurando coherencia visual y funcional en ambas plataformas.

**Desktop Landing Page y Dashboard Web:**

Menú de navegación principal:

En la versión web, el navbar se ubica en la parte superior de forma fija, alineado de izquierda a derecha, ofreciendo acceso directo a las secciones más relevantes:

- _Características:_ Descripción de los 6 módulos principales del producto.
- _Metodología:_ Explicación del enfoque técnico y de inteligencia artificial de RiskGuard.
- _Sectores:_ Industrias y tipos de plantas compatibles con el sistema.
- _Estadísticas:_ Datos de impacto y métricas de adopción en la industria peruana.
- _Contáctanos (CTA):_ Botón naranja destacado que lleva al formulario de contacto o inicio de prueba gratuita.

**Mobile Landing:**

La versión móvil de la landing condensa el navbar en un menú hamburguesa ubicado en la esquina superior derecha. Al desplegarse, muestra los mismos links principales en disposición vertical con separación generosa y área táctil amplia.

**Aplicación Móvil:**

Diseño general y menú inferior fijo:

La app móvil de RiskGuard prioriza la eficiencia y la claridad visual en entornos de uso industrial. La barra de navegación inferior fija contiene los tres módulos fundamentales de acceso constante:

- _Panel:_ Vista principal del estado de seguridad en tiempo real.
- _Alertas:_ Acceso inmediato al listado de alertas activas clasificadas por severidad.
- _Reportes:_ Módulo para crear, revisar y escalar incidencias registradas.

El menú hamburguesa en la esquina superior derecha agrupa acciones secundarias: ver perfil, configuración de notificaciones y preferencias de zona.

**Navegación y Acceso a Información:**

RiskGuard permite a operarios y supervisores monitorear el estado de seguridad industrial con el mínimo número de pasos posibles. Desde el panel principal, el usuario puede visualizar alertas activas, acceder a protocolos aplicables y generar reportes sin salir del flujo principal. La navegación entre secciones usa transiciones inmediatas sin animaciones innecesarias que puedan ralentizar la respuesta en contextos de urgencia.

**Interacción y Experiencia de Usuario:**

El diseño se centra en la claridad funcional y la velocidad de respuesta. Los íconos de línea fina, los colores de alto contraste y la jerarquía tipográfica bien definida permiten al usuario identificar información crítica de forma instantánea. Las acciones de alto impacto (escalar alerta, activar protocolo, generar informe) están accesibles en máximo dos toques desde cualquier punto de la aplicación.

**Conectividad y Actualización de Datos:**

La plataforma opera con datos actualizados en tiempo real, asegurando que los paneles de control reflejen el estado actual de cada zona de la planta. Los operarios reciben notificaciones automáticas multi-canal (app, SMS, SMTP) ante eventos críticos en sus zonas asignadas, fomentando la respuesta inmediata y el monitoreo continuo.

**Experiencia General:**

En conjunto, el sistema de navegación de RiskGuard equilibra funcionalidad operativa, accesibilidad en condiciones industriales y estética técnica profesional, asegurando que operarios, supervisores y gerencia puedan actuar con rapidez y precisión. Su diseño, tanto en web como en aplicación móvil, consolida una experiencia confiable, moderna y eficiente que refuerza el propósito central de la plataforma: predecir y prevenir riesgos industriales antes de que ocurran.

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
El Context Level Diagram del modelo C4 permite visualizar el sistema como una caja negra dentro de su entorno, mostrando los actores que interactúan con él y los sistemas externos con los que se integra. Este nivel de abstracción es fundamental para comprender el alcance del sistema, sus límites y las relaciones principales sin entrar en detalles técnicos internos.

En este caso, se presenta el sistema RiskGuard, una plataforma inteligente orientada a la prevención, monitoreo y mitigación de riesgos industriales en plantas productivas. El diagrama muestra cómo diferentes tipos de usuarios interactúan con el sistema, así como las integraciones necesarias para su correcto funcionamiento.

<img width="2378" height="2454" alt="Operarte" src="https://github.com/user-attachments/assets/b30a4f6e-94c9-42a5-9ae8-f8a6107dc074" />
￼
El sistema RiskGuard constituye el núcleo de la solución, representado centralmente en el diagrama.  A su alrededor se encuentran los diversos actores y sistemas externos con los que interactúa, estableciendo una red de relaciones que optimizan su funcionamiento.

**Usuarios del Sistema**

El sistema RiskGuard se adapta a las necesidades de cinco perfiles de usuario distintos, cada uno con funciones específicas dentro del flujo de trabajo. El Operario detecta y reporta incidencias, registrando condiciones inseguras y adjuntando evidencias fotográficas o de video. El Supervisor monitorea las zonas de trabajo, analiza alertas y gestiona acciones correctivas. RRHH/Gerencia utiliza el sistema para consultar KPIs, generar reportes ejecutivos y verificar el cumplimiento normativo. El Administrador gestiona usuarios, roles y permisos, asegurando el control de acceso y la confidencialidad. Finalmente, el Visitante accede únicamente a información pública, como la presentada en la landing page, sin interacción con datos internos.

**Sistemas Externos**

RiskGuard se integra con diversos sistemas externos para optimizar sus capacidades y funcionalidades.  Los sensores IoT proporcionan datos en tiempo real sobre las condiciones operativas de la planta, permitiendo un monitoreo continuo y la detección temprana de anomalías.  Un sistema de IA externo procesa estos datos mediante algoritmos de inteligencia artificial para la detección de patrones, la predicción de riesgos y el cálculo de indicadores clave como el Índice de Potencial de Riesgo de Accidentes (IPERC).  Además, un servicio de notificaciones garantiza la rápida difusión de alertas críticas a través de SMS, correo electrónico y notificaciones push.  Finalmente, el sistema se integra con SUNAFIL para facilitar la supervisión y el cumplimiento de las regulaciones laborales mediante el envío de reportes de cumplimiento normativo y auditorías.

**Relaciones Principales**

El sistema RiskGuard establece relaciones estratégicas con actores y sistemas externos para optimizar la gestión de riesgos y la seguridad operativa.  Los usuarios interactúan directamente con RiskGuard para la captura de información, monitoreo de riesgos y toma de decisiones informadas.  RiskGuard procesa datos en tiempo real de sensores IoT para generar alertas, que son enviadas a los usuarios mediante el servicio de notificaciones.  Además, el sistema envía información al sistema de inteligencia artificial para obtener análisis predictivos y recomendaciones estratégicas.  Finalmente, RiskGuard exporta reportes a sistemas regulatorios para el cumplimiento de normativas legales.

El diagrama de contexto permite identificar de manera clara los límites del sistema RiskGuard, los actores involucrados y las dependencias externas críticas. Este nivel de representación facilita la comprensión integral del sistema antes de profundizar en su arquitectura interna, la cual será desarrollada en los siguientes niveles del modelo C4.

---

### 4.6.3. Software Architecture Container Diagrams
El Container Level Diagram del modelo C4 describe la arquitectura interna de un sistema identificando sus principales contenedores, que representan aplicaciones o servicios independientes con responsabilidades específicas.  Este diagrama facilita la comprensión de la organización, distribución de funciones e interacción de componentes del sistema.  En RiskGuard, ilustra la estructura de la plataforma para el monitoreo, análisis y mitigación de riesgos industriales en tiempo real, asegurando una adecuada separación de responsabilidades y una arquitectura escalable.

<img width="7849" height="3392" alt="ContainerDiagram-dark copia" src="https://github.com/user-attachments/assets/90a55378-ff18-452c-ae89-83b796f87f53" />


**Descripción del Diagrama de Contenedores**

El sistema RiskGuard se organiza en capas para separar responsabilidades y facilitar la escalabilidad.

**Tipos de Usuarios**

* Operario: Reporta incidencias y registra condiciones inseguras.
* Supervisor: Monitorea zonas y gestiona acciones correctivas.
* RRHH / Gerencia: Consulta KPIs y reportes ejecutivos.
* Administrador: Gestiona usuarios y permisos.
* Visitante: Accede a información pública.

**Capa de Presentación (Frontend)**

* Web Application (React): Dashboard interactivo para monitoreo y alertas.
* Mobile Application (Flutter): Registro de incidencias y alertas en tiempo real.
* Comunicación: Servicios REST con el backend.

**Capa de Aplicación (Backend)**

* Backend API (Node.js): Núcleo del sistema, gestiona la lógica de negocio.

**Capa de Servicios Funcionales**

* Gestión de Incidentes: Registro de incidencias y evidencias.
* Monitoreo de Zonas: Visualización del estado de las áreas.
* Motor de Riesgo (IPERC): Análisis de riesgo (probabilidad, severidad, criticidad).
* Gestión de Mitigación: Acciones correctivas y control de riesgos.
* Reportes y KPIs: Indicadores y reportes para la toma de decisiones.
* Servicio de Notificaciones: Envío de alertas.

**Capa de Datos**

* Base de Datos (MongoDB): Almacenamiento y consulta eficiente de información.

**Sistemas Externos**

* Sensores IoT: Datos en tiempo real sobre condiciones operativas.
* Sistema de IA externo: Análisis predictivo y detección de patrones.
* Sistema regulatorio (SUNAFIL): Recibe reportes de cumplimiento normativo.

**Comunicación entre Contenedores**

* Usuarios interactúan con frontend.
* Frontend envía solicitudes al backend API.
* Backend distribuye solicitudes a servicios funcionales.
* Servicios acceden a la base de datos.
* Motor de Riesgo se integra con IA.
* Sensores IoT envían datos al backend.
* Servicio de notificaciones comunica alertas.
* Sistema exporta información a plataformas regulatorias.

**Decisiones de Arquitectura y Tecnología**

* Arquitectura modular basada en contenedores: Separación de responsabilidades y escalabilidad.
* Node.js: Manejo eficiente de solicitudes concurrentes.
* React y Flutter: Interfaces modernas y adaptadas a dispositivos.
* MongoDB: Flexibilidad en manejo de datos.
* Integración con sistemas externos: Análisis predictivo y monitoreo en tiempo real.

**Elementos de alto nivel de la arquitectura**

La arquitectura de RiskGuard se compone de los siguientes elementos principales:

* Capa de Presentación (Frontend):  Incluye la aplicación web y móvil para la interacción directa con los usuarios.
* Backend API:  Núcleo del sistema, centraliza la lógica de negocio y coordina la comunicación entre componentes.
* Servicios Funcionales:  Módulos especializados que implementan funcionalidades clave como gestión de incidencias, monitoreo, análisis de riesgo, mitigación, reportes y notificaciones.
* Base de Datos (MongoDB):  Persiste la información del sistema, incluyendo usuarios, incidencias, reportes y configuraciones.
* Sistemas Externos:  Componentes externos como sensores IoT, IA y plataformas regulatorias que complementan el sistema.


El diagrama de contenedores de RiskGuard presenta una arquitectura modular y escalable, con componentes específicos para cada función. La distribución de responsabilidades y la integración con sistemas externos garantizan un funcionamiento eficiente en entornos industriales.



### 4.6.4. Software Architecture Components Diagrams
En esta sección se presentan los diagramas de componentes del sistema RiskGuard, los cuales muestran la descomposición interna de cada contenedor, identificando sus principales bloques funcionales, responsabilidades y tecnologías. Esto permite entender cómo se implementa la lógica del sistema y cómo interactúan sus partes internas.

<img width="5610" height="4458" alt="ComponentDiagramFinal-dark copia 2" src="https://github.com/user-attachments/assets/e3209216-6f29-45c7-9d70-4209d1ddfffa" />

**Backend API**
El Backend API (Node.js + Express) centraliza la lógica del sistema.
Componentes principales:
* API Controllers: gestionan las solicitudes del frontend.
* Auth Component (JWT): controla autenticación y permisos.
* Incident Service: gestiona incidencias.
* Monitoring Service: monitorea zonas.
* Risk Service: analiza riesgos.
* Mitigation Service: gestiona acciones correctivas.
* Reporting Service: genera reportes y KPIs.
* Notification Service: envía alertas.
* Repository Layer (MongoDB): maneja la persistencia de datos.
Interacción: Los controladores reciben solicitudes, los servicios procesan la lógica y el repositorio gestiona el acceso a la base de datos.

**Web Application**
La Web App (React) permite el monitoreo y gestión del sistema.
Componentes:
* UI Components: estructura visual.
* Dashboard: muestra métricas y estado general.
* Alert Module: gestiona alertas.
* Reports Module: consulta reportes.
* API Client: comunica con el backend.

**Mobile Application**
La Mobile App (Flutter) permite el registro de incidencias en campo.
Componentes:
* Mobile UI: interfaz principal.
* Form Handler: registro de incidencias.
* Media Component: captura de evidencia.
* API Client: comunicación con backend.

**Motor de Riesgo**

El Motor de Riesgo (Python) realiza el análisis avanzado.
Componentes:
* Risk Calculator: calcula niveles de riesgo.
* IPERC Processor: evalúa riesgos.
* Pattern Detection: detecta patrones.

Los diagramas de componentes muestran la estructura interna del sistema, permitiendo entender cómo se distribuyen las responsabilidades y cómo interactúan los módulos para garantizar el funcionamiento de RiskGuard.


## 4.7. Software Object-Oriented Design

### 4.7.1. Class Diagrams

<p align="center">Usuario y Autenticación de Cuenta BC</p>
<p align="center"><img src="images/bc/dia_bc1.png" width="500"/></p>

<p align="center">Sede / Área y Activo industrial BC</p>
<p align="center"><img src="images/bc/dia_bc2.png" width="500"/></p>

<p align="center">Inspección / Condición Insegura BC</p>
<p align="center"><img src="images/bc/dia_bc3.png" width="500"/></p>

<p align="center">Evaluación de Riesgo BC</p>
<p align="center"><img src="images/bc/dia_bc4.png" width="500"/></p>

<p align="center">Mitigación BC</p>
<p align="center"><img src="images/bc/dia_bc5.png" width="500"/></p>

<p align="center">Monitoreo y Dashboard BC</p>
<p align="center"><img src="images/bc/dia_bc6.png" width="500"/></p>

<p align="center">Reportes y Cumplimiento BC</p>
<p align="center"><img src="images/bc/dia_bc7.png" width="500"/></p>


## 4.8. Database Design

### 4.8.1. Database Diagrams
