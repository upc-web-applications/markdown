# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción del startup

RiskGuard Solutions es una iniciativa concebida por estudiantes de Ingeniería de Sistemas de Software, cuyo objetivo primordial es la aplicación de la tecnología para la optimización de la seguridad en entornos industriales.  Nuestro proyecto, RiskGuard, surge de la imperiosa necesidad de mitigar los riesgos laborales en fábricas, donde una cantidad considerable de incidentes y casi-accidentes no son debidamente registrados ni analizados.

La propuesta se materializa en una aplicación web diseñada para facilitar el registro y procesamiento de información de seguridad ingresada por operarios, supervisores y personal de recursos humanos.  A partir del análisis exhaustivo de estos datos, el sistema genera alertas y visualizaciones estratégicas que contribuyen a la identificación de riesgos potenciales y a la prevención de accidentes laborales.

RiskGuard Solutions se presenta como una solución práctica, accesible y de fácil uso, orientada a la mejora de la toma de decisiones y a la protección integral de la salud y el bienestar de los trabajadores.



**Misión:**

Nuestra misión consiste en desarrollar soluciones tecnológicas avanzadas que permitan a las empresas industriales gestionar y prevenir riesgos laborales de manera eficiente.  A través del uso estratégico de herramientas digitales, contribuimos a la protección integral de la salud de los trabajadores, priorizando su bienestar en el entorno laboral.


**Visión:**

Aspiramos a ser una startup reconocida a nivel nacional por brindar soluciones innovadoras y de alto impacto en el ámbito de la seguridad industrial.  Nuestro objetivo es destacarnos por nuestra capacidad para reducir significativamente los accidentes laborales y mejorar sustancialmente las condiciones de trabajo en las empresas.

**Valores:**

En nuestra empresa, la innovación constituye el motor fundamental para el progreso y la mejora continua de la seguridad en los entornos industriales.  Priorizamos la protección de la salud y el bienestar de los trabajadores, considerándolos el eje central de nuestras acciones.  Además, nos comprometemos a ofrecer soluciones accesibles, diseñadas para que cualquier usuario pueda utilizarlas sin dificultad.  La colaboración es la base sólida sobre la que construimos el trabajo en equipo, y la escalabilidad representa la clave para adaptarnos eficazmente a las necesidades cambiantes y dinámicas de las empresas.


**Características principales:**

La solución RiskGuard se caracteriza por su capacidad para registrar y centralizar incidentes y condiciones de riesgo mediante una plataforma web de acceso universal, diseñada para satisfacer las necesidades de diversos perfiles de usuario, incluyendo operarios, supervisores y personal administrativo.  A través de la integración de información proveniente de estas fuentes, el sistema realiza un análisis exhaustivo que facilita la identificación de patrones de riesgo y la generación de alertas preventivas, apoyando así la toma de decisiones estratégicas y oportunas.  Adicionalmente, RiskGuard incorpora visualizaciones avanzadas, tales como reportes detallados y dashboards interactivos, que optimizan la comprensión integral del estado de la seguridad organizacional.  La facilidad de uso intuitiva, la accesibilidad universal y la capacidad de adaptación a las necesidades específicas de las empresas consolidan a RiskGuard como una herramienta esencial para la gestión proactiva del riesgo.



### 1.1.2. Perfiles de integrantes del equipo

| Foto | Nombre | Descripción |
| -------- | -------- | -------- |
| ![](images/isabel-aponte.jpg) | Aponte Pablo, Isabel Luisa (u20241e158) | Soy estudiante de Ingeniería de Software con interés en la programación y el desarrollo de soluciones prácticas. Disfruto aprender cómo funcionan los sistemas por dentro y aplicar ese conocimiento en proyectos. Poseo conocimientos en C++, Java y HTML, además de otras herramientas tecnológicas. Me caracterizo por ser responsable, organizada y orientada al trabajo en equipo. |
| ![](images/carlos-blancas.jpg) | Blancas Chávez, Carlos Franco (u20241a322) |Me interesa mucho el desarrollo de software ya que desde siempre me ha interesado conocer cómo funcionan las cosas por dentro y esa curiosidad fue lo que me motivó a elegir esta profesión. Me gustaría desempeñarme en el área de bases de datos o desarrollador backend, porque me atrae la lógica que hay detrás de los sistemas y la forma en la que se organiza y gestiona la información. Habilidades: C++, Python, Js,React, Html, css, JavaScript, MySql|
| ![](images/angel-flores.jpg) | Flores Eusebio, Angel Thyago (u20231b781) | Soy estudiante de la carrera de ingenieria de Software. Disfruto mucho de aprender nuevas tecnologías como vue, javascript, c# y mas, para luego ponerlas en práctica creando códigos que puedan ayudarme o ayudar a alguien de mi entorno cercano. |
| ![](images/victor-laura.jpg) | Laura Acosta, Victor Jhosuef (u202418655) | Soy estudiante de Ingeniería de Software, con conocimientos en C++, C# y Java, y experiencia en Visual Studio Code y Visual Studio. Cuento con habilidades en diseño de bases de datos, elaborando modelos conceptuales y físicos. Me caracterizo por estar en constante aprendizaje y disposición para trabajar en equipo. |

## 1.2. Solution Profile

### 1.2.1. Antecedentes y problemática

En el Perú, la gestión de la Seguridad y Salud en el Trabajo (SST) todavía presenta dificultades para registrar, evaluar y atender oportunamente los riesgos laborales. Esta problemática es especialmente relevante en las actividades industriales, donde los trabajadores se encuentran expuestos a maquinaria, ruido, sustancias químicas, esfuerzos físicos y condiciones operativas cambiantes. Cuando los incidentes y condiciones inseguras se registran mediante papel, hojas de cálculo o comunicaciones informales, la información queda dispersa y se dificulta el seguimiento de las acciones correctivas.

Según el Ministerio de Trabajo y Promoción del Empleo (MTPE, 2025), en diciembre de 2024 se registraron 3 568 notificaciones relacionadas con la SST: 3 512 accidentes de trabajo no mortales, 19 accidentes mortales, 32 incidentes peligrosos y 5 enfermedades ocupacionales. Las industrias manufactureras concentraron el mayor porcentaje de notificaciones por actividad económica, con el 19,98 % del total. Asimismo, SUNAFIL informó que entre 2023 y 2024 realizó 2 818 inspecciones relacionadas con accidentes de trabajo, de las cuales 381 estuvieron vinculadas con accidentes mortales (SUNAFIL, 2024).

Estas cifras evidencian la necesidad de contar con mecanismos que conecten el reporte de un peligro con su evaluación, asignación, mitigación y cierre. Una gestión deficiente puede afectar la salud de los trabajadores, interrumpir las operaciones y reducir la productividad. Para comprender esta problemática de manera estructurada se aplica la técnica de las 5W+2H:

**What (¿Qué?)**

**¿Cuál es el problema?**

El problema central es la falta de un proceso integrado y trazable para registrar, evaluar, atender y monitorear los riesgos laborales. Muchas empresas recopilan datos de inspecciones, incidentes y condiciones inseguras mediante herramientas manuales o desconectadas que no permiten seguir el ciclo completo desde la identificación del peligro hasta el cierre de la acción de mitigación.

**¿Cuál es la relación con las personas afectadas?**

Los operarios son quienes detectan primero numerosos peligros dentro de la planta, pero necesitan un medio rápido para reportarlos y conocer su estado. Los supervisores deben evaluar la criticidad, asignar responsables y controlar plazos, aunque con frecuencia trabajan con información dispersa. Los gerentes necesitan indicadores consolidados para tomar decisiones y comprobar el desempeño de la gestión de SST, pero reciben reportes tardíos o incompletos.

**When (¿Cuándo?)**

**¿Cuándo sucede el problema?**

El problema se presenta durante toda la operación industrial: al ejecutar inspecciones, detectar actos o condiciones inseguras, reportar incidentes y casi-accidentes, evaluar riesgos, programar mantenimientos o verificar acciones correctivas. Se intensifica cuando existe alta carga operativa, cambios de turno, actividades de mantenimiento, ingreso de personal nuevo o necesidad de responder rápidamente ante un riesgo crítico.

**Where (¿Dónde?)**

**¿Dónde surge el problema?**

Surge principalmente en plantas industriales, sedes operativas, áreas de producción, almacenes, talleres y zonas de mantenimiento donde existen peligros asociados con personas, procesos y activos. También continúa en las oficinas de seguridad y administración, donde los datos deben consolidarse para elaborar indicadores, reportes y evidencias de cumplimiento.

**¿Dónde se encuentra el usuario cuando necesita la solución?**

El operario puede encontrarse en la planta mientras realiza sus labores y dispone de poco tiempo para completar un reporte. El supervisor puede estar recorriendo diferentes áreas o gestionando casos desde una computadora. El gerente consulta información resumida desde un entorno administrativo. Por ello, la solución debe ser web, responsive y comprensible desde distintos dispositivos.

**Who (¿Quién?)**

**¿Quiénes están involucrados?**

Los principales involucrados son los operarios de planta, los supervisores de seguridad y mantenimiento, los técnicos responsables de acciones correctivas y los gerentes o administradores de empresas industriales. De manera indirecta también participan las áreas de recursos humanos, cumplimiento y dirección, que requieren evidencia confiable sobre la gestión de SST.

**¿A quiénes les sucede el problema?**

El problema afecta principalmente a organizaciones que aún dependen de registros manuales, hojas de cálculo, mensajes o sistemas aislados. Dentro de ellas, afecta a los trabajadores expuestos a peligros, a los supervisores responsables de prevenir accidentes y a los directivos que necesitan controlar el desempeño y el cumplimiento de la organización.

**Why (¿Por qué?)**

**¿Cuáles son las causas del problema?**

Entre las principales causas se encuentran la dependencia de procesos manuales, la fragmentación de la información entre diferentes áreas, la ausencia de un flujo común para gestionar hallazgos y mitigaciones, la limitada trazabilidad de responsables y plazos, y la demora en transformar los registros operativos en indicadores útiles. También influyen el poco tiempo disponible para reportar, la falta de retroalimentación al operario y el uso de herramientas que no están adaptadas a los roles y necesidades de una operación industrial.

**How (¿Cómo?)**

**¿Cómo se gestiona actualmente la situación?**

Los hallazgos suelen registrarse mediante formatos físicos, archivos de Excel, llamadas, mensajes o aplicaciones independientes. Posteriormente, un responsable debe consolidar manualmente la información, evaluar el nivel de riesgo, coordinar la atención y preparar reportes. Este proceso incrementa la posibilidad de duplicidad, omisiones, errores y pérdida de seguimiento.

**¿Cómo prefieren los usuarios acceder a la información?**

Los operarios requieren formularios breves y claros que puedan completar desde un teléfono, tablet o computadora y que confirmen inmediatamente el registro. Los supervisores necesitan una bandeja priorizada con niveles de criticidad, responsables, plazos y estados. Los gerentes requieren dashboards, tendencias, mapas de calor e informes exportables que resuman la situación de la organización.

**How much (¿Cuánto?)**

**¿Cuál es la magnitud del problema?**

El estudio de Aquino Canchari et al. (2022) registró 37 899 casos de enfermedades ocupacionales en el sector minero peruano entre 2011 y 2020. De ese total, el 90,74 % correspondió a hipoacusia y el 4,94 % a neumoconiosis. Si bien estas cifras pertenecen al sector minero, evidencian la magnitud que puede alcanzar la exposición prolongada a peligros físicos y ambientales cuando la prevención y el monitoreo resultan insuficientes.

**¿Qué impacto genera en las organizaciones?**

El impacto no se limita al número de accidentes o enfermedades. También comprende horas de trabajo perdidas, ausentismo, retrasos operativos, acciones correctivas vencidas, posibles sanciones y tiempo administrativo destinado a consolidar información. Vargas y Gutiérrez (2021) sostienen que una inversión adecuada en SST puede reducir accidentes, sanciones, estrés y ausentismo, además de favorecer la productividad y la eficiencia.

**Figura 1**

*Notificaciones de accidentes de trabajo según actividad económica, diciembre de 2024.*

[![Captura-de-pantalla-2026-07-08-144253.png](https://i.postimg.cc/MGRyhQfH/Captura-de-pantalla-2026-07-08-144253.png)](https://postimg.cc/kVJ6SDcP)

*Nota.* Adaptado del *Boletín Estadístico Mensual de Notificaciones de Accidentes de Trabajo, Incidentes Peligrosos y Enfermedades Ocupacionales*, por el Ministerio de Trabajo y Promoción del Empleo (2025).


### 1.2.2. Lean UX Process

En esta sección aplicamos el Lean UX Process con el propósito de comprender la problemática relacionada con la gestión de riesgos laborales y orientar el desarrollo de RiskGuard hacia las necesidades reales de sus usuarios. Para ello, presentamos el Lean UX Problem Statement, las Assumptions, los Hypothesis Statements y el Lean UX Canvas. Estos artefactos permiten identificar los principales problemas de operarios, supervisores y gerentes, establecer las suposiciones iniciales del equipo, formular hipótesis medibles y definir las funcionalidades necesarias para validar la propuesta de valor de la solución.

#### 1.2.2.1. Lean UX Problem Statements

El proyecto RiskGuard propone una aplicación web para fortalecer la Seguridad y Salud en el Trabajo en empresas industriales peruanas. Mediante una experiencia accesible y diferenciada por roles, la plataforma permite que los operarios registren incidentes, casi-accidentes y condiciones inseguras; que los supervisores evalúen riesgos mediante criterios IPERC, asignen responsables y gestionen acciones de mitigación; y que los gerentes consulten indicadores, tendencias y reportes para tomar decisiones. Su objetivo es integrar en un solo entorno digital el registro, la evaluación, la atención y el monitoreo de los riesgos laborales, mejorando la prevención y la trazabilidad de las acciones correctivas.

Dentro de las empresas industriales, se busca que la identificación de un peligro produzca una respuesta oportuna y verificable antes de que la situación derive en un accidente. No obstante, observamos que una parte importante de las inspecciones, incidentes y condiciones inseguras todavía se registra mediante papel, hojas de cálculo o canales informales. Estos medios no ofrecen un proceso continuo que conecte el hallazgo con su evaluación, la asignación de un responsable, la ejecución de una medida de mitigación y la comprobación de su cierre. Esto se refleja en información dispersa, subregistro de eventos, dificultades para priorizar riesgos críticos, acciones correctivas fuera de plazo y poca visibilidad gerencial sobre el estado real de la seguridad en la organización.

Aunque actualmente existen formularios digitales, sistemas documentales y herramientas generales para registrar incidencias, identificamos que la integración entre la operación en planta, la gestión del supervisor y el análisis gerencial continúa siendo limitada. Ahí radica la oportunidad que RiskGuard desea aprovechar: intervenir en la brecha existente entre la detección de una condición insegura y su atención efectiva, centralizando sedes, áreas, activos, inspecciones, evaluaciones IPERC, mitigaciones, tickets, técnicos, dashboards y reportes. La solución se dirige inicialmente a empresas de manufactura y operaciones de planta que dependen de procesos manuales o herramientas fragmentadas, considerando restricciones como la disponibilidad de tiempo de los operarios, la conectividad en determinadas zonas, el acceso desde distintos dispositivos, la calidad de los datos registrados y la necesidad de proteger la información según el rol del usuario.

**¿Cómo podríamos conectar el reporte, la evaluación, la mitigación y el monitoreo de los riesgos laborales para que operarios, supervisores y gerentes actúen de manera coordinada y oportuna, aun cuando existen limitaciones de tiempo, conectividad y acceso a dispositivos dentro de las operaciones industriales?**

#### 1.2.2.2. Lean UX Assumptions

#### Features

- Interfaz gráfica para el registro rápido de incidentes, permitiendo adjuntar evidencia fotográfica de condiciones inseguras en tiempo real.
- Algoritmos que aplican modelos matemáticos de riesgo para categorizar la urgencia de cada hallazgo.
- Panel visual con mapas de calor y gráficas de tendencia que se actualizan sin necesidad de recargar la página, facilitando el monitoreo continuo de la planta.
- Funcionalidad para exportar documentos de auditoría que cumplan con los formatos referenciales de la ley peruana.

#### Needings

- Las empresas presentan una deficiencia en la capacidad de prevención de riesgos, causada por el uso de métodos de registro que no permiten un análisis estadístico oportuno.
- Los Usuarios necesitan superar esta deficiencia aprendiendo a identificar y registrar peligros de manera digital, confiando en que el sistema procesará esa información para alertar sobre riesgos inminentes.
- Empresas de manufactura y logística están interesados en optimizar sus sistemas de gestión de la seguridad con el fin de reducir la tasa de accidentes.
- Los administradores desean ver una gráfica de tendencia en base a los datos de ingresados.
- Corregir la brecha entre el hallazgo de un peligro y su mitigación mediante una plataforma accesible y predictiva que prepare a la organización para actuar ante situaciones críticas antes de que ocurran accidentes.
- La falta de veracidad en el llenado de datos por parte del personal operativo, lo cual se abordará con interfaces simplificadas y validaciones automáticas de integridad en el frontend.
- Sistemas de gestión documental genéricos o formularios en Excel, que carecen de la capacidad reactiva y del motor predictivo propuesto en ....

#### 1.2.2.3. Lean UX Hypothesis Statements

**Creemos** que digitalizar el proceso de inspección mediante la aplicación web RiskGuard evolucionará la captura de datos en planta. 
**Sabremos** que lo propuesto es cierto 
**Cuando** los reportes diarios se incrementen en un 40% debido a la facilidad de uso frente al registro en hojas de cálculos o papel

**Creemos** que integrar un motor de reglas en la aplicación web permitirá predecir accidentes antes de que ocurran. 
**Sabremos** que lo propuesto es cierto
**Cuando** el sistema identifique correctamente al menos el 70% de las áreas de alta criticidad antes de que se registre un siniestro real

**Creemos** que ofrecer Dashboards visuales con indicadores predictivos potenciará la toma de decisiones gerenciales
**Sabremos** que lo propuesto es cierto 
**Cuando** se reporte una reducción del 50% en el tiempo dedicado a elaborar informes mensuales de gestión.

**Creemos** que ofrecer una plataforma ligera y accesible desde navegadores web permitirá la adopción de RiskGuard en empresas con baja infraestructura tecnológica. 
**Sabremos** que esto es cierto 
**Cuando** logremos mantener una tasa de disponibilidad del sistema superior al 70% sin requerir hardware especializado del lado del cliente.

#### 1.2.2.4. Lean UX Canvas

<table>
  <tr>
    <th>Business Problem</th>
    <th>Solutions</th>
    <th>Business Outcomes</th>
  </tr>
  <tr>
    <td>
      Las empresas de manufactura y logística presentan una brecha crítica en la prevención de riesgos laborales debido al uso de registros manuales, hojas de cálculo y reportes tardíos. Esta situación afecta a los operarios, quienes no reportan incidentes por falta de tiempo o retroalimentación; a los supervisores, quienes no cuentan con datos centralizados para priorizar riesgos; y a los gerentes, quienes reciben información incompleta o tardía para tomar decisiones preventivas y cumplir con la Ley N.° 29783.
    </td>
    <td>
      <ul>
        <li>Formulario móvil/web para registrar casi-accidentes y condiciones inseguras con evidencia fotográfica.</li>
        <li>Backend que clasifica la criticidad del riesgo mediante reglas de probabilidad, severidad y recurrencia.</li>
        <li>Dashboard operativo con mapa de calor, alertas activas y patrones recurrentes.</li>
        <li>Gestión de tickets y acciones correctivas.</li>
        <li>Dashboard ejecutivo y reportes exportables para cumplimiento normativo.</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Reducción del subregistro de incidentes.</li>
        <li>Disminución del tiempo de respuesta ante riesgos críticos.</li>
        <li>Mejora en la trazabilidad de acciones correctivas.</li>
        <li>Apoyo al cumplimiento de la Ley N.° 29783.</li>
        <li>Reducción progresiva de condiciones inseguras no atendidas.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Users</th>
    <th>Hypotheses</th>
    <th>User Outcomes & Benefits</th>
  </tr>
  <tr>
    <td>
      <ul>
        <li>Operarios de planta</li>
        <li>Supervisores de seguridad y mantenimiento</li>
        <li>Gerentes y administradores</li>
      </ul>
    </td>
    <td>
      Creemos que digitalizar el reporte de incidentes mediante RiskGuard incrementará la cantidad de reportes registrados por los operarios, porque el proceso será más rápido, simple y trazable que el uso de papel o Excel. Sabremos que esto es cierto cuando los usuarios puedan completar un reporte en menos de 30 segundos y los supervisores visualicen automáticamente el riesgo en el dashboard.
    </td>
    <td>
      <ul>
        <li><strong>Operarios:</strong> reportan riesgos en pocos pasos y reciben confirmación.</li>
        <li><strong>Supervisores:</strong> centralizan reportes, priorizan zonas críticas y asignan acciones correctivas.</li>
        <li><strong>Gerentes:</strong> consultan indicadores predictivos y exportan reportes para auditorías y toma de decisiones.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th colspan="2">What’s the most important thing we need to learn first?</th>
    <th>What’s the least amount of work we need to do to learn the next most important thing?</th>
  </tr>
  <tr>
    <td colspan="2">
      ¿Los operarios, supervisores y gerentes consideran útil una plataforma web que permita registrar incidentes, visualizar riesgos por sector y recibir alertas de criticidad para mejorar la prevención de accidentes laborales?
    </td>
    <td>
      Desarrollar un MVP funcional con autenticación por roles, formulario de reporte de incidentes, registro de sectores y activos, dashboard con mapa de calor simulado, alertas de criticidad y reportes básicos usando una fake API basada en json-server y db.json.
    </td>
  </tr>
</table>


## 1.3. Segmentos objetivo
Los segmentos objetivo comprenden a los usuarios finales a los que nuestra solución busca atender. Para el caso de nuestra plataforma se han determinado los siguientes perfiles prioritarios:

#### Segmento objetivo #1: Operarios de Planta

**Descripción general**

Este segmento está constituido por el personal operativo de primera línea responsable de la ejecución de procesos productivos, mantenimiento de maquinaria y manipulación de insumos en entornos industriales.

**Aspectos demográficos:**

*   **Edad:** 20 a 55 años.
*   **Género:** Masculino y femenino.
*   **Nivel Educativo:** Técnico o secundaria completa con certificaciones operativas específicas.
*   **Ubicación:** Zonas de alta actividad industrial (Lima, Callao) o enclaves mineros/energéticos.
*   **Nivel digital:** Básico; usuarios de smartphones para redes sociales y mensajería, pero requieren herramientas laborales simplificadas.

**Aspectos conductuales:**

Su prioridad es el trabajo de campo y suelen usar el celular solo para consultas rápidas o reportes breves. No les gusta perder tiempo en formularios largos; prefieren herramientas sencillas que les den alertas claras y los ayuden a evitar accidentes sin interrumpir su ritmo de producción.

**Información estadística de sustento**

La investigación demuestra que cuando el personal operativo utiliza herramientas de identificación de actos inseguros (como cartillas de reporte), se logra una reducción del 50% en los accidentes de trabajo (de 37 a 18 casos en el periodo de estudio) (Escudero, 2022).

**Necesidad**

El operario requiere un medio de reporte inmediato para registrar "casi-accidentes" sin interrumpir su flujo de trabajo, asegurando que esta información genere alertas preventivas en tiempo real sobre zonas de riesgo. Su prioridad es una herramienta que garantice que sus reportes sean gestionados por los supervisores, transformando los datos capturados en soluciones operativas que protejan su integridad física.

---

#### Segmento objetivo #2: Supervisores de Seguridad y Mantenimiento

**Descripción general**

Este segmento está formado por mandos medios responsables de la seguridad y el mantenimiento preventivo.

**Aspectos demográficos**

*   **Edad:** 25 a 50 años.
*   **Género:** Masculino y femenino.
*   **Nivel Educativo:** Universitario o técnico superior (Ingeniería Industrial, Seguridad, Mantenimiento o afines).
*   **Ubicación:** Plantas industriales, almacenes o sedes administrativas de operaciones.
*   **Nivel digital:** Medio-Alto; habituados al uso de laptops, tablets, hojas de cálculo y sistemas de gestión (ERP/EAM).

**Aspectos conductuales**

Supervisan métricas a diario para planificar el mantenimiento y la seguridad con un enfoque en la eficiencia normativa. Buscan centralizar la información de campo en herramientas digitales que les permitan reaccionar rápido ante anomalías, eliminando procesos manuales y brechas de comunicación con el personal.

**Información estadística de sustento**

Según una investigación antes de contar con herramientas de gestión adecuadas, el 39% de los trabajadores percibía que la labor del supervisor no influía en la prevención; sin embargo, tras implementar reportes y seguimiento, el 83% de los colaboradores reconoció una mejora significativa en el liderazgo y compromiso de sus jefaturas (Escudero 2022).

**Necesidad**

El supervisor necesita centralizar los reportes de campo en un dashboard de visualización que le permita identificar patrones de riesgo mediante mapas de calor y alertas automáticas. Su prioridad es contar con una herramienta que automatice la gestión de actos y condiciones inseguras, asegurando que el motor de reglas del sistema priorice los peligros críticos para intervenir proactivamente antes de que ocurra una falla mayor.

---

#### Segmento objetivo #3: Gerentes y Administradores

**Descripción general**

Este segmento está constituido por la alta dirección, jefaturas de planta y responsables administrativos encargados de asegurar la continuidad del negocio, la rentabilidad y el cumplimiento estricto de la Ley.

**Aspectos demográficos**

*   **Edad:** 35 a 60 años.
*   **Género:** Masculino y femenino.
*   **Nivel Educativo:** Postgrado o Especialización (Maestrías en Gestión de Operaciones, MBA, Derecho Laboral o Seguridad Industrial).
*   **Ubicación:** Sedes corporativas u oficinas administrativas de empresas industriales y logísticas.
*   **Nivel digital:** Alto; usuarios de herramientas de reporte ejecutivo, software de gestión (ERP) y tableros de control (Dashboards).

**Aspectos conductuales**

Toman decisiones basadas en indicadores macro y tendencias de largo plazo. Su prioridad es la eficiencia operativa y la reputación de la empresa; buscan herramientas que automaticen la burocracia legal y les den una "foto" clara del estado de la planta sin necesidad de bajar al campo. Valoran la veracidad de los datos y la capacidad de anticiparse a crisis reputacionales o paradas de planta costosas.

**Información estadística de sustento**

Un estudio de la Sociedad Nacional de Industrias mostró que el 45% de los empresarios industriales incrementó sus gastos en seguridad; mientras que el 15% tuvo que reducir, postergar o cancelar inversiones debido a incidentes y riesgos que afectaron la continuidad del negocio.

**Necesidad**

El administrador y el gerente necesitan una visión consolidada y predictiva que justifique la inversión en seguridad. Su prioridad es contar con un sistema que exporte automáticamente formatos de auditoría legales y muestre Dashboards con indicadores predictivos, permitiéndoles identificar brechas de seguridad antes de que se conviertan en siniestros reales o sanciones legales que afecten la rentabilidad.

