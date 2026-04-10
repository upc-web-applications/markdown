## 1.2.2. Lean UX Process

### 1.2.2.1. Lean UX Problem Statements

Nuestra plataforma se sitúa en el dominio de la Seguridad y Salud en el Trabajo (SST) bajo un enfoque de analítica predictiva. Está dirigida principalmente a empresas del sector manufacturero y logístico en el Perú, las cuales operan bajo la normativa de la Ley N° 29783. Actualmente, estos segmentos carecen de herramientas digitales que permitan procesar indicadores preventivos en tiempo real, limitándose al registro reactivo de accidentes ya ocurridos

Hemos identificado como problema central la alta dependencia de procesos manuales, lo que genera una "ceguera operativa": los datos de incidentes menores, fallas de maquinaria y actos inseguros no se cruzan ni se analizan. Esta fragmentación de la información impide identificar patrones de riesgo antes de que se conviertan en accidentes fatales o paradas de planta costosas

Nuestra visión es ofrecer una aplicación web desarrollada con C# y Vue.js que actúe como un motor de inteligencia preventiva. El sistema permitirá a los supervisores reportar condiciones inseguras mediante una interfaz dinamica, mientras que un motor de reglas en el backend calculará automáticamente niveles de criticidad.

### 1.2.2.2. Lean UX Assumptions

#### Features

- Interfaz grafica para el registro rápido de incidentes, permitiendo adjuntar evidencia fotográfica de condiciones inseguras en tiempo real.
- Algoritmos que aplican modelos matematicos de riesgo para categorizar la urgencia de cada hallazgo.
- Panel visual con mapas de calor y gráficas de tendencia que se actualizan sin necesidad de recargar la página, facilitando el monitoreo continuo de la planta.
- Funcionalidad para exportar documentos de auditoría que cumplan con los formatos referenciales de la ley peruana.

#### Needings

- Las empresas presentan una deficiencia en la capacidad de prevención de riesgos, causada por el uso de métodos de registro que no permiten un análisis estadístico oportuno.
- Los Usuarios necesitan superar esta deficiencia aprendiendo a identificar y registrar peligros de manera digital, confiando en que el sistema procesará esa información para alertar sobre riesgos inminentes.
- Empresas de manufactura y logistica estan interesados en optimizar sus sistemas de gestion de la seguridad con el fin de reducir la tasa de accidentes.
- Los administradores desean ver una grafica de tendencia en base a los datos de ingresados.
- Corregir la brecha entre el hallazgo de un peligro y su mitigación mediante una plataforma accesible y predictiva que prepare a la organización para actuar ante situaciones críticas antes de que ocurran accidentes.
- La falta de veracidad en el llenado de datos por parte del personal operativo, lo cual se abordará con interfaces simplificadas y validaciones automáticas de integridad en el frontend.
- Sistemas de gestión documental genéricos o formularios en Excel, que carecen de la capacidad reactiva y del motor predictivo propuesto en ....

### 1.2.2.3. Lean UX Hypothesis Statements

**Creemos** que digitalizar el proceso de inspeccion mediante la aplicacion web ... evolucionará la captura de datos en planta. 
**Sabremos** que lo propuesto es cierto 
**Cuando** los reportes diarios se incrementen en un 40% debido a la facilidad de uso frente al registro en hojas de calculos o papel

**Creemos** que integrar un motor de reglas en la aplicacion web permitira predecir accidentes antes de que ocurran. 
**Sabremos** que lo propuesto es cierto
**Cuando** el sistema identifique correctamente al menos el 70% de las áreas de alta criticidad antes de que se registre un siniestro real

**Creemos** que ofrecer Dashboards visuales con indicadores predictivos potenciara la toma de decisiones gerenciales
**Sabremos** que lo propuesto es cierto 
**Cuando** se reporte una reduccion del 50% en el tiempo dedicado a elaborar informes mensuales de gestion.

**Creemos** que ofrecer una plataforma ligera y accesible desde navegadores web permitirá la adopción de ... en empresas con baja infraestructura tecnológica. 
**Sabremos** que esto es cierto 
**Cuando** logremos mantener una tasa de disponibilidad del sistema superior al 70% sin requerir hardware especializado del lado del cliente.

### 1.2.2.4. Lean UX Canvas
<div align="center">
  <p>
    <b>Grafico 2</b>: Lean UX Canvas
  </p>
  <img src="../assets/images/leanuxcanvas-app-web.png" alt="Grafico 2" />
  <p>
    <i><b>Fuente</b>: Elaboración propia</i>
  </p>
</div>

## 1.3. Segmentos Objetivo

Los segmentos objetivo comprenden a los usuarios finales a los que nuestra solución busca atender. Para el caso de nuestra plataforma se han determinado los siguientes perfiles prioritarios:

### Segmento objetivo #1: Operarios de Planta

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

### Segmento objetivo #2: Supervisores de Seguridad y Mantenimiento

**Descripción general**

Este segmento está formado por mandos medios responsables de la seguridad y el mantenimiento preventivo.

**Aspectos demográficos**

*   **Edad:** 28 a 50 años.
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

### Segmento objetivo #3: Gerentes y Administradores

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
