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

### 1.2.2.4. Lean UX Canvas
