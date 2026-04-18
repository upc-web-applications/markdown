
# Capítulo IV: Product Design


## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines

**Logo:**

El logo de RiskGuard combina robustez visual y autoridad técnica a través de un diseño que evoca un escudo de protección integrado con elementos industriales. La tipografía fuerte y geométrica transmite precisión y control, mientras que el uso del color naranja sobre fondo oscuro genera un contraste inmediato que comunica alerta y acción. La disposición compacta del logotipo junto al nombre asegura reconocimiento rápido en entornos de alta densidad informativa como dashboards industriales.

///

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

///

---

### 4.1.3. Mobile Style Guidelines

**Estructura general:**

La app sigue principios de Material Design (Android) e Human Interface Guidelines (iOS) para mantener consistencia y usabilidad en cada plataforma:

- **iOS:**
  Paleta oscura con fondos predominantemente `#0A0C0F` y `#111418`. El header superior incluye logo y acceso al perfil con separación visual respecto al contenido mediante un borde sutil. La barra inferior contiene 4 ítems de navegación (Panel, Alertas, Reportes, Ajustes), cada uno con ícono y label. El texto sigue jerarquía: 20 px títulos, 16 px subtítulos, 14 px texto simple.

- **Android:**
  El header mantiene logo y acceso al usuario en la parte superior. La navegación principal se ubica como pestañas superiores siguiendo el estándar Material Design. Los botones de acción rápida se posicionan ligeramente más abajo que en iOS.

**Componentes básicos en Mobile:**

- **Botones:**
  Primarios en naranja `#FF5B00` con texto blanco, esquinas redondeadas de 8 px. Secundarios en fondo transparente con borde naranja.

- **Inputs:**
  Minimalistas con línea inferior naranja `#FF5B00` en Android y borde suave `#2A2F38` en iOS. Texto en blanco sobre fondo `#1A1E24`.

- **Cards de alerta / incidencia:**
  Fondo `#1A1E24`, badge de nivel de riesgo (rojo/naranja/verde), descripción del evento y timestamp. Divisores en `#2A2F38`.

- **Panel de métricas:**
  Valores numéricos grandes en naranja o verde, label descriptivo en gris, agrupados en grilla de 2 columnas.

**Tipografía en Mobile:**

- Títulos (H1): 20 px SemiBold, color `#FFFFFF`.
- Subtítulos (H2/H3): 16 px Regular, color `#FFFFFF`.
- Texto simple / descripción: 14 px Regular, color `#8A8F9A`.
- Botones: 14 px SemiBold, blanco sobre fondo naranja.
- Tags / Badges: 10 px Uppercase, color según nivel de alerta.

#### 4.1.3.1. iOS Mobile Style Guidelines

La versión iOS de RiskGuard prioriza la claridad y la velocidad de lectura en condiciones de uso industrial. Los elementos de la interfaz se presentan sobre fondos oscuros profundos con acentos naranjas precisos que guían la atención del operario hacia las alertas críticas. La barra inferior fija garantiza acceso constante a las cuatro funciones principales sin interrumpir el flujo de monitoreo.

///

#### 4.1.3.2. Android Mobile Style Guidelines

La versión Android de RiskGuard adopta los patrones de navegación de Material Design, con pestañas superiores y un FAB (botón de acción flotante) naranja para reportes de incidencias rápidas. La barra de navegación inferior se reemplaza por las pestañas superiores estándar de Material You, manteniendo la paleta oscura y los acentos naranjas de la identidad de marca.

///

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

  ///foto

**Landing Page:**

La landing page sigue una estructura de bloques verticales con jerarquía visual clara orientada a la conversión:

- Hero: Propuesta de valor central + widget demo del panel de seguridad.
- Features: Grid de 6 features con cards de producto (Digitalización 337, Alertas Multi-Canal, Informes PERC, Predicción de Tendencias, Control por Zonas, Protocolos LOTO Digital).
- Sección "Diseñado para el piso industrial": 3 pasos del flujo operativo (Operarios reportan → Sistema analiza → Supervisores actúan).
- Stats: 4 métricas de impacto de la industria peruana.
- Soluciones por rol: 3 cards diferenciadas por perfil de usuario (Operarios, Supervisores, RRHH/Gerencia).
- CTA final: Llamada a la acción con dos botones (iniciar prueba / hablar con ventas).
- Footer: Links institucionales, contacto y créditos.

///foto

---

### 4.2.2. Labeling Systems

**Aplicación Web / Dashboard:**

El sistema de etiquetado está diseñado para ser inmediatamente comprensible en entornos de alta presión operativa:

- **Íconos con propósito:** Cada módulo del menú lateral y del panel principal está acompañado por un ícono representativo que facilita la identificación visual instantánea sin necesidad de leer el texto completo.
- **Etiquetas de nivel de alerta:** Badges de color codificado — Rojo (`CRÍTICO`), Naranja (`ADVERTENCIA`), Verde (`OPERATIVO`) — visibles en todas las vistas del panel para comunicar estado de riesgo de forma unívoca.
- **Etiquetas de rol:** Las vistas y módulos accesibles se etiquetan claramente según el rol del usuario (Operario, Supervisor, Gerencia) para evitar confusión en interfaces compartidas.
- **Coherencia visual:** Se mantiene un estilo uniforme de etiquetado en el menú lateral, las cards de alerta y la barra inferior de navegación móvil, reforzando una experiencia operativa consistente.

///foto

Etiquetas principales del sistema:

- _Barra de navegación:_ Panel, Alertas, Informes, Zonas, Configuración.
- _Botones de acción principal:_ "Reportar incidencia", "Ver protocolo", "Generar informe", "Escalar alerta".
- _Secciones del dashboard:_ "Alertas activas", "Cobertura de zona", "Tendencias de riesgo", "Protocolos pendientes".
- _Tags de features en landing:_ "NUEVO", "IA", "CRÍTICO", "MULTI-CANAL" en uppercase con color de acento según categoría.

///foto

---

### 4.2.3. Searching Systems

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

///foto
---

### 4.2.4. Navigation Systems

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


///foto

**Mobile Landing:**

La versión móvil de la landing condensa el navbar en un menú hamburguesa ubicado en la esquina superior derecha. Al desplegarse, muestra los mismos links principales en disposición vertical con separación generosa y área táctil amplia.

**Aplicación Móvil:**

Diseño general y menú inferior fijo:

La app móvil de RiskGuard prioriza la eficiencia y la claridad visual en entornos de uso industrial. La barra de navegación inferior fija contiene los tres módulos fundamentales de acceso constante:

- _Panel:_ Vista principal del estado de seguridad en tiempo real.
- _Alertas:_ Acceso inmediato al listado de alertas activas clasificadas por severidad.
- _Reportes:_ Módulo para crear, revisar y escalar incidencias registradas.

El menú hamburguesa en la esquina superior derecha agrupa acciones secundarias: ver perfil, configuración de notificaciones y preferencias de zona.

///foto

**Navegación y Acceso a Información:**

RiskGuard permite a operarios y supervisores monitorear el estado de seguridad industrial con el mínimo número de pasos posibles. Desde el panel principal, el usuario puede visualizar alertas activas, acceder a protocolos aplicables y generar reportes sin salir del flujo principal. La navegación entre secciones usa transiciones inmediatas sin animaciones innecesarias que puedan ralentizar la respuesta en contextos de urgencia.

**Interacción y Experiencia de Usuario:**

El diseño se centra en la claridad funcional y la velocidad de respuesta. Los íconos de línea fina, los colores de alto contraste y la jerarquía tipográfica bien definida permiten al usuario identificar información crítica de forma instantánea. Las acciones de alto impacto (escalar alerta, activar protocolo, generar informe) están accesibles en máximo dos toques desde cualquier punto de la aplicación.

**Conectividad y Actualización de Datos:**

La plataforma opera con datos actualizados en tiempo real, asegurando que los paneles de control reflejen el estado actual de cada zona de la planta. Los operarios reciben notificaciones automáticas multi-canal (app, SMS, SMTP) ante eventos críticos en sus zonas asignadas, fomentando la respuesta inmediata y el monitoreo continuo.

**Experiencia General:**

En conjunto, el sistema de navegación de RiskGuard equilibra funcionalidad operativa, accesibilidad en condiciones industriales y estética técnica profesional, asegurando que operarios, supervisores y gerencia puedan actuar con rapidez y precisión. Su diseño, tanto en web como en aplicación móvil, consolida una experiencia confiable, moderna y eficiente que refuerza el propósito central de la plataforma: predecir y prevenir riesgos industriales antes de que ocurran.

///foto



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
