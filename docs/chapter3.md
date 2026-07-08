# Capítulo III: Requirements Specification

## 3.1. User Stories

### Epics

<table align="center">
    <tr>
        <td align="center">
        <b>Epic ID</b>
        </td>
        <td align="center">
        <b>Descripción de la épica</b>
        </td>
    </tr>
    <tr>
        <td align="center"><b>EP01</b></td>
        <td align="center">Operario de Planta</td>
    </tr>
    <tr>
        <td align="center"><b>EP02</b></td>
        <td align="center">Motor Predictivo y Análisis de Riesgos</td>
    </tr>
    <tr>
        <td align="center"><b>EP03</b></td>
        <td align="center">Gestión de Alertas y Mitigación de Incidentes</td>
    </tr>
    <tr>
        <td align="center"><b>EP04</b></td>
        <td align="center">Dashboard Ejecutivo y Reportes de Cumplimiento</td>
    </tr>
    <tr>
        <td align="center"><b>EP05</b></td>
        <td align="center">Configuración del Sistema</td>
    </tr>
    <tr>
        <td align="center"><b>EP06</b></td>
        <td align="center">Presencia Digital y Estrategia de Conversión de Usuarios</td>
    </tr>
</table>



### User Stories

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US01</b></td>
<td>Autenticación de Operario</td>
<td>Como usuario, quiero iniciar sesión en RiskGuard con mis credenciales asignadas, para acceder a las funciones correspondientes a mi rol.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Autenticación de Operario.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Inicio de sesión exitoso<br/>
<ul>
<li><b>Given</b> que el usuario se encuentra en la pantalla de inicio de sesión,</li>
<li><b>When</b> ingresa su correo y contraseña correctos y hace clic en "Ingresar",</li>
<li><b>Then</b> el sistema valida las credenciales,</li>
<li><b>And</b> redirige al operario a su vista principal de funciones.</li>
</ul>
<b>Escenario 2:</b> Credenciales inválidas<br/>
<ul>
<li><b>Given</b> que el usuario se encuentra en la pantalla de inicio de sesión,</li>
<li><b>When</b> ingresa alguna credencial incorrecta y hace clic en "Ingresar",</li>
<li><b>Then</b> el sistema deniega el acceso,</li>
<li><b>And</b> muestra el mensaje "Correo o contraseña incorrectos".</li>
</ul>
<b>Escenario 3:</b> Bloqueo por intentos fallidos<br/>
<ul>
<li><b>Given</b> que el Operario acumula 5 intentos fallidos consecutivos,</li>
<li><b>When</b> intenta ingresar nuevamente,</li>
<li><b>Then</b> el sistema bloquea la cuenta temporalmente,</li>
<li><b>And</b> muestra el mensaje "Demasiados intentos fallidos. Intente en 15 minutos".</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US02</b></td>
<td>Cierre de Sesión del Operario</td>
<td>Como usuario, quiero cerrar sesión de forma segura desde la aplicación, para proteger mi cuenta en dispositivos compartidos del área de trabajo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Cierre de Sesión del Operario.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Cierre de sesión exitoso<br/>
<ul>
<li><b>Given</b> que el usuario se encuentra en cualquier pantalla de la aplicación,</li>
<li><b>When</b> hace clic en "Cerrar sesión" desde el menú,</li>
<li><b>Then</b> el sistema invalida su token de autenticación,</li>
<li><b>And</b> redirige al operario a la pantalla de inicio de sesión.</li>
</ul>
<b>Escenario 2:</b> Cierre con reporte en proceso<br/>
<ul>
<li><b>Given</b> que el usuario tiene un formulario de reporte con datos ingresados sin enviar,</li>
<li><b>When</b> intenta cerrar sesión,</li>
<li><b>Then</b> el sistema muestra el mensaje "Tienes un reporte sin enviar. ¿Deseas salir de todas formas?",</li>
<li><b>And</b> ofrece las opciones "Continuar reportando" y "Salir sin guardar".</li>
</ul>
<b>Escenario 3:</b> Intento de acceso tras cerrar sesión<br/>
<ul>
<li><b>Given</b> que el usuario cerró sesión correctamente,</li>
<li><b>When</b> intenta acceder a una URL protegida directamente,</li>
<li><b>Then</b> el sistema detecta que no hay token válido,</li>
<li><b>And</b> redirige automáticamente a la pantalla de inicio de sesión.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US03</b></td>
<td>Registro Rápido de Casi-Accidente</td>
<td>Como Operario de Planta, quiero registrar un casi-accidente desde mi celular en menos de 30 segundos, para asegurarme de que la información llegue al sistema sin interrumpir mi flujo de trabajo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Registro Rápido de Casi-Accidente.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Registro exitoso<br/>
<ul>
<li><b>Given</b> que el Operario se encuentra en su pantalla principal,</li>
<li><b>When</b> hace clic en "Nuevo Reporte", completa los campos obligatorios y presiona "Enviar",</li>
<li><b>Then</b> el sistema registra el incidente en la base de datos,</li>
<li><b>And</b> muestra el mensaje "Reporte enviado correctamente".</li>
</ul>
<b>Escenario 2:</b> Campos incompletos<br/>
<ul>
<li><b>Given</b> que el Operario está completando el formulario de reporte,</li>
<li><b>When</b> intenta enviar sin completar todos los campos obligatorios,</li>
<li><b>Then</b> el sistema bloquea el envío,</li>
<li><b>And</b> resalta en rojo los campos pendientes indicando cuáles son requeridos.</li>
</ul>
<b>Escenario 3:</b> Confirmación de reporte enviado<br/>
<ul>
<li><b>Given</b> que el Operario completó y envió el formulario correctamente,</li>
<li><b>When</b> el sistema procesa el registro,</li>
<li><b>Then</b> el operario visualiza una confirmación con el número de reporte asignado,</li>
<li><b>And</b> puede volver a la pantalla principal con un solo clic.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US04</b></td>
<td>Adjuntar Evidencia Fotográfica al Reporte</td>
<td>Como Operario de Planta, quiero adjuntar una foto desde mi celular al momento de reportar un incidente, para proporcionar evidencia visual que facilite la evaluación del riesgo por parte del supervisor.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Adjuntar Evidencia Fotográfica al Reporte.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Adjuntar foto exitosamente<br/>
<ul>
<li><b>Given</b> que el Operario está completando el formulario de reporte,</li>
<li><b>When</b> hace clic en "Adjuntar foto" y selecciona una imagen válida desde su galería,</li>
<li><b>Then</b> el sistema muestra una miniatura de previsualización de la imagen,</li>
<li><b>And</b> la imagen queda lista para enviarse junto al reporte.</li>
</ul>
<b>Escenario 2:</b> Imagen supera el tamaño máximo<br/>
<ul>
<li><b>Given</b> que el Operario intenta adjuntar una imagen al formulario,</li>
<li><b>When</b> selecciona un archivo que supera los 5 MB,</li>
<li><b>Then</b> el sistema rechaza el archivo,</li>
<li><b>And</b> muestra el mensaje "La imagen supera el tamaño permitido. Máximo 5 MB".</li>
</ul>
<b>Escenario 3:</b> Eliminar foto antes de enviar<br/>
<ul>
<li><b>Given</b> que el Operario adjuntó una foto al formulario,</li>
<li><b>When</b> hace clic en el ícono de eliminar sobre la miniatura,</li>
<li><b>Then</b> el sistema elimina la imagen adjunta del formulario,</li>
<li><b>And</b> el operario puede adjuntar una foto diferente o enviar el reporte sin imagen.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US05</b></td>
<td>Selección de Sector al Registrar Incidente</td>
<td>Como Operario de Planta, quiero seleccionar el sector de la planta donde ocurrió el incidente al momento de reportarlo, para que el sistema pueda georreferenciar el riesgo correctamente y el supervisor identifique la zona afectada.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Selección de Sector al Registrar Incidente.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Selección de sector exitosa<br/>
<ul>
<li><b>Given</b> que el Operario está completando el formulario de reporte,</li>
<li><b>When</b> despliega la lista de sectores y selecciona el sector correspondiente,</li>
<li><b>Then</b> el sistema registra el sector seleccionado en el formulario,</li>
<li><b>And</b> lo vincula al ticket del incidente al momento del envío.</li>
</ul>
<b>Escenario 2:</b> No hay sectores activos disponibles<br/>
<ul>
<li><b>Given</b> que el Operario intenta seleccionar un sector en el formulario,</li>
<li><b>When</b> despliega la lista y no existen sectores activos registrados,</li>
<li><b>Then</b> el sistema muestra el mensaje "No hay sectores disponibles. Contacte a su supervisor",</li>
<li><b>And</b> bloquea el envío del formulario hasta que exista al menos un sector activo.</li>
</ul>
<b>Escenario 3:</b> Intento de envío sin seleccionar sector<br/>
<ul>
<li><b>Given</b> que el Operario completó el formulario pero omitió seleccionar sector,</li>
<li><b>When</b> hace clic en "Enviar",</li>
<li><b>Then</b> el sistema bloquea el envío,</li>
<li><b>And</b> muestra el mensaje "Debe seleccionar el sector donde ocurrió el incidente".</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US06</b></td>
<td>Selección del Nivel de Urgencia del Incidente</td>
<td>Como Operario de Planta, quiero indicar el nivel de urgencia del incidente que estoy reportando, para que el sistema priorice correctamente la alerta hacia el supervisor.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Selección del Nivel de Urgencia del Incidente.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Selección de nivel Alto<br/>
<ul>
<li><b>Given</b> que el Operario está completando el formulario de reporte,</li>
<li><b>When</b> selecciona el nivel de urgencia "Alto",</li>
<li><b>Then</b> el campo queda resaltado en rojo,</li>
<li><b>And</b> al enviar, el sistema genera una alerta de prioridad crítica hacia el supervisor.</li>
</ul>
<b>Escenario 2:</b> Envío sin seleccionar nivel<br/>
<ul>
<li><b>Given</b> que el Operario intenta enviar el formulario sin seleccionar nivel de urgencia,</li>
<li><b>When</b> hace clic en "Enviar",</li>
<li><b>Then</b> el sistema bloquea el envío,</li>
<li><b>And</b> muestra el mensaje "Debe seleccionar el nivel de urgencia del incidente".</li>
</ul>
<b>Escenario 3:</b> Cambio de nivel antes de enviar<br/>
<ul>
<li><b>Given</b> que el Operario seleccionó un nivel de urgencia en el formulario,</li>
<li><b>When</b> decide cambiarlo antes de enviar,</li>
<li><b>Then</b> el sistema actualiza el campo con el nuevo nivel seleccionado,</li>
<li><b>And</b> el color del indicador cambia acorde al nuevo nivel elegido.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US07</b></td>
<td>Selección del Tipo de Incidente</td>
<td>Como Operario de Planta, quiero seleccionar el tipo de incidente de una lista predefinida al momento de reportar, para categorizar correctamente el riesgo y facilitar el análisis posterior del sistema.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Selección del Tipo de Incidente.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Selección de tipo exitosa<br/>
<ul>
<li><b>Given</b> que el Operario está completando el formulario,</li>
<li><b>When</b> selecciona "Falla de equipo" de la lista,</li>
<li><b>Then</b> el sistema registra el tipo en el formulario,</li>
<li><b>And</b> lo incluye en el ticket al momento del envío.</li>
</ul>
<b>Escenario 2:</b> Envío sin tipo seleccionado<br/>
<ul>
<li><b>Given</b> que el Operario intenta enviar el formulario sin seleccionar tipo,</li>
<li><b>When</b> hace clic en "Enviar",</li>
<li><b>Then</b> el sistema bloquea el envío,</li>
<li><b>And</b> muestra el mensaje "Debe seleccionar el tipo de incidente".</li>
</ul>
<b>Escenario 3:</b> Selección de tipo "Otro"<br/>
<ul>
<li><b>Given</b> que el Operario selecciona el tipo "Otro",</li>
<li><b>When</b> el sistema detecta esa selección,</li>
<li><b>Then</b> habilita un campo de texto adicional obligatorio para describir el tipo,</li>
<li><b>And</b> bloquea el envío si ese campo queda vacío.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US08</b></td>
<td>Registro de Condición Insegura Vinculada a un Activo</td>
<td>Como Operario de Planta, quiero vincular mi reporte a un activo específico de la planta, para indicar con precisión qué máquina o equipo presenta la condición insegura.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Registro de Condición Insegura Vinculada a un Activo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Vincular reporte a un activo<br/>
<ul>
<li><b>Given</b> que el Operario seleccionó un sector en el formulario,</li>
<li><b>When</b> despliega la lista de activos y selecciona la máquina correspondiente,</li>
<li><b>Then</b> el sistema vincula el activo al reporte,</li>
<li><b>And</b> el ticket queda registrado con la referencia exacta del activo afectado.</li>
</ul>
<b>Escenario 2:</b> Sector sin activos registrados<br/>
<ul>
<li><b>Given</b> que el Operario seleccionó un sector sin activos activos asociados,</li>
<li><b>When</b> intenta desplegar la lista de activos,</li>
<li><b>Then</b> el sistema muestra el mensaje "No hay activos registrados en este sector",</li>
<li><b>And</b> permite continuar el reporte sin vincular activo.</li>
</ul>
<b>Escenario 3:</b> Envío sin activo seleccionado<br/>
<ul>
<li><b>Given</b> que el Operario no seleccionó ningún activo en el formulario,</li>
<li><b>When</b> hace clic en "Enviar",</li>
<li><b>Then</b> el sistema procesa el reporte correctamente vinculado solo al sector,</li>
<li><b>And</b> no muestra ningún error por el campo de activo vacío.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US09</b></td>
<td>Descripción de Texto Libre en el Reporte</td>
<td>Como Operario de Planta, quiero ingresar una descripción en texto libre al momento de reportar un incidente, para detallar con mis propias palabras lo que observé y dar más contexto al supervisor.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Descripción de Texto Libre en el Reporte.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Descripción ingresada correctamente<br/>
<ul>
<li><b>Given</b> que el Operario está completando el formulario,</li>
<li><b>When</b> ingresa una descripción válida en el campo de texto,</li>
<li><b>Then</b> el contador muestra los caracteres restantes en tiempo real,</li>
<li><b>And</b> la descripción queda registrada en el ticket al momento del envío.</li>
</ul>
<b>Escenario 2:</b> Descripción que supera el límite<br/>
<ul>
<li><b>Given</b> que el Operario está escribiendo en el campo de descripción,</li>
<li><b>When</b> alcanza el límite de 300 caracteres,</li>
<li><b>Then</b> el sistema deja de aceptar nuevos caracteres,</li>
<li><b>And</b> el contador muestra "0 caracteres restantes" resaltado en rojo.</li>
</ul>
<b>Escenario 3:</b> Descripción con solo espacios en blanco<br/>
<ul>
<li><b>Given</b> que el Operario ingresa solo espacios en el campo de descripción,</li>
<li><b>When</b> hace clic en "Enviar",</li>
<li><b>Then</b> el sistema bloquea el envío,</li>
<li><b>And</b> muestra el mensaje "La descripción no puede estar vacía".</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US10</b></td>
<td>Confirmación de Recepción del Reporte</td>
<td>Como Operario de Planta, quiero recibir una confirmación visible después de enviar mi reporte, para saber que la información llegó correctamente al sistema y no quedó perdida.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Confirmación de Recepción del Reporte.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Confirmación exitosa<br/>
<ul>
<li><b>Given</b> que el Operario envió correctamente el formulario de reporte,</li>
<li><b>When</b> el sistema procesa el registro,</li>
<li><b>Then</b> muestra el mensaje "Reporte enviado. Número de ticket: #XXXX",</li>
<li><b>And</b> el operario puede volver a la pantalla principal con un solo clic.</li>
</ul>
<b>Escenario 2:</b> Fallo en el envío por error de conexión<br/>
<ul>
<li><b>Given</b> que el Operario intenta enviar el reporte sin conexión a internet,</li>
<li><b>When</b> hace clic en "Enviar",</li>
<li><b>Then</b> el sistema muestra el mensaje "Error al enviar. Verifique su conexión e intente nuevamente",</li>
<li><b>And</b> conserva los datos ingresados para que el operario no deba rellenar el formulario nuevamente.</li>
</ul>
<b>Escenario 3:</b> Reintento tras fallo<br/>
<ul>
<li><b>Given</b> que el sistema mostró un error al enviar el reporte,</li>
<li><b>When</b> el operario recupera la conexión y hace clic en "Reintentar",</li>
<li><b>Then</b> el sistema procesa el envío con los mismos datos,</li>
<li><b>And</b> muestra la confirmación con el número de ticket asignado.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US11</b></td>
<td>Notificación de Atención del Reporte</td>
<td>Como Operario de Planta, quiero recibir una notificación cuando mi reporte haya sido revisado o atendido por el supervisor, para saber que mi reporte tuvo un impacto real y no fue ignorado.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Notificación de Atención del Reporte.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Notificación de ticket en progreso<br/>
<ul>
<li><b>Given</b> que el Operario envió un reporte previamente,</li>
<li><b>When</b> el supervisor asigna el ticket a un técnico y cambia su estado a "En Progreso",</li>
<li><b>Then</b> el sistema envía una notificación al operario indicando "Tu reporte #XXXX está siendo atendido",</li>
<li><b>And</b> la notificación aparece en su centro de notificaciones.</li>
</ul>
<b>Escenario 2:</b> Notificación de ticket resuelto<br/>
<ul>
<li><b>Given</b> que el ticket del operario fue atendido por el técnico asignado,</li>
<li><b>When</b> el supervisor cambia el estado del ticket a "Resuelto",</li>
<li><b>Then</b> el sistema notifica al operario "Tu reporte #XXXX ha sido resuelto",</li>
<li><b>And</b> el operario puede consultar el detalle de la resolución desde la notificación.</li>
</ul>
<b>Escenario 3:</b> Marcar notificación como leída<br/>
<ul>
<li><b>Given</b> que el Operario tiene notificaciones pendientes en su centro de notificaciones,</li>
<li><b>When</b> hace clic sobre una notificación,</li>
<li><b>Then</b> el sistema la marca como leída,</li>
<li><b>And</b> actualiza el contador de notificaciones no leídas.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US12</b></td>
<td>Historial de Reportes del Operario</td>
<td>Como Operario de Planta, quiero consultar el historial de los reportes que he enviado, para hacer seguimiento del estado de cada uno y verificar que fueron atendidos.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Historial de Reportes del Operario.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Consulta del historial con reportes registrados<br/>
<ul>
<li><b>Given</b> que el Operario ingresa a la sección "Mis Reportes",</li>
<li><b>When</b> el sistema recupera sus registros,</li>
<li><b>Then</b> muestra la lista de reportes enviados con su estado actual,</li>
<li><b>And</b> los ordena del más reciente al más antiguo.</li>
</ul>
<b>Escenario 2:</b> Filtrado por estado<br/>
<ul>
<li><b>Given</b> que el Operario visualiza su historial de reportes,</li>
<li><b>When</b> selecciona el filtro "Pendiente",</li>
<li><b>Then</b> el sistema muestra únicamente los tickets que aún no han sido atendidos,</li>
<li><b>And</b> oculta los reportes con estado "En Progreso" o "Resuelto".</li>
</ul>
<b>Escenario 3:</b> Historial vacío<br/>
<ul>
<li><b>Given</b> que el Operario ingresa a "Mis Reportes" por primera vez,</li>
<li><b>When</b> el sistema consulta su historial,</li>
<li><b>Then</b> muestra el mensaje "Aún no has enviado ningún reporte",</li>
<li><b>And</b> muestra un botón directo para crear el primer reporte.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US13</b></td>
<td>Consulta del Detalle de un Reporte Enviado</td>
<td>Como Operario de Planta, quiero ver el detalle completo de un reporte que envié, para conocer la descripción registrada, el sector, la foto adjunta y el estado actual de atención.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Consulta del Detalle de un Reporte Enviado.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Ver detalle de reporte pendiente<br/>
<ul>
<li><b>Given</b> que el Operario accede a su historial de reportes,</li>
<li><b>When</b> hace clic sobre un ticket con estado "Pendiente",</li>
<li><b>Then</b> el sistema muestra el detalle completo del reporte,</li>
<li><b>And</b> el estado aparece resaltado en amarillo indicando que está en espera.</li>
</ul>
<b>Escenario 2:</b> Ver detalle de reporte resuelto<br/>
<ul>
<li><b>Given</b> que el Operario accede al detalle de un ticket con estado "Resuelto",</li>
<li><b>When</b> el sistema carga la información,</li>
<li><b>Then</b> muestra la descripción de la acción correctiva registrada por el técnico,</li>
<li><b>And</b> el estado aparece en verde indicando que fue atendido.</li>
</ul>
<b>Escenario 3:</b> Ver foto adjunta en el detalle<br/>
<ul>
<li><b>Given</b> que el reporte incluye una foto adjunta,</li>
<li><b>When</b> el Operario accede al detalle del ticket,</li>
<li><b>Then</b> el sistema muestra la imagen en tamaño completo al hacer clic sobre la miniatura,</li>
<li><b>And</b> el operario puede cerrarla para volver al detalle del reporte.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US14</b></td>
<td>Visualización de Alertas Activas en el Sector</td>
<td>Como Operario de Planta, quiero ver las alertas activas en mi sector al ingresar a la aplicación, para estar informado de los riesgos identificados en mi zona de trabajo antes de iniciar mi turno.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de Alertas Activas en el Sector.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Sector con alertas activas<br/>
<ul>
<li><b>Given</b> que el Operario inicia sesión en la aplicación,</li>
<li><b>When</b> el sistema carga su pantalla principal,</li>
<li><b>Then</b> muestra las alertas activas de su sector ordenadas por urgencia,</li>
<li><b>And</b> cada alerta está diferenciada visualmente por color según su nivel.</li>
</ul>
<b>Escenario 2:</b> Sector sin alertas activas<br/>
<ul>
<li><b>Given</b> que el Operario inicia sesión y su sector no tiene alertas activas,</li>
<li><b>When</b> el sistema carga la pantalla principal,</li>
<li><b>Then</b> muestra el mensaje "Tu sector opera dentro de los parámetros seguros",</li>
<li><b>And</b> mantiene visible el botón de "Nuevo Reporte".</li>
</ul>
<b>Escenario 3:</b> Ver detalle de alerta activa<br/>
<ul>
<li><b>Given</b> que el Operario visualiza una alerta activa en su pantalla principal,</li>
<li><b>When</b> hace clic sobre ella,</li>
<li><b>Then</b> el sistema muestra el detalle de la alerta con descripción, sector y estado,</li>
<li><b>And</b> el operario puede volver a la pantalla principal desde el detalle.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US15</b></td>
<td>Edición de Reporte Antes del Envío</td>
<td>Como Operario de Planta, quiero poder revisar y corregir los datos de mi reporte antes de enviarlo, para asegurarme de que la información registrada es precisa y completa.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Edición de Reporte Antes del Envío.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Corrección de campo antes del envío<br/>
<ul>
<li><b>Given</b> que el Operario completó el formulario pero detectó un error en la descripción,</li>
<li><b>When</b> edita el campo de descripción con el texto correcto,</li>
<li><b>Then</b> el formulario actualiza el contenido en tiempo real,</li>
<li><b>And</b> el sistema envía la versión corregida al hacer clic en "Enviar".</li>
</ul>
<b>Escenario 2:</b> Cambio de sector antes del envío<br/>
<ul>
<li><b>Given</b> que el Operario seleccionó un sector incorrecto,</li>
<li><b>When</b> lo cambia por el sector correcto antes de enviar,</li>
<li><b>Then</b> el sistema actualiza la lista de activos disponibles al nuevo sector,</li>
<li><b>And</b> limpia la selección de activo previa para evitar inconsistencias.</li>
</ul>
<b>Escenario 3:</b> Cancelar reporte en proceso<br/>
<ul>
<li><b>Given</b> que el Operario está completando el formulario,</li>
<li><b>When</b> hace clic en "Cancelar",</li>
<li><b>Then</b> el sistema muestra el mensaje "¿Deseas descartar este reporte?",</li>
<li><b>And</b> si confirma, descarta los datos y regresa a la pantalla principal.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>

---


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US16</b></td>
<td>Visualización de Métricas de Impacto Predictivo</td>
<td>Como visitante, quiero visualizar indicadores reales de siniestralidad y beneficios del sistema en la Landing Page de RiskGuard, para comprender el impacto de la analítica predictiva en la reducción de riesgos industriales.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de Métricas de Impacto Predictivo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Visualización de métricas<br/>
<ul>
<li><b>Given</b> que el visitante se encuentra navegando en la Landing Page,</li>
<li><b>When</b> se desplaza hasta la sección “La realidad de la industria peruana”,</li>
<li><b>Then</b> el sistema muestra métricas de reducción de accidentes, clima laboral,mejoras</li>
<li><b>And</b> estas métricas se visualizan de forma clara y destacada.</li>
</ul>
<b>Escenario 2:</b> Carga de la sección<br/>
<ul>
<li><b>Given</b> que el visitante accede al landing,</li>
<li><b>When</b> la sección de métricas se renderiza,</li>
<li><b>Then</b> el contenido carga en menos de 3 segundos,</li>
<li><b>And</b> no presenta errores visuales.</li>
</ul>
<b>Escenario 3:</b> Acceso sin autenticación<br/>
<ul>
<li><b>Given</b> que el visitante no ha iniciado sesión,</li>
<li><b>When</b> navega por la landing,</li>
<li><b>Then</b> puede visualizar las métricas sin restricciones,</li>
<li><b>And</b> el sistema no solicita autenticación.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US17</b></td>
<td>Interacción con Botones de Conversión</td>
<td>Como visitante, quiero interactuar con los botones “Iniciar prueba gratuita” y “Hablar con ventas”, para contactar con el servicio de RiskGuard.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Interacción con Botones de Conversión.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Redirección correcta<br/>
<ul>
<li><b>Given</b> que el visitante está en el landing,</li>
<li><b>When</b> hace clic en “Iniciar prueba gratuita”,</li>
<li><b>Then</b> el sistema redirige al formulario,</li>
</ul>
<b>Escenario 2:</b> Registro de interacción<br/>
<ul>
<li><b>Given</b> que el usuario hace clic,</li>
<li><b>When</b> se ejecuta la acción,</li>
<li><b>Then</b> el sistema registra el evento,</li>
</ul>
<b>Escenario 3:</b> Compatibilidad móvil<br/>
<ul>
<li><b>Given</b> que el usuario accede desde móvil,</li>
<li><b>When</b> presiona el botón,</li>
<li><b>Then</b> responde correctamente,</li>
<li><b>And</b> mantiene diseño adaptado.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US18</b></td>
<td>Visualización de Alerta por Riesgo Recurrente en sector</td>
<td>Como supervisor de seguridad, quiero recibir una alerta cuando el mismo tipo de riesgo se repita más de 3 veces en 30 días en una misma sector, para intervenir antes de que ocurra un accidente.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de Alerta por Riesgo Recurrente en sector.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Patrón recurrente detectado<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad se encuentra en el dashboard de monitoreo de RiskGuard,</li>
<li><b>When</b> el sistema detecta que el mismo tipo de riesgo ha ocurrido por cuarta vez en el sector de Almacén dentro de los últimos 30 días,</li>
<li><b>Then</b> el sistema muestra una alerta de patrón recurrente en el dashboard,</li>
<li><b>And</b> la alerta indica el tipo de riesgo, el sector afectada, el número de ocurrencias y la fecha del primer reporte del período.</li>
</ul>
<b>Escenario 2:</b> Riesgo sin patrón recurrente<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad se encuentra en el dashboard de monitoreo,</li>
<li><b>When</b> el riesgo registrado tiene menos de 3 ocurrencias en los últimos 30 días en esa sector,</li>
<li><b>Then</b> el sistema no genera ninguna alerta de recurrencia para ese riesgo.</li>
</ul>
<b>Escenario 3:</b> Ver detalle de la alerta de recurrencia<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad visualiza una alerta de patrón recurrente en el dashboard,</li>
<li><b>When</b> hace clic sobre la alerta,</li>
<li><b>Then</b> el sistema muestra el historial de ocurrencias del riesgo en esa sector con fechas y detalles de cada reporte,</li>
<li><b>And</b> el supervisor puede volver al dashboard con un solo clic.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US19</b></td>
<td>Visualización de Mapa de Calor de Riesgos de la Planta</td>
<td>Como supervisor de seguridad, quiero ver un mapa de calor actualizado de la planta con la concentración de riesgos activos por zona, para priorizar mis recursos de inspección donde más se necesitan.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de Mapa de Calor de Riesgos de la Planta.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Zona crítica identificada en el mapa<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad se encuentra en la pantalla del mapa de calor de RiskGuard,</li>
<li><b>When</b> el sector de Almacén tiene 4 riesgos activos de criticidad alta sin resolver,</li>
<li><b>Then</b> el sistema resalta el sector de Almacén con la intensidad de color más alta del mapa,</li>
<li><b>And</b> la diferencia visual con las zonas de menor concentración es clara y distinguible.</li>
</ul>
<b>Escenario 2:</b> Planta sin riesgos activos<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad accede al mapa de calor,</li>
<li><b>When</b> ninguna sector de la planta tiene riesgos activos registrados,</li>
<li><b>Then</b> el sistema muestra todas las sectors en el nivel de intensidad más bajo,</li>
<li><b>And</b> muestra el mensaje "No hay riesgos activos registrados en la planta".</li>
</ul>
<b>Escenario 3:</b> Ver detalle de sector desde el mapa<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad visualiza el mapa de calor con sectors resaltadas,</li>
<li><b>When</b> hace clic sobre el sector de Producción,</li>
<li><b>Then</b> el sistema muestra la lista de riesgos activos de ese sector con su tipo, criticidad y estado,</li>
<li><b>And</b> el supervisor puede volver al mapa con un solo clic.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

---
<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US20</b></td>
<td>Notificación de Riesgo Crítico Sin Atender</td>
<td>Como supervisor de seguridad, quiero que el sistema me notifique cuando un riesgo crítico lleve más de 24 horas sin ser atendido, para escalar la situación a gerencia a tiempo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Notificación de Riesgo Crítico Sin Atender.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Notificación de escalamiento enviada<br/>
<ul>
<li><b>Given</b> que existe un riesgo crítico registrado hace más de 24 horas sin acción correctiva asignada,</li>
<li><b>When</b> el sistema evalúa los riesgos activos pendientes,</li>
<li><b>Then</b> el supervisor de seguridad recibe una notificación de escalamiento en su centro de notificaciones,</li>
<li><b>And</b> la notificación detalla el sector afectada, el tipo de riesgo y el tiempo transcurrido sin atención.</li>
</ul>
<b>Escenario 2:</b> Sin notificación cuando el riesgo fue atendido a tiempo<br/>
<ul>
<li><b>Given</b> que un riesgo crítico tiene acción correctiva asignada dentro de las primeras 24 horas de su registro,</li>
<li><b>When</b> el sistema evalúa los riesgos activos,</li>
<li><b>Then</b> el sistema no genera ninguna notificación de escalamiento para ese riesgo.</li>
</ul>
<b>Escenario 3:</b> Ver detalle del riesgo desde la notificación<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad recibió una notificación de escalamiento,</li>
<li><b>When</b> hace clic sobre la notificación,</li>
<li><b>Then</b> el sistema lo redirige al detalle del ticket del riesgo crítico sin atender,</li>
<li><b>And</b> puede asignar una acción correctiva directamente desde esa pantalla.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US21</b></td>
<td>Filtrado de Patrones de Riesgo por Tipo de Peligro</td>
<td>Como supervisor de seguridad, quiero filtrar los patrones de riesgo detectados por tipo de peligro (físico, químico, ergonómico, otros), para analizar de forma segmentada cuál categoría representa mayor amenaza en la planta.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Filtrado de Patrones de Riesgo por Tipo de Peligro.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Filtro aplicado con resultados<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad se encuentra en el panel de patrones de riesgo de RiskGuard,</li>
<li><b>When</b> selecciona el filtro de tipo de peligro "Ergonómico",</li>
<li><b>Then</b> el sistema muestra únicamente los patrones recurrentes de tipo ergonómico,</li>
<li><b>And</b> oculta los patrones de las demás categorías de peligro.</li>
</ul>
<b>Escenario 2:</b> Sin patrones para el tipo seleccionado<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad aplica el filtro de tipo de peligro "Quimico",</li>
<li><b>When</b> el sistema busca patrones de esa categoría en el período actual,</li>
<li><b>Then</b> el sistema muestra el mensaje "No hay patrones recurrentes de tipo químico en el período consultado".</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US22</b></td>
<td>Visualización de Resumen de Riesgos del Día</td>
<td>Como supervisor de seguridad, quiero ver cuántos riesgos nuevos se registraron hoy en cada sector, para tener una visión rápida del estado de la planta al inicio de mi turno.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de Resumen de Riesgos del Día.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Resumen del día con riesgos registrados<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad se encuentra en el dashboard de RiskGuard,</li>
<li><b>When</b> accede al panel,</li>
<li><b>Then</b> el sistema muestra el total de riesgos registrados hoy agrupados por sector,</li>
<li><b>And</b> cada sector indica la cantidad de riesgos nuevos, en progreso y resueltos.</li>
</ul>
<b>Escenario 2:</b> Sin riesgos registrados en el día<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad accede al dashboard al inicio del turno,</li>
<li><b>When</b> no se han registrado riesgos durante el día actual,</li>
<li><b>Then</b> el sistema muestra el mensaje "No se han reportado riesgos hoy".</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US23</b></td>
<td>Marcar Alerta de Patrón Recurrente como Revisada</td>
<td>Como supervisor de seguridad, quiero marcar una alerta de patrón recurrente como revisada, para indicar que ya tomé conocimiento de ella y mantener el dashboard organizado.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Marcar Alerta de Patrón Recurrente como Revisada.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Marcar alerta como revisada exitosamente<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad visualiza una alerta de patrón recurrente en el dashboard,</li>
<li><b>When</b> hace clic en "Marcar como revisada",</li>
<li><b>Then</b> el sistema mueve la alerta fuera del panel principal,</li>
</ul>
<b>Escenario 2:</b> Sin alertas pendientes en el panel<br/>
<ul>
<li><b>Given</b> que el supervisor de seguridad marcó todas las alertas de patrón como revisadas,</li>
<li><b>When</b> accede al panel principal de alertas,</li>
<li><b>Then</b> el sistema muestra el mensaje "No hay alertas de patrón pendientes por revisar".</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>
---
<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US24</b></td>
<td>Autenticación Segura de Supervisor</td>
<td>Como usuario, quiero iniciar sesión en la plataforma utilizando mis credenciales preconfiguradas, para acceder a las funciones establecidas de acuerdo mi rol</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Autenticación Segura de Supervisor.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Inicio de sesión exitoso<br/>
<ul>
<li><b>Given</b> que el usuario se encuentra en la pantalla de inicio de sesión de RiskGuard</li>
<li><b>When</b> ingresa su correo corporativo preconfigurado y su contraseña correcta,</li>
<li><b>And</b> hace clic en el botón "Ingresar",</li>
<li><b>Then</b> el sistema valida las credenciales,</li>
<li><b>And</b> autoriza el acceso y redirige al usuario a la vista principal en donde se encuentran sus funciones como supervisor</li>
</ul>
<b>Escenario 2:</b> Intento fallido por credenciales inválidas<br/>
<ul>
<li><b>Given</b> que el usuario se encuentra en la pantalla de inicio de sesión de RiskGuard</li>
<li><b>When</b> ingresa alguna credencial de manera incorrecta</li>
<li><b>And</b> hace clic en el botón "Ingresar",</li>
<li><b>Then</b> el sistema deniega el acceso a la plataforma,</li>
<li><b>And</b> muestra una mensaje indicando "Correo o contraseña incorrectos, intentelo nuevamente", manteniendo los campos limpios para un nuevo intento.</li>
</ul>
<b>Escenario 3:</b> Bloqueo preventivo por múltiples intentos fallidos consecutivos<br/>
<ul>
<li><b>Given</b> que el usuario intenta acceder al sistema,</li>
<li><b>When</b> acumula 5 intentos de autenticación fallidos consecutivos,</li>
<li><b>And</b> hace clic en el botón "Ingresar",</li>
<li><b>Then</b> el sistema bloquea temporalmente las peticiones para ese usuario,</li>
<li><b>And</b> muestra el mensaje indicando "Demasiados intentos fallidos. Por favor, intente nuevamente en 15 minutos".</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US25</b></td>
<td>Configuración de Sectores y Áreas Operativas</td>
<td>Como Supervisor de Seguridad, quiero administrar y gestionar los sectores fisicos de la planta, para georreferenciar correctamente las incidencias reportadas y organizar el catálogo de activos.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de Sectores y Áreas Operativas.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Registro exitoso de nuevo sector<br/>
<ul>
<li><b>Given</b> que el Supervisor se encuentra en el módulo de "Gestión de Sectores",</li>
<li><b>When</b> hace clic en "Nuevo Sector", ingresa un nombre en especifico y una descripción,</li>
<li><b>Then</b> el sistema registra el nuevo sector en la base de datos con estado "Activo",</li>
<li><b>And</b> actualiza la tabla de sectores mostrando el nuevo sector en la primera fila</li>
</ul>
<b>Escenario 2:</b> Validación de sector duplicado<br/>
<ul>
<li><b>Given</b> que el Supervisor se encuentra en el módulo de "Gestión de Sectores",</li>
<li><b>When</b> hace clic en "Nuevo Sector", ingresa un nombre en especifico y una descripción,</li>
<li><b>Then</b> el sistema bloquea la creación del registro,</li>
<li><b>And</b> muestra un mensaje indicando: "El nombre del área ya existe. Por favor, elija un nombre diferente"</li>
</ul>
<b>Escenario 3:</b> Desactivación de un área con historial<br/>
<ul>
<li><b>Given</b> que el Supervisor necesita retirar un sector que ya no se usa en la planta,</li>
<li><b>When</b> selecciona la opción "Desactivar" sobre el sector</li>
<li><b>Then</b> el sistema cambia el estado del sector a "Inactivo", conservando sus datos históricos de incidencias,</li>
<li><b>And</b> el sector aparece como "Inactivo" en la lista de sectores</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US26</b></td>
<td>Configuración y Gestión de Activos Industriales</td>
<td>Como Supervisor de Seguridad, quiero registrar y administrar la maquinaria y equipos de la planta, para vincularlos a su sector operativo correspondiente y permitir la asignación precisa de reportes de inspección a cada activo</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración y Gestión de Activos Industriales.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Registro exitoso de un activo vinculado a un sector<br/>
<ul>
<li><b>Given</b> que el supervisor cuenta con la información de una nueva maquinaria y tiene identificado el sector activo al cual asignara la maquinaria,</li>
<li><b>When</b> envía la solicitud de registro del activo con su respectivo código único,</li>
<li><b>Then</b> el sistema almacena el activo en la base de datos,</li>
<li><b>And</b> establece la relación referencial entre el activo y el sector especificado</li>
<li><b>And</b> muestra el activo en la lista de activos con estado "Activo"</li>
</ul>
<b>Escenario 2:</b> Validación por sector inactivo<br/>
<ul>
<li><b>Given</b> que un sector específico se encuentra con estado "Inactivo" en la base de datos,</li>
<li><b>When</b> el supervisor envía una solicitud para registrar o trasladar un activo hacia dicho sector,</li>
<li><b>Then</b> el sistema rechaza la operación,</li>
<li><b>And</b> retorna un error de validación indicando que el sector de destino no es válido para asignaciones</li>
</ul>
<b>Escenario 3:</b> Reubicación de un activo existente<br/>
<ul>
<li><b>Given</b> que un activo se encuentra registrado y asociado a un sector,</li>
<li><b>When</b> el supervisor envía una solicitud de actualización modificando la asociación hacia un sector,</li>
<li><b>Then</b> el sistema actualiza la ubicación del activo en los registros,</li>
<li><b>And</b> mantiene intacto el historial de reportes previos generados en su ubicación original</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US27</b></td>
<td>Gestión y Administración de Personal Técnico</td>
<td>Como Supervisor de Seguridad, quiero registrar y administrar al personal de mantenimiento en el sistema, para disponer de una lista actualizada de técnicos calificados a quienes delegar los tickets de acción correctiva</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Gestión y Administración de Personal Técnico.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Registro exitoso de un nuevo técnico<br/>
<ul>
<li><b>Given</b> que el supervisor dispone de los datos de un nuevo colaborador de mantenimiento,</li>
<li><b>When</b> envía la solicitud de registro con el número de documento, nombre y especialidad,</li>
<li><b>Then</b> el sistema almacena el perfil del técnico en la base de datos</li>
<li><b>And</b> le asigna el estado predeterminado de "Activo" para habilitar su disponibilidad en la asignación de tickets</li>
</ul>
<b>Escenario 2:</b> Validación por documento de identidad duplicado<br/>
<ul>
<li><b>Given</b> que un técnico ya se encuentra registrado activamente en la plataforma,</li>
<li><b>When</b> el supervisor intenta registrar un nuevo perfil utilizando el mismo número de documento de identidad,</li>
<li><b>Then</b> el sistema rechaza la solicitud de inserción,</li>
<li><b>And</b> retorna un mensaje de error validando la duplicidad del documento</li>
</ul>
<b>Escenario 3:</b> Inhabilitación de personal<br/>
<ul>
<li><b>Given</b> que un técnico registrado finaliza su vínculo laboral con la empresa y posee un historial de mitigación de riesgos,</li>
<li><b>When</b> el supervisor emite la solicitud para dar de baja dicho perfil,</li>
<li><b>Then</b> el sistema actualiza el estado del técnico a "Inactivo",</li>
<li><b>And</b> lo oculta de la lista de personal disponible para nuevas asignaciones, manteniendo intactos los registros de sus trabajos previos</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US28</b></td>
<td>Asignación de Tickets de Acción Correctiva</td>
<td>Como Supervisor de Seguridad, quiero asignar un ticket de incidente a un técnico de mantenimiento específico, para delegar la responsabilidad de la reparación y cambiar el estado de la alerta a un proceso de mitigación activo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Asignación de Tickets de Acción Correctiva.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Asignación inicial exitosa<br/>
<ul>
<li><b>Given</b> que existe un ticket de acción correctiva en estado "Pendiente",</li>
<li><b>When</b> el supervisor envía la solicitud de asignación vinculando a un técnico de mantenimiento en estado activo,</li>
<li><b>Then</b> el sistema procesa la vinculación en la base de datos</li>
<li><b>And</b> actualiza el estado del ticket a "En Progreso".</li>
</ul>
<b>Escenario 2:</b> Validación por datos incompletos<br/>
<ul>
<li><b>Given</b> que el supervisor intenta delegar la responsabilidad de un incidente,</li>
<li><b>When</b> envía la solicitud de asignación sin especificar el identificador de un técnico válido,</li>
<li><b>Then</b> el sistema rechaza la operación,</li>
<li><b>And</b> retorna un mensaje de error indicando que se requiere un responsable para continuar.</li>
</ul>
<b>Escenario 3:</b> Reasignación de ticket activo<br/>
<ul>
<li><b>Given</b> que un ticket se encuentra "En Progreso" asignado previamente a un técnico en específico,</li>
<li><b>When</b> el supervisor emite una nueva solicitud de asignación para el mismo ticket vinculando a un técnico diferente,</li>
<li><b>Then</b> el sistema actualiza al responsable activo de la tarea,</li>
<li><b>And</b> añade un registro en el historial detallando la transferencia de responsabilidad entre ambos técnicos.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US29</b></td>
<td>Exploración Sectorizada y Filtrado de Alertas Activas</td>
<td>Como Supervisor de Seguridad, quiero acceder a las alertas activas seleccionando previamente un sector específico, para enfocar mi análisis en un sector a la vez y aplicar filtros de riesgo sobre sus incidentes correspondientes.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Exploración Sectorizada y Filtrado de Alertas Activas.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Acceso a un sector con múltiples alertas<br/>
<ul>
<li><b>Given</b> que el supervisor necesita evaluar una zona específica de la planta,</li>
<li><b>When</b> selecciona un sector en especifico para su exploración,</li>
<li><b>Then</b> el sistema procesa la solicitud y retorna únicamente los tickets de incidentes asociados a dicho sector,</li>
<li><b>And</b> mantiene ocultas las alertas pertenecientes a otras áreas operativas</li>
</ul>
<b>Escenario 2:</b> Filtrado dentro de un sector específico<br/>
<ul>
<li><b>Given</b> que el sistema muestra todas las alertas correspondientes a un sector en especifico,</li>
<li><b>When</b> el supervisor aplica algun filtro secundario,</li>
<li><b>Then</b> el sistema filtra los resultados internos del sector</li>
<li><b>And</b> retorna exclusivamente los tickets basados en los filtros secundarios aplicados</li>
</ul>
<b>Escenario 3:</b> Exploración de un sector sin incidentes<br/>
<ul>
<li><b>Given</b> que el supervisor explora el estado operativo de un sector específico,</li>
<li><b>When</b> selecciona un sector el cual posee un historial reciente limpio,</li>
<li><b>Then</b> el sistema procesa la consulta sin retornar tickets de incidentes,</li>
<li><b>And</b> emite el mensaje informativo indicando que el sector opera dentro de los parámetros seguros y no posee alertas activas</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US30</b></td>
<td>Verificación y Cierre de Medidas de Control</td>
<td>Como Supervisor de Seguridad, quiero evaluar la efectividad de las medidas correctivas implementadas, para garantizar que el riesgo ha sido mitigado satisfactoriamente antes de proceder al cierre definitivo del incidente en el sistema</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Verificación y Cierre de Medidas de Control.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Aprobación de medida y cierre de ticket<br/>
<ul>
<li><b>Given</b> que un ticket de acción correctiva se encuentra en estado "Medida Implementada",</li>
<li><b>When</b> el supervisor emite un veredicto de aprobación tras la inspección del riesgo,</li>
<li><b>Then</b> el sistema registra el cierre definitivo del ticket,</li>
<li><b>And</b> procede a la actualización del nivel de riesgo del sector correspondiente en la base de datos</li>
</ul>
<b>Escenario 2:</b> Rechazo de medida por persistencia de riesgo<br/>
<ul>
<li><b>Given</b> que el supervisor inspecciona una medida de control implementada y determina que la falla persiste,</li>
<li><b>When</b> envía un veredicto de rechazo junto con la justificación técnica del hallazgo,</li>
<li><b>Then</b> el sistema cambia el estado del ticket nuevamente a "En Progreso",</li>
</ul>
<b>Escenario 3:</b> Validación de datos obligatorios en el rechazo<br/>
<ul>
<li><b>Given</b> que el supervisor decide rechazar una medida de control implementada,</li>
<li><b>When</b> intenta procesar el veredicto de rechazo sin registrar el comentario de justificación,</li>
<li><b>Then</b> el sistema impide la actualización del estado del ticket,</li>
<li><b>And</b> emite una mensaje indicando que debe ingresar una justificación del motivo del rechazo.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>
<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US31</b></td>
<td>Visualización del Mapa de Calor Operativo</td>
<td>Como Supervisor de Seguridad, quiero visualizar la distribución de los niveles de riesgo de los sectores de la planta, para identificar de forma inmediata qué sectores requieren intervención prioritaria</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización del Mapa de Calor Operativo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Identificación de sector en estado crítico<br/>
<ul>
<li><b>Given</b> que el motor predictivo registra un nuevo incidente que supera el umbral de criticidad máxima en un sector específico,</li>
<li><b>When</b> el supervisor solicita la visualización del mapa de calor operativo,</li>
<li><b>Then</b> el sistema procesa la clasificación de riesgo actualizada,</li>
<li><b>And</b> expone el sector afectado con el indicador de estado de máxima alerta.</li>
</ul>
<b>Escenario 2:</b> Exploración de contexto desde el mapa<br/>
<ul>
<li><b>Given</b> que un sector específico presenta un indicador de riesgo activo en el mapa de calor,</li>
<li><b>When</b> el supervisor emite la solicitud de selección sobre dicho sector,</li>
<li><b>Then</b> el sistema recupera la información de la base de datos,</li>
<li><b>And</b> expone los datos de los incidentes que justifican el estado de alerta de la zona</li>
</ul>
<b>Escenario 3:</b> Normalización del estado del sector<br/>
<ul>
<li><b>Given</b> que un sector se encuentra en estado de alerta debido a un ticket de incidente activo,</li>
<li><b>When</b> el sistema registra el cierre definitivo de dicho ticket y no existen otras alertas pendientes en la zona,</li>
<li><b>Then</b> el sistema recalcula el estado general del sector,</li>
<li><b>And</b> actualiza el indicador hacia un estado de riesgo tolerable o normal.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US32</b></td>
<td>Notificación Externa Automática por Incidentes Críticos</td>
<td>Como Supervisor de Seguridad, quiero recibir notificaciones automáticas a través de canales externos cuando el sistema registre un incidente de riesgo crítico, para garantizar un tiempo de respuesta inmediato ante emergencias sin requerir un monitoreo activo de la plataforma</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Notificación Externa Automática por Incidentes Críticos.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Emisión exitosa de alerta por riesgo crítico<br/>
<ul>
<li><b>Given</b> que se registra un nuevo incidente que supera el umbral máximo de peligro,</li>
<li><b>When</b> el sistema genera formalmente el ticket de acción correctiva,</li>
<li><b>Then</b> el sistema extrae los datos principales del incidente,</li>
<li><b>And</b> envía un mensaje de correo electrónico al supervisor registrado indicando la existencia de la emergencia.</li>
</ul>
<b>Escenario 2:</b> Omisión de notificación por riesgo operativo<br/>
<ul>
<li><b>Given</b> que el sistema evalúa un reporte de incidencia,</li>
<li><b>When</b> el sistema registra el evento con un nivel de riesgo inferior al umbral de criticidad,</li>
<li><b>Then</b> el sistema almacena el incidente para su revisión en la plataforma,</li>
<li><b>And</b> omite el disparo del evento de notificación hacia el correo electrónico externo del supervisor.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US33</b></td>
<td>Escalamiento Automático por Incumplimiento de SLA</td>
<td>Como Supervisor de Seguridad, quiero que el sistema escale automáticamente los tickets de incidentes que superen su tiempo máximo de resolución permitido (SLA), para alertar a la gerencia sobre posibles negligencias operativas y evitar la materialización de accidentes graves</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Escalamiento Automático por Incumplimiento de SLA.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Incumplimiento de SLA en incidente crítico<br/>
<ul>
<li><b>Given</b> que un ticket de nivel "Crítico" se encuentra "En Progreso" y se acerca a su límite de tiempo permitido (SLA),</li>
<li><b>When</b> el reloj del sistema determina que el tiempo transcurrido ha superado el umbral máximo sin registrar un cierre,</li>
<li><b>Then</b> el sistema actualiza la prioridad del ticket a "SLA Incumplido" o "Escalado",</li>
<li><b>And</b> envía la notificación de alerta a la gerencia reportando la demora en la mitigación.</li>
</ul>
<b>Escenario 2:</b> Resolución dentro del tiempo permitido<br/>
<ul>
<li><b>Given</b> que un técnico se encuentra mitigando un incidente con un SLA activo,</li>
<li><b>When</b> el supervisor aprueba la medida de control y el ticket pasa a estado "Cerrado" antes de vencer el límite de tiempo,</li>
<li><b>Then</b> el sistema detiene el contador de SLA para dicho ticket,</li>
<li><b>And</b> omite cualquier protocolo de escalamiento o notificación gerencial.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US34</b></td>
<td>Programación de Mantenimiento Preventivo de Activos</td>
<td>Como Supervisor de Seguridad, quiero programar tickets de mantenimiento preventivo sobre máquinas específicas independientes de su nivel de riesgo actual, para aislar temporalmente el activo y realizar revisiones periódicas que eviten fallas críticas futuras</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Programación de Mantenimiento Preventivo de Activos.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Programación exitosa sobre una máquina<br/>
<ul>
<li><b>Given</b> que un activo industrial opera con un nivel de riesgo tolerable y requiere una revisión de rutina,</li>
<li><b>When</b> el supervisor envía el formulario de mantenimiento asignando una fecha futura y un técnico responsable,</li>
<li><b>Then</b> el sistema registra el ticket preventivo,</li>
<li><b>And</b> lo mantiene en estado de espera hasta alcanzar la fecha programada.</li>
</ul>
<b>Escenario 2:</b> Clausura temporal del activo<br/>
<ul>
<li><b>Given</b> que un ticket de mantenimiento preventivo ha alcanzado su fecha y hora programada de ejecución,</li>
<li><b>When</b> el sistema actualiza el estado del ticket a "En Progreso",</li>
<li><b>Then</b> el sistema cambia simultáneamente el estado del activo industrial a "En Mantenimiento",</li>
<li><b>And</b> aísla el equipo temporalmente para evitar que el motor predictivo genere alertas de inoperatividad sobre esa máquina.</li>
</ul>
<b>Escenario 3:</b> Reactivación tras el cierre del mantenimiento<br/>
<ul>
<li><b>Given</b> que un técnico ha culminado las labores de rutina sobre una máquina clausurada temporalmente,</li>
<li><b>When</b> el supervisor registra la verificación y el cierre definitivo del ticket preventivo,</li>
<li><b>Then</b> el sistema actualiza el estado del activo devolviéndolo a operativo,</li>
<li><b>And</b> rehabilita la generación de alertas sobre el equipo.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US35</b></td>
<td>Generación y Exportación de Reportes de Cumplimiento</td>
<td>Como Supervisor de Seguridad, quiero generar y exportar reportes consolidados sobre el historial de incidentes y el rendimiento operativo, para documentar el cumplimiento normativo de la planta y sustentar la toma de decisiones gerenciales</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Generación y Exportación de Reportes de Cumplimiento.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Generación exitosa de reporte global<br/>
<ul>
<li><b>Given</b> que el supervisor necesita el consolidado de incidentes de un intervalo de fechas en especifico,</li>
<li><b>When</b> envía la solicitud de generación ingresando el rango de fechas correspondiente sin aplicar filtros de sector,</li>
<li><b>Then</b> el sistema extrae la data histórica de toda la planta desde la base de datos</li>
<li><b>And</b> compila y retorna un archivo descargable con las métricas operativas.</li>
</ul>
<b>Escenario 2:</b> Validación de consistencia en el rango de fechas<br/>
<ul>
<li><b>Given</b> que el supervisor configura los parámetros para la extracción de un reporte,</li>
<li><b>When</b> ingresa una fecha de inicio que es lógicamente posterior a la fecha de fin de la consulta,</li>
<li><b>Then</b> el sistema rechaza la ejecución del cálculo,</li>
<li><b>And</b> emite un mensaje de error indicando que el rango temporal estructurado es inválido.</li>
</ul>
<b>Escenario 3:</b> Generación de reporte filtrado por sector crítico<br/>
<ul>
<li><b>Given</b> que la gerencia solicita una auditoría específica sobre el área operativa más vulnerable,</li>
<li><b>When</b> el supervisor ejecuta la generación del reporte aplicando el filtro secundario de un sector físico específico</li>
<li><b>Then</b> el sistema extrae los registros correspondientes,</li>
<li><b>And</b> exporta un documento que contiene exclusivamente el historial de tickets y mantenimientos asociados a dicha ubicación.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US36</b></td>
<td>Autenticación Segura de Gerente o Administrador</td>
<td>Como usuario, quiero iniciar sesión en RiskGuard con mis credenciales preconfiguradas, para acceder al dashboard ejecutivo y a las funciones correspondientes a mi rol de alta dirección.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Autenticación Segura de Gerente o Administrador.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Inicio de sesión exitoso<br/>
<ul>
<li><b>Given</b> que el usuario se encuentra en la pantalla de inicio de sesión,</li>
<li><b>When</b> ingresa su correo y contraseña correctos y hace clic en "Ingresar",</li>
<li><b>Then</b> el sistema valida las credenciales,</li>
<li><b>And</b> redirige al gerente a su dashboard ejecutivo.</li>
</ul>
<b>Escenario 2:</b> Credenciales inválidas<br/>
<ul>
<li><b>Given</b> que el usuario se encuentra en la pantalla de inicio de sesión,</li>
<li><b>When</b> ingresa alguna credencial incorrecta y hace clic en "Ingresar",</li>
<li><b>Then</b> el sistema deniega el acceso,</li>
<li><b>And</b> muestra el mensaje "Correo o contraseña incorrectos".</li>
</ul>
<b>Escenario 3:</b> Bloqueo por intentos fallidos<br/>
<ul>
<li><b>Given</b> que el usuario acumula 5 intentos fallidos consecutivos,</li>
<li><b>When</b> intenta ingresar nuevamente,</li>
<li><b>Then</b> el sistema bloquea la cuenta temporalmente,</li>
<li><b>And</b> muestra el mensaje "Demasiados intentos fallidos. Intente en 15 minutos".</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US37</b></td>
<td>Visualización del Dashboard Ejecutivo de Seguridad</td>
<td>Como Gerente, quiero ver un dashboard ejecutivo con los indicadores clave de seguridad de la planta al ingresar a la plataforma, para tener una visión consolidada del estado de la SST sin necesidad de bajar al campo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización del Dashboard Ejecutivo de Seguridad.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Dashboard con incidentes activos<br/>
<ul>
<li><b>Given</b> que el Gerente inicia sesión en la plataforma,</li>
<li><b>When</b> el sistema carga su dashboard ejecutivo,</li>
<li><b>Then</b> muestra todos los indicadores clave con su estado actual,</li>
<li><b>And</b> los sectores críticos aparecen resaltados en rojo.</li>
</ul>
<b>Escenario 2:</b> Dashboard sin incidentes activos<br/>
<ul>
<li><b>Given</b> que el Gerente ingresa al dashboard y no existen incidentes activos,</li>
<li><b>When</b> el sistema carga los indicadores,</li>
<li><b>Then</b> todos los indicadores aparecen en verde,</li>
<li><b>And</b> muestra el mensaje "La planta opera dentro de los parámetros seguros".</li>
</ul>
<b>Escenario 3:</b> Acceso al detalle de un indicador<br/>
<ul>
<li><b>Given</b> que el Gerente visualiza el dashboard ejecutivo,</li>
<li><b>When</b> hace clic sobre el indicador de "Sectores en estado crítico",</li>
<li><b>Then</b> el sistema muestra el listado de sectores con sus alertas activas,</li>
<li><b>And</b> el gerente puede volver al dashboard con un solo clic.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US38</b></td>
<td>Visualización de Tendencias de Accidentabilidad</td>
<td>Como Gerente, quiero ver gráficas de tendencia de incidentes y accidentes por mes, para identificar si la accidentabilidad de la planta está mejorando o empeorando y tomar decisiones estratégicas a tiempo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de Tendencias de Accidentabilidad.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Visualización de tendencia global<br/>
<ul>
<li><b>Given</b> que el Gerente accede a la sección de tendencias,</li>
<li><b>When</b> el sistema carga la gráfica,</li>
<li><b>Then</b> muestra la evolución mensual diferenciada por tipo de incidente,</li>
</ul>
<b>Escenario 2:</b> Filtrado por sector<br/>
<ul>
<li><b>Given</b> que el Gerente visualiza la gráfica de tendencias global,</li>
<li><b>When</b> selecciona un sector específico del filtro,</li>
<li><b>Then</b> el sistema actualiza la gráfica mostrando solo los datos de ese sector,</li>
<li><b>And</b> el título de la gráfica refleja el sector seleccionado.</li>
</ul>
<b>Escenario 3:</b> Exportar gráfica<br/>
<ul>
<li><b>Given</b> que el Gerente visualiza una gráfica de tendencias,</li>
<li><b>When</b> hace clic en "Exportar imagen",</li>
<li><b>Then</b> el sistema descarga la gráfica en formato PNG,</li>
<li><b>And</b> el archivo incluye el rango de fechas.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US39</b></td>
<td>Exportación de Formatos de Auditoría para SUNAFIL</td>
<td>Como Gerente, quiero exportar automáticamente los formatos de auditoría exigidos por la Ley N° 29783 con los datos reales del sistema, para prepararme ante inspecciones de SUNAFIL sin depender de reportes manuales tardíos o incompletos.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Exportación de Formatos de Auditoría para SUNAFIL.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Exportación exitosa en PDF<br/>
<ul>
<li><b>Given</b> que el Gerente accede a la sección de exportación de auditoría,</li>
<li><b>When</b> selecciona un rango de fechas válido y el formato PDF,</li>
<li><b>Then</b> el sistema genera el documento con los datos del período,</li>
<li><b>And</b> lo descarga automáticamente en el dispositivo del gerente.</li>
</ul>
<b>Escenario 2:</b> Rango sin datos registrados<br/>
<ul>
<li><b>Given</b> que el Gerente selecciona un rango de fechas sin incidentes registrados,</li>
<li><b>When</b> hace clic en "Generar reporte",</li>
<li><b>Then</b> el sistema muestra el mensaje "No hay datos registrados para el período seleccionado",</li>
<li><b>And</b> no genera ningún archivo de descarga.</li>
</ul>
<b>Escenario 3:</b> Exportación en Excel<br/>
<ul>
<li><b>Given</b> que el Gerente prefiere el formato Excel para análisis posterior,</li>
<li><b>When</b> selecciona el formato Excel y hace clic en "Generar reporte",</li>
<li><b>Then</b> el sistema genera el archivo con los datos estructurados en columnas,</li>
<li><b>And</b> lo descarga con el nombre correspondiente al período seleccionado.</li>
</ul>
<b>Escenario 4:</b> Consulta y re-descarga desde el historial<br/>
<ul>
<li><b>Given</b> que el Gerente accede a la sección "Mis Reportes",</li>
<li><b>When</b> aplica filtros por mes, año o tipo para localizar un reporte de auditoría previo,</li>
<li><b>Then</b> el sistema muestra la lista de reportes que cumplen el filtro,</li>
<li><b>And</b> el gerente puede hacer clic en el ícono de descarga para volver a obtener el archivo o en el ícono de vista previa para previsualizar el PDF.</li>
</ul>
<b>Escenario 5:</b> Eliminación de reporte del historial<br/>
<ul>
<li><b>Given</b> que el Gerente visualiza el historial de reportes generados,</li>
<li><b>When</b> hace clic en el ícono de eliminar sobre un reporte,</li>
<li><b>Then</b> el sistema solicita confirmación antes de proceder,</li>
<li><b>And</b> al confirmar, elimina el registro del historial sin recargar la página.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US40</b></td>
<td>Seguimiento del Cumplimiento del Plan Anual de SST</td>
<td>Como Gerente, quiero ver el porcentaje de cumplimiento del plan anual de Seguridad y Salud en el Trabajo en tiempo real, para detectar brechas de ejecución antes de que se conviertan en observaciones durante una inspección de SUNAFIL.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Seguimiento del Cumplimiento del Plan Anual de SST.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Cumplimiento en nivel aceptable<br/>
<ul>
<li><b>Given</b> que el Gerente accede al indicador de cumplimiento del plan anual,</li>
<li><b>When</b> el sistema calcula el porcentaje actual,</li>
<li><b>Then</b> muestra el indicador en verde si es igual o mayor al 80%,</li>
<li><b>And</b> no genera ninguna alerta de desviación.</li>
</ul>
<b>Escenario 2:</b> Cumplimiento crítico con alerta<br/>
<ul>
<li><b>Given</b> que el cumplimiento del plan cae por debajo del 50%,</li>
<li><b>When</b> el sistema recalcula el indicador,</li>
<li><b>Then</b> muestra el indicador en rojo en el dashboard ejecutivo,</li>
<li><b>And</b> genera una alerta con el mensaje "El cumplimiento del plan de SST está por debajo del umbral mínimo".</li>
</ul>
<b>Escenario 3:</b> Detalle por sector<br/>
<ul>
<li><b>Given</b> que el Gerente quiere identificar qué sector tiene mayor brecha,</li>
<li><b>When</b> hace clic sobre el indicador de cumplimiento,</li>
<li><b>Then</b> el sistema muestra el porcentaje de cumplimiento desglosado por sector,</li>
<li><b>And</b> ordena los sectores de menor a mayor cumplimiento.</li>
</ul>
<b>Escenario 4:</b> Evolución mensual del cumplimiento<br/>
<ul>
<li><b>Given</b> que el Gerente visualiza la sección de cumplimiento mensual,</li>
<li><b>When</b> el sistema procesa el campo monthly_compliance del plan anual,</li>
<li><b>Then</b> muestra una gráfica de línea con el porcentaje de cumplimiento por cada mes del año,</li>
<li><b>And</b> el gerente puede identificar visualmente los meses con mayor y menor cumplimiento.</li>
</ul>
<b>Escenario 5:</b> Generar reporte de cumplimiento SST<br/>
<ul>
<li><b>Given</b> que el Gerente accede al formulario "Generar Reporte" y selecciona el tipo "Cumplimiento",           </li>
<li><b>When</b> elige el formato (PDF o Excel) y hace clic en "Generar",</li>
<li><b>Then</b> el sistema genera y descarga el reporte con el porcentaje de cumplimiento global, actividades             completadas y desglose por sector,</li>
<li><b>And</b> registra el reporte en el historial de reportes generados.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US41</b></td>
<td>Visualización de Indicadores Predictivos de Riesgo</td>
<td>Como Gerente, quiero ver indicadores predictivos que anticipen posibles accidentes en la planta antes de que ocurran, para justificar inversiones preventivas ante el directorio con datos concretos y no solo registros reactivos.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de Indicadores Predictivos de Riesgo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Indicadores con proyección de riesgo alto<br/>
<ul>
<li><b>Given</b> que el Gerente accede a la sección de indicadores predictivos,</li>
<li><b>When</b> el motor de reglas detecta un sector con tendencia creciente de incidentes,</li>
<li><b>Then</b> el sistema resalta ese sector como zona de atención prioritaria,</li>
<li><b>And</b> muestra la proyección de riesgo con su descripción interpretativa.</li>
</ul>
<b>Escenario 2:</b> Sin sectores con tendencia creciente<br/>
<ul>
<li><b>Given</b> que en los últimos 30 días no existe ningún sector con tendencia creciente de incidentes,</li>
<li><b>When</b> el sistema calcula los indicadores predictivos,</li>
<li><b>Then</b> muestra el mensaje "No se detectaron tendencias de riesgo creciente en el período consultado".</li>
</ul>
<b>Escenario 3:</b> Exportar resumen ejecutivo predictivo<br/>
<ul>
<li><b>Given</b> que el Gerente necesita presentar los indicadores al directorio,</li>
<li><b>When</b> hace clic en "Exportar resumen ejecutivo",</li>
<li><b>Then</b> el sistema genera un PDF con los indicadores predictivos y su interpretación,</li>
<li><b>And</b> lo descarga con el nombre "RiskGuard_Resumen_Ejecutivo_[fecha].pdf".</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US42</b></td>
<td>Notificación de Alerta Crítica No Resuelta a Gerencia</td>
<td>Como Gerente, quiero recibir una notificación cuando un riesgo crítico lleve más de 48 horas sin ser resuelto por el supervisor, para escalar el problema internamente y evitar sanciones legales o paradas de planta.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Notificación de Alerta Crítica No Resuelta a Gerencia.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Notificación de escalamiento enviada<br/>
<ul>
<li><b>Given</b> que existe un riesgo crítico sin resolución por más de 48 horas,</li>
<li><b>When</b> el sistema evalúa los riesgos activos pendientes,</li>
<li><b>Then</b> el Gerente recibe una notificación en su centro de notificaciones,</li>
<li><b>And</b> la notificación detalla el sector, tipo de riesgo, horas transcurridas y supervisor responsable.</li>
</ul>
<b>Escenario 2:</b> Sin notificación cuando el riesgo fue resuelto a tiempo<br/>
<ul>
<li><b>Given</b> que un riesgo crítico fue resuelto antes de las 48 horas,</li>
<li><b>When</b> el sistema evalúa los riesgos activos,</li>
<li><b>Then</b> el sistema no genera ninguna notificación de escalamiento al gerente.</li>
</ul>
<b>Escenario 3:</b> Acceso al ticket desde la notificación<br/>
<ul>
<li><b>Given</b> que el Gerente recibe una notificación de escalamiento,</li>
<li><b>When</b> hace clic sobre la notificación,</li>
<li><b>Then</b> el sistema lo redirige al detalle del ticket crítico sin resolver,</li>
<li><b>And</b> puede ver el historial completo del ticket incluyendo el supervisor asignado.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US43</b></td>
<td>Registro Histórico de Incidentes para Trazabilidad Legal</td>
<td>Como Gerente, quiero acceder al historial completo e inmutable de todos los incidentes registrados en la plataforma, para contar con evidencia documentada ante auditorías de SUNAFIL o procesos legales derivados de accidentes laborales.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Registro Histórico de Incidentes para Trazabilidad Legal.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Consulta del historial completo<br/>
<ul>
<li><b>Given</b> que el Gerente accede a la sección de historial de incidentes,</li>
<li><b>When</b> el sistema carga los registros,</li>
<li><b>Then</b> muestra todos los incidentes ordenados del más reciente al más antiguo,</li>
<li><b>And</b> cada registro muestra: fecha, sector, tipo, criticidad y estado final.</li>
</ul>
<b>Escenario 2:</b> Filtrado del historial<br/>
<ul>
<li><b>Given</b> que el Gerente necesita revisar los incidentes de un sector específico en un período concreto,</li>
<li><b>When</b> aplica los filtros de sector y rango de fechas,</li>
<li><b>Then</b> el sistema muestra únicamente los registros que cumplen ambos criterios,</li>
<li><b>And</b> actualiza el contador total de resultados filtrados.</li>
</ul>
<b>Escenario 3:</b> Intento de modificar un registro histórico<br/>
<ul>
<li><b>Given</b> que el Gerente visualiza el detalle de un incidente cerrado,</li>
<li><b>When</b> intenta editar cualquier campo del registro,</li>
<li><b>Then</b> el sistema no habilita ningún campo de edición,</li>
<li><b>And</b> muestra el mensaje "Los registros históricos son de solo lectura".</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US44</b></td>
<td>Gestión de Cuentas de Usuario desde Administración</td>
<td>Como Administrador, quiero crear, editar y desactivar cuentas de usuario para operarios, supervisores y otros gerentes, para mantener el control de acceso a la plataforma y asegurar que solo el personal autorizado pueda ingresar.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Gestión de Cuentas de Usuario desde Administración.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Creación exitosa de cuenta<br/>
<ul>
<li><b>Given</b> que el Administrador accede al módulo de gestión de usuarios,</li>
<li><b>When</b> completa el formulario con los datos del nuevo usuario y hace clic en "Crear cuenta",</li>
<li><b>Then</b> el sistema registra la cuenta en la base de datos,</li>
<li><b>And</b> muestra la contraseña temporal generada para su entrega al usuario.</li>
</ul>
<b>Escenario 2:</b> Correo ya registrado<br/>
<ul>
<li><b>Given</b> que el Administrador intenta crear una cuenta con un correo ya existente,</li>
<li><b>When</b> hace clic en "Crear cuenta",</li>
<li><b>Then</b> el sistema bloquea el registro,</li>
<li><b>And</b> muestra el mensaje "El correo ingresado ya está registrado en el sistema".</li>
</ul>
<b>Escenario 3:</b> Desactivación de cuenta<br/>
<ul>
<li><b>Given</b> que el Administrador necesita retirar el acceso a un usuario,</li>
<li><b>When</b> selecciona la opción "Desactivar" sobre la cuenta,</li>
<li><b>Then</b> el sistema cambia el estado de la cuenta a "Inactiva",</li>
<li><b>And</b> el usuario no puede iniciar sesión desde ese momento, conservando su historial de actividad.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---
<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US45</b></td>
<td>Generación de Reporte Mensual de Gestión de SST</td>
<td>Como Gerente, quiero generar un reporte mensual consolidado de la gestión de seguridad con un solo clic, para reducir el tiempo dedicado a elaborar informes manuales y tener siempre datos actualizados para presentar al directorio.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Generación de Reporte Mensual de Gestión de SST.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Generación exitosa del reporte mensual<br/>
<ul>
<li><b>Given</b> que el Gerente accede a la sección de nuevo reporte,</li>
<li><b>When</b> selecciona el mes y año y hace clic en "Generar reporte",</li>
<li><b>Then</b> el sistema genera el PDF con los datos consolidados del período con jsPDF,</li>
<li><b>And</b> lo descarga automáticamente y registra el reporte en el historial.</li>
</ul>
<b>Escenario 2:</b> Mes sin datos suficientes<br/>
<ul>
<li><b>Given</b> que el Gerente selecciona un mes sin incidentes registrados,</li>
<li><b>When</b> hace clic en "Generar reporte",</li>
<li><b>Then</b> el sistema muestra el mensaje "No hay datos registrados para el período seleccionado",</li>
<li><b>And</b> no genera ningún archivo ni registra el reporte en el historial.</li>
</ul>
<b>Escenario 3:</b> Previsualización de reporte mensual desde el historial<br/>
<ul>
<li><b>Given</b> que el Gerente accede al historial de reportes y localiza un reporte mensual previo,</li>
<li><b>When</b> hace clic en el ícono de vista previa,</li>
<li><b>Then</b> el sistema muestra el PDF en un panel emergente dentro de la misma pantalla,</li>
<li><b>And</b> el gerente puede cerrarlo o descargarlo directamente desde el panel.</li>
</ul>
<b>Escenario 4:</b> Eliminación de reporte mensual del historial<br/>
<ul>
<li><b>Given</b> que el Gerente visualiza el historial de reportes mensuales generados,</li>
<li><b>When</b> hace clic en el ícono de eliminar sobre un reporte,</li>
<li><b>Then</b> el sistema solicita confirmación antes de proceder,</li>
<li><b>And</b> al confirmar, elimina el registro del historial sin recargar la página.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>
---
<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US46</b></td>
<td>Configuración de niveles de riesgo</td>
<td>Como administrador, quiero definir los niveles de riesgo del sistema, para clasificar correctamente los incidentes detectados.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de niveles de riesgo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Creación de nivel de riesgo<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de configuración,</li>
<li><b>When</b> registra un nuevo nivel de riesgo y hace clic en "Guardar",</li>
<li><b>Then</b> el sistema valida los datos ingresados,</li>
<li><b>And</b> guarda el nuevo nivel correctamente.</li>
</ul>
<b>Escenario 2:</b> Edición de nivel de riesgo<br/>
<ul>
<li><b>Given</b> que existen niveles de riesgo registrados,</li>
<li><b>When</b> el administrador modifica un nivel existente,</li>
<li><b>Then</b> el sistema guarda los cambios correctamente,</li>
<li><b>And</b> actualiza la información en el sistema.</li>
</ul>
<b>Escenario 3:</b> Validación de duplicados<br/>
<ul>
<li><b>Given</b> que el administrador intenta crear un nivel con nombre repetido,</li>
<li><b>When</b> hace clic en "Guardar",</li>
<li><b>Then</b> el sistema rechaza la operación,</li>
<li><b>And</b> muestra el mensaje "El nivel de riesgo ya existe".</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US47</b></td>
<td>Configuración de umbrales de alerta</td>
<td>Como administrador, quiero definir los umbrales de alerta del sistema, para que se generen notificaciones cuando se superen ciertos valores.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de umbrales de alerta.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Configuración de umbral válida<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de configuración,</li>
<li><b>When</b> ingresa un valor válido de umbral y hace clic en "Guardar",</li>
<li><b>Then</b> el sistema valida el valor ingresado,</li>
<li><b>And</b> guarda la configuración correctamente.</li>
</ul>
<b>Escenario 2:</b> Ingreso de valor inválido<br/>
<ul>
<li><b>Given</b> que el administrador se encuentra configurando umbrales,</li>
<li><b>When</b> ingresa un valor negativo o inválido,</li>
<li><b>Then</b> el sistema rechaza el valor,</li>
<li><b>And</b> muestra un mensaje de error.</li>
</ul>
<b>Escenario 3:</b> Edición de umbral<br/>
<ul>
<li><b>Given</b> que existen umbrales previamente configurados,</li>
<li><b>When</b> el administrador modifica un umbral existente,</li>
<li><b>Then</b> el sistema guarda los cambios,</li>
<li><b>And</b> actualiza la configuración en el sistema.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US48</b></td>
<td>Configuración de reglas de alertas</td>
<td>Como administrador, quiero configurar reglas de generación de alertas, para adaptar el comportamiento del sistema a distintos escenarios operativos.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de reglas de alertas.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Creación de regla de alerta<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de reglas,</li>
<li><b>When</b> define una nueva regla con condiciones específicas y hace clic en "Guardar",</li>
<li><b>Then</b> el sistema valida los datos ingresados,</li>
<li><b>And</b> registra la regla correctamente.</li>
</ul>
<b>Escenario 2:</b> Edición de regla existente<br/>
<ul>
<li><b>Given</b> que existen reglas previamente configuradas,</li>
<li><b>When</b> el administrador modifica una regla,</li>
<li><b>Then</b> el sistema guarda los cambios,</li>
<li><b>And</b> actualiza la configuración.</li>
</ul>
<b>Escenario 3:</b> Eliminación de regla<br/>
<ul>
<li><b>Given</b> que el administrador selecciona una regla existente,</li>
<li><b>When</b> hace clic en "Eliminar",</li>
<li><b>Then</b> el sistema solicita confirmación,</li>
<li><b>And</b> elimina la regla del sistema.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US49</b></td>
<td>Activación y desactivación de módulos del sistema</td>
<td>Como administrador, quiero activar o desactivar módulos del sistema, para personalizar su funcionamiento según las necesidades de la organización.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Activación y desactivación de módulos del sistema.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Activación de módulo<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de configuración,</li>
<li><b>When</b> selecciona un módulo inactivo y hace clic en "Activar",</li>
<li><b>Then</b> el sistema cambia el estado del módulo a activo,</li>
<li><b>And</b> habilita sus funcionalidades.</li>
</ul>
<b>Escenario 2:</b> Desactivación de módulo<br/>
<ul>
<li><b>Given</b> que existe un módulo activo,</li>
<li><b>When</b> el administrador hace clic en "Desactivar",</li>
<li><b>Then</b> el sistema cambia su estado a inactivo,</li>
<li><b>And</b> deshabilita sus funcionalidades.</li>
</ul>
<b>Escenario 3:</b> Persistencia de cambios<br/>
<ul>
<li><b>Given</b> que el administrador realiza cambios en los módulos,</li>
<li><b>When</b> guarda la configuración,</li>
<li><b>Then</b> el sistema almacena los cambios correctamente,</li>
<li><b>And</b> mantiene el estado actualizado.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US50</b></td>
<td>Configuración de horarios operativos</td>
<td>Como administrador, quiero configurar los horarios de operación del sistema, para adaptarlo a los turnos y jornadas laborales de la planta.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de horarios operativos.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Configuración de horario válido<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de horarios,</li>
<li><b>When</b> define un horario con hora de inicio y fin válidas y hace clic en "Guardar",</li>
<li><b>Then</b> el sistema valida los datos,</li>
<li><b>And</b> registra el horario correctamente.</li>
</ul>
<b>Escenario 2:</b> Validación de formato incorrecto<br/>
<ul>
<li><b>Given</b> que el administrador ingresa un formato de hora inválido,</li>
<li><b>When</b> intenta guardar la configuración,</li>
<li><b>Then</b> el sistema rechaza el registro,</li>
<li><b>And</b> muestra un mensaje de error.</li>
</ul>
<b>Escenario 3:</b> Edición de horario<br/>
<ul>
<li><b>Given</b> que existen horarios configurados,</li>
<li><b>When</b> el administrador modifica un horario existente,</li>
<li><b>Then</b> el sistema guarda los cambios,</li>
<li><b>And</b> actualiza la información.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US51</b></td>
<td>Registro de dispositivos</td>
<td>Como administrador, quiero registrar dispositivos (sensores o cámaras), para integrarlos al sistema de monitoreo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Registro de dispositivos.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Registro exitoso de dispositivo<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de dispositivos,</li>
<li><b>When</b> ingresa los datos del dispositivo y hace clic en "Registrar",</li>
<li><b>Then</b> el sistema valida la información,</li>
<li><b>And</b> registra el dispositivo correctamente.</li>
</ul>
<b>Escenario 2:</b> Campos incompletos<br/>
<ul>
<li><b>Given</b> que el administrador deja campos obligatorios vacíos,</li>
<li><b>When</b> intenta registrar el dispositivo,</li>
<li><b>Then</b> el sistema rechaza el registro,</li>
<li><b>And</b> muestra un mensaje de error indicando los campos faltantes.</li>
</ul>
<b>Escenario 3:</b> Registro duplicado<br/>
<ul>
<li><b>Given</b> que ya existe un dispositivo registrado con los mismos datos,</li>
<li><b>When</b> el administrador intenta registrarlo nuevamente,</li>
<li><b>Then</b> el sistema bloquea la acción,</li>
<li><b>And</b> muestra el mensaje "El dispositivo ya existe".</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US52</b></td>
<td>Edición de dispositivos</td>
<td>Como administrador, quiero editar la información de los dispositivos registrados, para mantener actualizados sus datos dentro del sistema.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Edición de dispositivos.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Edición exitosa de dispositivo<br/>
<ul>
<li><b>Given</b> que el administrador accede a la lista de dispositivos,</li>
<li><b>When</b> selecciona un dispositivo, modifica sus datos y hace clic en "Guardar",</li>
<li><b>Then</b> el sistema valida la información,</li>
<li><b>And</b> actualiza el dispositivo correctamente.</li>
</ul>
<b>Escenario 2:</b> Campos inválidos<br/>
<ul>
<li><b>Given</b> que el administrador ingresa datos incompletos o inválidos,</li>
<li><b>When</b> intenta guardar los cambios,</li>
<li><b>Then</b> el sistema rechaza la operación,</li>
<li><b>And</b> muestra un mensaje de error.</li>
</ul>
<b>Escenario 3:</b> Cancelación de edición<br/>
<ul>
<li><b>Given</b> que el administrador está editando un dispositivo,</li>
<li><b>When</b> decide cancelar la operación,</li>
<li><b>Then</b> el sistema no guarda cambios,</li>
<li><b>And</b> mantiene la información original.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US53</b></td>
<td>Eliminación de dispositivos</td>
<td>Como administrador, quiero eliminar dispositivos registrados, para mantener el sistema actualizado y sin información innecesaria.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Eliminación de dispositivos.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Eliminación exitosa de dispositivo<br/>
<ul>
<li><b>Given</b> que el administrador accede a la lista de dispositivos,</li>
<li><b>When</b> selecciona un dispositivo y hace clic en "Eliminar",</li>
<li><b>Then</b> el sistema solicita confirmación,</li>
<li><b>And</b> elimina el dispositivo correctamente tras la confirmación.</li>
</ul>
<b>Escenario 2:</b> Cancelación de eliminación<br/>
<ul>
<li><b>Given</b> que el administrador inicia el proceso de eliminación,</li>
<li><b>When</b> decide cancelar la acción,</li>
<li><b>Then</b> el sistema no elimina el dispositivo,</li>
<li><b>And</b> mantiene la información sin cambios.</li>
</ul>
<b>Escenario 3:</b> Eliminación de dispositivo inexistente<br/>
<ul>
<li><b>Given</b> que el dispositivo ya no existe en el sistema,</li>
<li><b>When</b> el administrador intenta eliminarlo,</li>
<li><b>Then</b> el sistema muestra un mensaje de error,</li>
<li><b>And</b> evita la operación.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US54</b></td>
<td>Configuración de zonas de monitoreo</td>
<td>Como administrador, quiero definir zonas de monitoreo dentro de la planta, para segmentar las áreas según niveles de riesgo.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de zonas de monitoreo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Creación de zona<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de zonas,</li>
<li><b>When</b> registra una nueva zona con datos válidos,</li>
<li><b>Then</b> el sistema valida la información,</li>
<li><b>And</b> guarda la zona correctamente.</li>
</ul>
<b>Escenario 2:</b> Edición de zona<br/>
<ul>
<li><b>Given</b> que existen zonas previamente registradas,</li>
<li><b>When</b> el administrador modifica una zona,</li>
<li><b>Then</b> el sistema guarda los cambios,</li>
<li><b>And</b> actualiza la información en el sistema.</li>
</ul>
<b>Escenario 3:</b> Zona duplicada<br/>
<ul>
<li><b>Given</b> que el administrador intenta registrar una zona con un nombre ya existente,</li>
<li><b>When</b> hace clic en "Guardar",</li>
<li><b>Then</b> el sistema rechaza la operación,</li>
<li><b>And</b> muestra el mensaje "La zona ya existe".</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US55</b></td>
<td>Configuración de parámetros del motor predictivo</td>
<td>Como administrador, quiero configurar los parámetros del motor predictivo, para mejorar la precisión en la detección de riesgos.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de parámetros del motor predictivo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Configuración válida de parámetros<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo del motor predictivo,</li>
<li><b>When</b> modifica parámetros dentro de los rangos permitidos y hace clic en "Guardar",</li>
<li><b>Then</b> el sistema valida los valores ingresados,</li>
<li><b>And</b> guarda la configuración correctamente.</li>
</ul>
<b>Escenario 2:</b> Valores fuera de rango<br/>
<ul>
<li><b>Given</b> que el administrador ingresa valores inválidos,</li>
<li><b>When</b> intenta guardar la configuración,</li>
<li><b>Then</b> el sistema rechaza los valores,</li>
<li><b>And</b> muestra un mensaje de error indicando el rango permitido.</li>
</ul>
<b>Escenario 3:</b> Visualización de parámetros<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo,</li>
<li><b>When</b> visualiza los parámetros configurados,</li>
<li><b>Then</b> el sistema muestra los valores actuales,</li>
<li><b>And</b> permite su edición.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US56</b></td>
<td>Configuración de prioridad de alertas</td>
<td>Como administrador, quiero definir la prioridad de las alertas, para atender primero las más críticas.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de prioridad de alertas.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Asignación de prioridad<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de alertas,</li>
<li><b>When</b> asigna una prioridad a una alerta y guarda los cambios,</li>
<li><b>Then</b> el sistema registra la prioridad,</li>
<li><b>And</b> la aplica en el sistema.</li>
</ul>
<b>Escenario 2:</b> Modificación de prioridad<br/>
<ul>
<li><b>Given</b> que existen prioridades configuradas,</li>
<li><b>When</b> el administrador modifica una prioridad,</li>
<li><b>Then</b> el sistema guarda los cambios,</li>
<li><b>And</b> actualiza la información.</li>
</ul>
<b>Escenario 3:</b> Validación de prioridad obligatoria<br/>
<ul>
<li><b>Given</b> que una alerta no tiene prioridad asignada,</li>
<li><b>When</b> se intenta guardar la configuración,</li>
<li><b>Then</b> el sistema bloquea la acción,</li>
<li><b>And</b> solicita asignar una prioridad.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US57</b></td>
<td>Configuración de notificaciones</td>
<td>Como administrador, quiero configurar los canales de notificación del sistema, para recibir alertas de forma oportuna.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Configuración de notificaciones.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Configuración de notificación válida<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de notificaciones,</li>
<li><b>When</b> selecciona un canal y guarda la configuración,</li>
<li><b>Then</b> el sistema registra el canal seleccionado,</li>
<li><b>And</b> activa las notificaciones correctamente.</li>
</ul>
<b>Escenario 2:</b> Sin canales activos<br/>
<ul>
<li><b>Given</b> que el administrador desactiva todos los canales,</li>
<li><b>When</b> intenta guardar la configuración,</li>
<li><b>Then</b> el sistema bloquea la acción,</li>
<li><b>And</b> muestra un mensaje indicando que debe activar al menos uno.</li>
</ul>
<b>Escenario 3:</b> Modificación de configuración<br/>
<ul>
<li><b>Given</b> que existen configuraciones previas,</li>
<li><b>When</b> el administrador modifica los canales,</li>
<li><b>Then</b> el sistema guarda los cambios,</li>
<li><b>And</b> actualiza la configuración.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US58</b></td>
<td>Guardado de configuración del sistema</td>
<td>Como administrador, quiero guardar los cambios realizados en la configuración, para asegurar que los datos se mantengan persistentes en el sistema.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Guardado de configuración del sistema.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Guardado exitoso<br/>
<ul>
<li><b>Given</b> que el administrador ha realizado cambios en la configuración,</li>
<li><b>When</b> hace clic en "Guardar",</li>
<li><b>Then</b> el sistema valida los datos,</li>
<li><b>And</b> guarda la configuración correctamente.</li>
</ul>
<b>Escenario 2:</b> Error en la configuración<br/>
<ul>
<li><b>Given</b> que existen datos inválidos en la configuración,</li>
<li><b>When</b> el administrador intenta guardar,</li>
<li><b>Then</b> el sistema bloquea la acción,</li>
<li><b>And</b> muestra un mensaje de error.</li>
</ul>
<b>Escenario 3:</b> Persistencia de datos<br/>
<ul>
<li><b>Given</b> que la configuración ha sido guardada correctamente,</li>
<li><b>When</b> el sistema se recarga,</li>
<li><b>Then</b> los datos permanecen almacenados,</li>
<li><b>And</b> se muestran correctamente en la interfaz.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US59</b></td>
<td>Restaurar configuración por defecto</td>
<td>Como administrador, quiero restaurar la configuración del sistema a sus valores por defecto, para recuperar el funcionamiento original en caso de errores.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Restaurar configuración por defecto.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Restauración exitosa<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de configuración,</li>
<li><b>When</b> selecciona la opción "Restaurar configuración" y confirma la acción,</li>
<li><b>Then</b> el sistema elimina las configuraciones personalizadas,</li>
<li><b>And</b> restablece los valores por defecto correctamente.</li>
</ul>
<b>Escenario 2:</b> Cancelación de restauración<br/>
<ul>
<li><b>Given</b> que el administrador inicia el proceso de restauración,</li>
<li><b>When</b> decide cancelar la acción,</li>
<li><b>Then</b> el sistema no realiza cambios,</li>
<li><b>And</b> mantiene la configuración actual.</li>
</ul>
<b>Escenario 3:</b> Confirmación de restauración<br/>
<ul>
<li><b>Given</b> que el administrador selecciona restaurar configuración,</li>
<li><b>When</b> el sistema solicita confirmación,</li>
<li><b>Then</b> se muestra un mensaje de advertencia,</li>
<li><b>And</b> requiere confirmación explícita para continuar.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US60</b></td>
<td>Visualización de configuración del sistema</td>
<td>Como administrador, quiero visualizar la configuración actual del sistema, para tener un control general de todos los parámetros definidos.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Visualización de configuración del sistema.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Visualización general<br/>
<ul>
<li><b>Given</b> que el administrador accede al módulo de configuración,</li>
<li><b>When</b> ingresa a la vista general,</li>
<li><b>Then</b> el sistema muestra todos los parámetros configurados,</li>
<li><b>And</b> los organiza de manera clara.</li>
</ul>
<b>Escenario 2:</b> Actualización en tiempo real<br/>
<ul>
<li><b>Given</b> que se realizan cambios en la configuración,</li>
<li><b>When</b> el administrador visualiza la información,</li>
<li><b>Then</b> el sistema refleja los cambios actualizados,</li>
<li><b>And</b> muestra los datos en tiempo real.</li>
</ul>
<b>Escenario 3:</b> Organización de la información<br/>
<ul>
<li><b>Given</b> que existen múltiples configuraciones en el sistema,</li>
<li><b>When</b> el administrador accede a la vista,</li>
<li><b>Then</b> el sistema organiza la información por categorías,</li>
<li><b>And</b> facilita su comprensión.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US61</b></td>
<td>Identidad y Acceso General</td>
<td>Como visitante, quiero acceder a una Landing Page oficial de RiskGuard, para conocer la identidad de la marca y las soluciones que ofrece de manera centralizada.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Identidad y Acceso General.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Acceso exitoso a la Landing Page oficial<br/>
<ul>
<li><b>Given</b> que el visitante dispone de la dirección URL oficial de la Landing Page de RiskGuard,</li>
<li><b>When</b> ingresa la dirección en su navegador y presiona Enter,</li>
<li><b>Then</b> el sistema carga la interfaz principal de la Landing Page,</li>
<li><b>And</b> expone correctamente la identidad visual (logo y colores corporativos) en el encabezado.</li>
</ul>
<b>Escenario 2:</b> Navegación interna por anclas<br/>
<ul>
<li><b>Given</b> que el visitante se encuentra en el inicio de la página,</li>
<li><b>When</b> hace clic en algun enlace del menu de navegacion,</li>
<li><b>Then</b> el sistema realiza un desplazamiento suave hacia la sección seleccionada,</li>
<li><b>And</b> mantiene el Navbar visible para permitir saltar a otras secciónes.</li>
</ul>
</td>
<td align="center"><b>EP06</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US62</b></td>
<td>Propuesta de Valor</td>
<td>Como visitante, quiero visualizar la propuesta de valor principal y un adelanto del panel de control, para entender el impacto inmediato del software en las operaciones segun mi rol.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Propuesta de Valor.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Captación de interés inicial<br/>
<ul>
<li><b>Given</b> que el visitante entra a la Landing Page por primera vez,</li>
<li><b>When</b> visualiza la sección principal,</li>
<li><b>Then</b> el sistema presenta el titular y el porcentaje de "Precisión Predictiva" para generar impacto inmediato.</li>
</ul>
</td>
<td align="center"><b>EP06</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US63</b></td>
<td>Catálogo de Capacidades Técnicas</td>
<td>Como visitante, quiero explorar las funcionalidades específicas del sistema, para validar si la herramienta cumple con los requerimientos que necesita mi sector en la empresa en la que opero.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Catálogo de Capacidades Técnicas.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Exploración general de soluciones<br/>
<ul>
<li><b>Given</b> que el visitante se encuentra navegando por el Landing Page de RiskGuard,</li>
<li><b>When</b> se desplaza hacia la sección de infraestructura de seguridad,</li>
<li><b>Then</b> el sistema presenta el catálogo completo de funcionalidades de manera organizada,</li>
<li><b>And</b> permite al usuario visualizar todas las herramientas disponibles de un solo vistazo.</li>
</ul>
<b>Escenario 2:</b> Comprensión del valor por funcionalidad<br/>
<ul>
<li><b>Given</b> que el visitante está interesado en una funcionalidad específica,</li>
<li><b>When</b> lee la descripción breve que acompaña a cada icono,</li>
<li><b>Then</b> el sistema proporciona información clara sobre el beneficio operativo de dicha función,</li>
<li><b>And</b> ayuda al usuario a determinar si la herramienta se ajusta a las necesidades operativas del sector en el que opera.</li>
</ul>
</td>
<td align="center"><b>EP06</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US64</b></td>
<td>Metodología y Validación Social</td>
<td>Como visitante, quiero conocer el proceso de trabajo que realiza la aplicación web y estadísticas del rubro, para confiar en que la solución es efectiva y está respaldada por datos reales.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Metodología y Validación Social.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Comprensión del flujo de trabajo integral<br/>
<ul>
<li><b>Given</b> el visitante desea conocer cómo se opera con el software en el día a día,</li>
<li><b>When</b> consulta la sección "Diseñado para el piso industrial",</li>
<li><b>Then</b> el sistema describe visualmente la secuencia lógica de participación entre el personal de campo y la plataforma,</li>
<li><b>And</b> permite al usuario entender cómo se cierra el ciclo desde el reporte hasta la actuación del supervisor.</li>
</ul>
<b>Escenario 2:</b> Sensibilización mediante datos del rubro<br/>
<ul>
<li><b>Given</b> que el visitante busca argumentos para priorizar la seguridad en su planta,</li>
<li><b>When</b> revisa las estadísticas de la industria peruana presentadas en la página,</li>
<li><b>Then</b> el sistema expone cifras relevantes sobre el impacto de la prevención y los riesgos actuales,</li>
<li><b>And</b> ayuda al usuario a visualizar la magnitud del problema que RiskGuard ayuda a resolver.</li>
</ul>
</td>
<td align="center"><b>EP06</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US65</b></td>
<td>Beneficios por Rol Operativo</td>
<td>Como visitante, quiero identificar qué herramientas específicas recibe cada nivel de mi organización, para planificar la adopción del sistema entre mis colaboradores.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Beneficios por Rol Operativo.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Identificación de herramientas por nivel jerárquico<br/>
<ul>
<li><b>Given</b> que un visitante evalúa cómo distribuir la solución entre sus colaboradores,</li>
<li><b>When</b> explora la sección de "Una herramienta unificada para toda la jerarquía",</li>
<li><b>Then</b> el sistema presenta las capacidades que recibirá cada perfil (Operarios, Supervisores y Administracion),</li>
<li><b>And</b> permite al usuario confirmar que cada rol tiene las herramientas necesarias para cumplir su función.</li>
</ul>
</td>
<td align="center"><b>EP06</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>US66</b></td>
<td>Cierre y Conversión de Prospectos</td>
<td>Como visitante, quiero disponer de opciones claras para iniciar una prueba o contactar a ventas, para comenzar el proceso de implementación en mi empresa.</td>
<td>
<ol>
<li>El sistema debe permitir al usuario realizar la acción principal de Cierre y Conversión de Prospectos.</li>
<li>La información debe mostrarse o registrarse correctamente, validando errores y estados necesarios.</li>
</ol>

<b>Escenario 1:</b> Intención de inicio de uso del software<br/>
<ul>
<li><b>Given</b> que el visitante ha terminado de informarse y desea probar la solución,</li>
<li><b>When</b> localiza y presiona el botón de "Iniciar prueba gratuita",</li>
<li><b>Then</b> el sistema facilita el punto de partida para la conversión, guiando al usuario hacia el siguiente paso de adquisición.</li>
</ul>
<b>Escenario 2:</b> Verificación de soporte y respaldo institucional<br/>
<ul>
<li><b>Given</b> que el visitante requiere verificar la procedencia y el soporte técnico del sistema,</li>
<li><b>When</b> revisa la sección del footer al final de la navegación,</li>
<li><b>Then</b> el sistema muestra claramente la afiliación a la UPC y las opciones de soporte técnico disponibles,</li>
<li><b>And</b> genera una percepción de confianza y seriedad institucional sobre el producto.</li>
</ul>
</td>
<td align="center"><b>EP06</b></td>
</tr>
</tbody>
</table>


#### Technical Stories 


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS01</b></td>
<td>Servicio de Notificaciones Push</td>
<td>Como desarrollador, quiero implementar el endpoint POST /api/v1/notificaciones/push para enviar alertas críticas en tiempo real a los dispositivos móviles.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Envío exitoso<br/>
<ul>
<li><b>Given</b> que existe una alerta crítica,</li>
<li><b>When</b> el sistema envía la notificación,</li>
<li><b>Then</b> el endpoint responde con HTTP 202,</li>
<li><b>And</b> la notificación es entregada al dispositivo del usuario.</li>
</ul>
<b>Escenario 2:</b> Error en servicio externo<br/>
<ul>
<li><b>Given</b> que falla el proveedor de notificaciones,</li>
<li><b>When</b> el sistema intenta enviar el mensaje,</li>
<li><b>Then</b> se ejecuta un reintento automático,</li>
<li><b>And</b> el error queda registrado en logs.</li>
</ul>
<b>Escenario 3:</b> Usuario offline<br/>
<ul>
<li><b>Given</b> que el usuario no tiene conexión,</li>
<li><b>When</b> se envía la notificación,</li>
<li><b>Then</b> el sistema la almacena en cola,</li>
<li><b>And</b> la envía cuando el usuario se reconecta.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS02</b></td>
<td>Endpoint para Obtener Patrones de Riesgo Recurrentes</td>
<td>Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/patrones que devuelva los patrones de riesgo recurrentes por sector y período, para mostrar las alertas predictivas en el dashboard del supervisor de seguridad.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Solicitud exitosa con patrones detectados<br/>
<ul>
<li><b>Given</b> que el sector consultada tiene registros suficientes en el período indicado,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/patrones?area=almacen&dias=30,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y la lista de patrones detectados con tipo de riesgo, frecuencia y fecha de primera ocurrencia.</li>
</ul>
<b>Escenario 2:</b> Sector sin datos suficientes para detectar patrones<br/>
<ul>
<li><b>Given</b> que el sector consultada tiene menos de 3 registros en el período indicado,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/patrones con esos parámetros,</li>
<li><b>Then</b> el endpoint responde con HTTP 200, lista vacía y el mensaje "Datos insuficientes para detectar patrones en el período indicado".</li>
</ul>
<b>Escenario 3:</b> Sector no encontrada en el sistema<br/>
<ul>
<li><b>Given</b> que el desarrollador envía un identificador de sector que no existe en el sistema,</li>
<li><b>When</b> el endpoint procesa la solicitud,</li>
<li><b>Then</b> el endpoint retorna HTTP 404 con el mensaje "sector no encontrada en el sistema".</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS03</b></td>
<td>Endpoint para Obtener Datos del Mapa de Calor</td>
<td>Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/mapa-calor que retorne la concentración de riesgos activos por sector clasificada por nivel de intensidad, para alimentar el mapa de calor del dashboard en tiempo real.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Solicitud exitosa con riesgos activos registrados<br/>
<ul>
<li><b>Given</b> que al menos un sector de la planta tiene riesgos activos registrados,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/mapa-calor,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 con cada sector y su nivel de intensidad calculado según la concentración de riesgos activos.</li>
</ul>
<b>Escenario 2:</b> Sin riesgos activos en ningun sector de la planta<br/>
<ul>
<li><b>Given</b> que ninguna sector tiene riesgos activos registrados en ese momento,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/mapa-calor,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 con todas las sectors en nivel de intensidad "bajo".</li>
</ul>
<b>Escenario 3:</b> Sector recién actualizada reflejada en el mapa<br/>
<ul>
<li><b>Given</b> que se acaba de registrar un nuevo riesgo crítico en el sector de Producción,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/mapa-calor inmediatamente después,</li>
<li><b>Then</b> el endpoint retorna el sector de Producción con el nivel de intensidad actualizado reflejando el nuevo riesgo.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS04</b></td>
<td>Endpoint para Obtener Riesgos Críticos Sin Atender</td>
<td>Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/no-atendidos que retorne los riesgos críticos sin acción correctiva asignada que superen el tiempo indicado, para que el módulo de notificaciones escale automáticamente al supervisor de seguridad.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Riesgos sin atender encontrados en el sistema<br/>
<ul>
<li><b>Given</b> que existen riesgos críticos sin acción correctiva asignada por más de 24 horas,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/no-atendidos?horas=24,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y la lista de riesgos que superaron el umbral con sector, tipo, criticidad y horas transcurridas sin atención.</li>
</ul>
<b>Escenario 2:</b> Todos los riesgos críticos fueron atendidos a tiempo<br/>
<ul>
<li><b>Given</b> que todos los riesgos críticos activos tienen acción correctiva asignada dentro del plazo,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/no-atendidos?horas=24,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y lista vacía confirmando que no hay riesgos sin atender.</li>
</ul>
<b>Escenario 3:</b> Parámetro de horas no enviado en la solicitud<br/>
<ul>
<li><b>Given</b> que el desarrollador realiza GET /api/v1/predictivo/no-atendidos sin enviar el parámetro de horas,</li>
<li><b>When</b> el endpoint procesa la solicitud,</li>
<li><b>Then</b> el endpoint retorna HTTP 400 con el mensaje "El parámetro 'horas' es requerido para procesar esta solicitud".</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS05</b></td>
<td>Endpoint para Marcar Alerta de Patrón como Revisada</td>
<td>Como desarrollador, quiero implementar el endpoint PATCH /api/v1/predictivo/alertas/{id}/revisada que permita marcar una alerta de patrón recurrente como revisada, para retirarla del panel principal y registrar quién la atendió.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Alerta marcada como revisada exitosamente<br/>
<ul>
<li><b>Given</b> que existe una alerta de patrón recurrente en estado pendiente,</li>
<li><b>When</b> el desarrollador realiza PATCH /api/v1/predictivo/alertas/{id}/revisada con token válido,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y actualiza el estado de la alerta a "revisada" registrando la fecha y el usuario.</li>
</ul>
<b>Escenario 2:</b> Alerta no encontrada en el sistema<br/>
<ul>
<li><b>Given</b> que el identificador de alerta enviado no existe en el sistema,</li>
<li><b>When</b> el endpoint procesa la solicitud,</li>
<li><b>Then</b> el endpoint retorna HTTP 404 indicando que la alerta no fue encontrada.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>



<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS06</b></td>
<td>Endpoint para Obtener Resumen Diario de Riesgos por Sector</td>
<td>Como desarrollador, quiero implementar el endpoint GET /api/v1/predictivo/resumen-diario que retorne el total de riesgos registrados en el día agrupados por sector, para alimentar el panel de resumen del dashboard del supervisor.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Solicitud exitosa con riesgos del día<br/>
<ul>
<li><b>Given</b> que se han registrado riesgos durante el día actual en al menos un sector,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/resumen-diario con token válido,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el listado de sectores con sus conteos de riesgos nuevos, en progreso y resueltos del día.</li>
</ul>
<b>Escenario 2:</b> Sin riesgos registrados en el día<br/>
<ul>
<li><b>Given</b> que no se han registrado riesgos durante el día actual,</li>
<li><b>When</b> el desarrollador realiza GET /api/v1/predictivo/resumen-diario,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y lista vacía.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>



<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS07</b></td>
<td>Endpoint de Cálculo de Matriz IPERC</td>
<td>Como desarrollador, quiero implementar el endpoint POST /api/v1/predictivo/iperc que reciba los índices de probabilidad y severidad, para calcular el nivel de criticidad del riesgo según la lógica IPERC del sistema.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Cálculo de riesgo exitoso<br/>
<ul>
<li><b>Given</b> se procesa el request válido con probability_index y severity_index,</li>
<li><b>When</b> el API procesa la solicitud en el endpoint POST /api/v1/predictivo/iperc,</li>
<li><b>Then</b> el sistema calcula correctamente el nivel de criticidad del riesgo,</li>
<li><b>And</b> retorna un HTTP 200 OK</li>
</ul>
<b>Escenario 2:</b> Valores fuera de rango<br/>
<ul>
<li><b>Given</b> que los valores enviados están fuera del rango permitido,</li>
<li><b>When</b> el API valida la solicitud,</li>
<li><b>Then</b> responde con HTTP 400 Bad Request,</li>
<li><b>And</b> retorna un mensaje de error de validación de parámetros.</li>
</ul>
</td>
<td align="center"><b>EP02</b></td>
</tr>
</tbody>
</table>



<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS08</b></td>
<td>Endpoint para Obtener Indicadores del Dashboard Ejecutivo</td>
<td>Como desarrollador, quiero consumir el endpoint GET /api/v1/kpi_dashboard que retorna los indicadores clave de SST consolidados, para alimentar el tablero ejecutivo del gerente con datos actualizados en tiempo real.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Solicitud exitosa con datos disponibles<br/>
<ul>
<li><b>Given</b> que existen registros en la colección kpi_dashboard,</li>
<li><b>When</b> el frontend realiza GET /api/v1/kpi_dashboard,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el arreglo de indicadores con sus valores y estados actuales.</li>
</ul>
<b>Escenario 2:</b> Sin datos registrados<br/>
<ul>
<li><b>Given</b> que la colección kpi_dashboard no tiene registros,</li>
<li><b>When</b> el frontend realiza GET /api/v1/kpi_dashboard,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y un arreglo vacío.</li>
</ul>
<b>Escenario 3:</b> Actualización reactiva de indicadores<br/>
<ul>
<li><b>Given</b> que el frontend recibe los indicadores y el usuario resuelve un incidente o alerta,</li>
<li><b>When</b> el store ejecuta syncKPIs(),</li>
<li><b>Then</b> los valores de active_incidents, resolved_incidents y critical_sectors se recalculan automáticamente sin necesidad de recargar la página.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS09</b></td>
<td>Endpoint para Obtener Tendencias Históricas de Accidentabilidad</td>
<td>Como desarrollador, quiero consumir el endpoint GET /api/v1/historical_trends que retorna la evolución mensual de incidentes agrupados por tipo y sector, para alimentar las gráficas de tendencia del tablero ejecutivo del gerente.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Solicitud exitosa con datos disponibles<br/>
<ul>
<li><b>Given</b> que existen registros en la colección historical_trends,</li>
<li><b>When</b> el frontend realiza GET /api/v1/historical_trends,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el arreglo de datos mensuales con su desglose por tipo y sector.</li>
</ul>
<b>Escenario 2:</b> Filtrado por sector en el frontend<br/>
<ul>
<li><b>Given</b> que el gerente selecciona un sector específico en el filtro del dashboard,</li>
<li><b>When</b> el frontend aplica el filtro sobre los datos ya cargados del endpoint,</li>
<li><b>Then</b> la gráfica se actualiza mostrando únicamente los datos del sector seleccionado sin realizar una nueva petición al servidor.</li>
</ul>
<b>Escenario 3:</b> Vista por tipo de incidente<br/>
<ul>
<li><b>Given</b> que el gerente activa el modo "por tipo" en la gráfica,</li>
<li><b>When</b> el frontend procesa el campo incidents_by_type de cada registro,</li>
<li><b>Then</b> la gráfica muestra una línea por cada tipo de incidente con colores diferenciados.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS10</b></td>
<td>Endpoint para Gestión de Reportes Generados</td>
<td>Como desarrollador, quiero consumir los endpoints GET y POST /api/v1/generated_reports y DELETE /api/v1/generated_reports/{id} para registrar, listar y eliminar reportes generados, mientras la generación del documento PDF o Excel se realiza en el cliente con jsPDF.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Generación y registro exitoso en PDF<br/>
<ul>
<li><b>Given</b> que existen incidentes registrados en el rango de fechas indicado,</li>
<li><b>When</b> el gerente hace clic en "Generar reporte" con formato PDF,</li>
<li><b>Then</b> el frontend genera el PDF con jsPDF, lo descarga automáticamente y registra el reporte en el endpoint POST /api/v1/generated_reports.</li>
</ul>
<b>Escenario 2:</b> Período sin datos<br/>
<ul>
<li><b>Given</b> que no existen incidentes en el rango de fechas seleccionado,</li>
<li><b>When</b> el gerente hace clic en "Generar reporte",</li>
<li><b>Then</b> el frontend muestra el mensaje "No hay datos registrados para el período seleccionado" y no genera ningún archivo ni realiza el POST al endpoint.</li>
</ul>
<b>Escenario 3:</b> Eliminación de reporte generado<br/>
<ul>
<li><b>Given</b> que el gerente visualiza la lista de reportes generados,</li>
<li><b>When</b> hace clic en el ícono de eliminar sobre un reporte,</li>
<li><b>Then</b> el frontend realiza DELETE /api/v1/generated_reports/{id} y el registro desaparece de la lista sin recargar la página.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS11</b></td>
<td>Endpoint para Gestión de Alertas Críticas</td>
<td>Como desarrollador, quiero consumir los endpoints GET, PATCH y DELETE /api/v1/critical_alerts para listar, actualizar el estado y eliminar alertas críticas, para que el gerente pueda gestionar los riesgos no resueltos desde el tablero ejecutivo.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Listado de alertas exitoso<br/>
<ul>
<li><b>Given</b> que existen alertas registradas en la colección critical_alerts,</li>
<li><b>When</b> el frontend realiza GET /api/v1/critical_alerts,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el arreglo de alertas con todos sus campos.</li>
</ul>
<b>Escenario 2:</b> Marcar alerta como resuelta<br/>
<ul>
<li><b>Given</b> que el gerente visualiza una alerta con status "unresolved" o "in_review",</li>
<li><b>When</b> hace clic en el ícono de check,</li>
<li><b>Then</b> el frontend realiza PATCH /api/v1/critical_alerts/{id} con status "resolved", actualiza el registro en el store y recalcula los KPIs sin recargar la página.</li>
</ul>
<b>Escenario 3:</b> Eliminación de alerta<br/>
<ul>
<li><b>Given</b> que el gerente hace clic en el ícono de eliminar sobre una alerta,</li>
<li><b>When</b> el frontend realiza DELETE /api/v1/critical_alerts/{id},</li>
<li><b>Then</b> la alerta desaparece de la tabla y el KPI de sectores críticos se actualiza automáticamente.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

---

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS12</b></td>
<td>Endpoint para Obtener el Plan Anual de SST y su Cumplimiento</td>
<td>Como desarrollador, quiero consumir el endpoint GET /api/v1/annual_ohs_plan que retorne el plan anual de SST con el porcentaje de cumplimiento global y el desglose por sector, para alimentar el indicador de seguimiento del tablero ejecutivo del gerente.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Solicitud exitosa con plan registrado<br/>
<ul>
<li><b>Given</b> que existe un plan anual de SST registrado en la colección annual_ohs_plan,</li>
<li><b>When</b> el frontend realiza GET /api/v1/annual_ohs_plan,</li>
<li><b>Then</b> el endpoint responde con HTTP 200, el porcentaje global de cumplimiento y el desglose por sector.</li>
</ul>
<b>Escenario 2:</b> Detalle de cumplimiento por sector desde el dashboard<br/>
<ul>
<li><b>Given</b> que el gerente hace clic en el KPI de cumplimiento del plan SST,</li>
<li><b>When</b> el frontend procesa el campo details_by_sector del plan retornado,</li>
<li><b>Then</b> muestra un dialog con los sectores ordenados de menor a mayor cumplimiento con sus indicadores de color.</li>
</ul>
<b>Escenario 3:</b> Sin plan registrado<br/>
<ul>
<li><b>Given</b> que la colección annual_ohs_plan no tiene registros,</li>
<li><b>When</b> el frontend realiza GET /api/v1/annual_ohs_plan,</li>
<li><b>Then</b> el endpoint retorna HTTP 200 con arreglo vacío y el frontend muestra el estado vacío en la vista de seguimiento SST.</li>
</ul>
</td>
<td align="center"><b>EP04</b></td>
</tr>
</tbody>
</table>

<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS13</b></td>
<td>Endpoint para Registro y Consulta de Inspecciones por Operario</td>
<td>Como desarrollador, quiero implementar los endpoints POST /api/v1/inspecciones para registrar una nueva inspección y GET /api/v1/inspecciones/mine/{operarioId} para que el operario consulte sus inspecciones enviadas, permitiendo la trazabilidad de reportes desde el backend.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Registro exitoso de inspección<br/>
<ul>
<li><b>Given</b> que el operario completa el formulario de inspección con todos los campos obligatorios,</li>
<li><b>When</b> el frontend realiza POST /api/v1/inspecciones con token válido,</li>
<li><b>Then</b> el endpoint responde con HTTP 201 y el objeto de inspección creado con su ticket generado.</li>
</ul>
<b>Escenario 2:</b> Consulta de inspecciones propias<br/>
<ul>
<li><b>Given</b> que el operario desea ver el historial de sus reportes,</li>
<li><b>When</b> el frontend realiza GET /api/v1/inspecciones/mine/{operarioId},</li>
<li><b>Then</b> el endpoint retorna HTTP 200 con el listado de inspecciones del operario.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS14</b></td>
<td>Endpoint para Gestión de Catálogo de Peligros</td>
<td>Como desarrollador, quiero implementar los endpoints CRUD /api/v1/peligros para administrar el catálogo de tipos de peligro (físico, químico, ergonómico, biológico) que se utilizan al clasificar inspecciones y evaluar riesgos.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Listado exitoso de peligros<br/>
<ul>
<li><b>Given</b> que existen tipos de peligro registrados en el sistema,</li>
<li><b>When</b> el frontend realiza GET /api/v1/peligros,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el arreglo de peligros con id, nombre y descripción.</li>
</ul>
<b>Escenario 2:</b> Creación de nuevo tipo de peligro<br/>
<ul>
<li><b>Given</b> que el administrador necesita agregar una nueva categoría de peligro,</li>
<li><b>When</b> realiza POST /api/v1/peligros con nombre y descripción,</li>
<li><b>Then</b> el endpoint responde con HTTP 201 y el peligro creado.</li>
</ul>
</td>
<td align="center"><b>EP01</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS15</b></td>
<td>Endpoint para Gestión de Sedes Operativas</td>
<td>Como desarrollador, quiero implementar los endpoints CRUD /api/v1/sedes para registrar, listar, actualizar y eliminar las sedes físicas de la planta industrial, permitiendo la organización jerárquica de la infraestructura operativa.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Listado exitoso de sedes<br/>
<ul>
<li><b>Given</b> que existen sedes registradas en el sistema,</li>
<li><b>When</b> el supervisor realiza GET /api/v1/sedes,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el arreglo de sedes.</li>
</ul>
<b>Escenario 2:</b> Eliminación bloqueada por áreas activas<br/>
<ul>
<li><b>Given</b> que la sede tiene áreas activas asociadas,</li>
<li><b>When</b> se intenta DELETE /api/v1/sedes/{id},</li>
<li><b>Then</b> el endpoint retorna HTTP 409 indicando que no se puede eliminar.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS16</b></td>
<td>Endpoint para Gestión de Áreas y Activos Industriales</td>
<td>Como desarrollador, quiero implementar los endpoints CRUD /api/v1/areas con filtro GET /active y /api/v1/activos con filtro GET /by-area/{areaId}, para gestionar las áreas operativas y los activos industriales vinculados a cada zona de la planta.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Consulta de áreas activas<br/>
<ul>
<li><b>Given</b> que existen áreas con diferentes estados en el sistema,</li>
<li><b>When</b> el frontend realiza GET /api/v1/areas/active,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y solo las áreas con estado activo.</li>
</ul>
<b>Escenario 2:</b> Consulta de activos por área<br/>
<ul>
<li><b>Given</b> que un área tiene activos industriales registrados,</li>
<li><b>When</b> el frontend realiza GET /api/v1/activos/by-area/{areaId},</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el listado de activos del área.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS17</b></td>
<td>Endpoint para Autenticación y Generación de Token JWT</td>
<td>Como desarrollador, quiero implementar los endpoints POST /api/v1/authentication/sign-in y POST /api/v1/authentication/sign-up para autenticar usuarios y generar tokens JWT con claims de rol (operario, supervisor, gerente), permitiendo el control de acceso basado en roles en todos los Web Services.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Inicio de sesión exitoso<br/>
<ul>
<li><b>Given</b> que el usuario tiene credenciales válidas registradas,</li>
<li><b>When</b> realiza POST /api/v1/authentication/sign-in con username y password,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el token JWT con claims de rol.</li>
</ul>
<b>Escenario 2:</b> Credenciales inválidas<br/>
<ul>
<li><b>Given</b> que el password no coincide con el registrado,</li>
<li><b>When</b> realiza POST /api/v1/authentication/sign-in,</li>
<li><b>Then</b> el endpoint retorna HTTP 401 indicando credenciales inválidas.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS18</b></td>
<td>Endpoint para Gestión de Usuarios, Roles y Sesiones</td>
<td>Como desarrollador, quiero implementar los endpoints CRUD /api/v1/users, /api/v1/roles, /api/v1/sessions y /api/v1/access-logs para administrar las cuentas de usuario, los roles del sistema, las sesiones activas y el registro de auditoría de accesos.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Listado de usuarios<br/>
<ul>
<li><b>Given</b> que el administrador necesita gestionar las cuentas del sistema,</li>
<li><b>When</b> realiza GET /api/v1/users con token de administrador,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y el listado de usuarios.</li>
</ul>
<b>Escenario 2:</b> Consulta de logs de acceso<br/>
<ul>
<li><b>Given</b> que se requiere auditar los accesos al sistema,</li>
<li><b>When</b> realiza GET /api/v1/access-logs,</li>
<li><b>Then</b> el endpoint retorna HTTP 200 con el historial de accesos.</li>
</ul>
</td>
<td align="center"><b>EP05</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS19</b></td>
<td>Endpoint para Gestión de Tickets, Técnicos y Mantenimiento Preventivo</td>
<td>Como desarrollador, quiero implementar los endpoints CRUD /api/v1/tickets, /api/v1/technicians, /api/v1/preventive-maintenances y /api/v1/assets para gestionar la asignación de tickets correctivos, el directorio de técnicos, la programación de mantenimientos preventivos y el inventario de activos desde el dashboard del supervisor.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Creación de ticket correctivo<br/>
<ul>
<li><b>Given</b> que el supervisor identifica una acción correctiva necesaria,</li>
<li><b>When</b> realiza POST /api/v1/tickets con los datos del ticket y técnico asignado,</li>
<li><b>Then</b> el endpoint responde con HTTP 201 y el ticket creado con su deadline de SLA calculado.</li>
</ul>
<b>Escenario 2:</b> Programación de mantenimiento preventivo<br/>
<ul>
<li><b>Given</b> que el supervisor necesita programar mantenimiento sobre un activo,</li>
<li><b>When</b> realiza POST /api/v1/preventive-maintenances con activo y fecha programada,</li>
<li><b>Then</b> el endpoint responde con HTTP 201 y el mantenimiento programado.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>


<table align="center">
<thead>
<tr>
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relacionado con (Epic ID)</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td align="center"><b>TS20</b></td>
<td>Endpoint para Gestión de Zonas del Mapa de Calor y Reportes Archivados</td>
<td>Como desarrollador, quiero implementar los endpoints CRUD /api/v1/heat-map-zones y /api/v1/archived-reports para gestionar las zonas del mapa de calor operativo y el archivo histórico de reportes del dashboard de monitoreo del supervisor.</td>
<td>
<ol>
<li>El endpoint debe responder correctamente seg?n la operaci?n solicitada y validar los datos obligatorios.</li>
<li>El sistema debe guardar o devolver la información necesaria con mensajes claros ante errores.</li>
</ol>

<b>Escenario 1:</b> Listado de zonas del mapa de calor<br/>
<ul>
<li><b>Given</b> que existen zonas registradas con diferentes niveles de riesgo,</li>
<li><b>When</b> el frontend realiza GET /api/v1/heat-map-zones,</li>
<li><b>Then</b> el endpoint responde con HTTP 200 y las zonas ordenadas por riskLevel descendente.</li>
</ul>
<b>Escenario 2:</b> Archivo de reporte<br/>
<ul>
<li><b>Given</b> que el supervisor desea archivar un reporte generado,</li>
<li><b>When</b> realiza POST /api/v1/archived-reports,</li>
<li><b>Then</b> el endpoint responde con HTTP 201 y el reporte archivado.</li>
</ul>
</td>
<td align="center"><b>EP03</b></td>
</tr>
</tbody>
</table>



## 3.2. Impact Mapping

El Impact Mapping es una técnica de planificación estratégica que permite vincular los objetivos de negocio con las funcionalidades del producto, respondiendo las preguntas: ¿por qué construimos esto?, ¿quién nos ayuda a lograrlo?, ¿cómo cambia su comportamiento? y ¿qué entregamos para provocar ese cambio? Su elaboración permite asegurar que cada User Story tenga un propósito claro y directo sobre el objetivo del negocio.

A continuación se presenta el Impact Map elaborado en UXPressia para RiskGuard:

  <div align="center">
      
![Foto](images/imp_map.png)
  <p>
    <i><b>Fuente</b>: Elaboración propia en UXPRESSIA. </i>
  </p>
</div>

---

El Impact Map parte de un único objetivo de negocio: incrementar la prevención de accidentes laborales en entornos industriales mediante la digitalización del registro de incidentes y el uso de analítica predictiva en tiempo real. Para lograr este objetivo, se identificaron tres actores clave dentro del ecosistema de la seguridad laboral: el operario de planta, el supervisor de seguridad y mantenimiento, y el gerente o administrador.

A partir de estos actores se definieron los impactos esperados en su comportamiento. En el caso del operario, se busca que registre incidentes y condiciones inseguras de manera constante y que confíe en el sistema al recibir retroalimentación sobre sus reportes. En el caso del supervisor, se espera que identifique patrones de riesgo de forma automática y que actúe de manera proactiva ante situaciones críticas. Finalmente, en el caso del gerente, se pretende que tome decisiones estratégicas basadas en información confiable y que anticipe riesgos antes de que se conviertan en incidentes que afecten la operación.

Cada uno de estos impactos se traduce en entregables concretos, tales como formularios de registro rápido, dashboards con mapas de calor, sistemas de alertas automáticas y reportes ejecutivos, los cuales corresponden a las funcionalidades principales de la plataforma. Estos entregables están respaldados por las User Stories definidas en la sección correspondiente, garantizando la trazabilidad entre el objetivo de negocio, los cambios de comportamiento esperados y las soluciones implementadas en el sistema.


## 3.3. Product Backlog

| # | ID | Título | Descripción | SP |
|---|---|---|---|---|
| 1 | US61 | Identidad y Acceso General | Como visitante, quiero acceder a una Landing Page oficial de RiskGuard, para conocer la identidad de la marca y las soluciones que ofrece de manera centralizada. | 2 |
| 2 | US62 | Propuesta de Valor | Como visitante, quiero visualizar la propuesta de valor principal y un adelanto del panel de control, para entender el impacto inmediato del software en las operaciones segun mi rol. | 3 |
| 3 | US63 | Catálogo de Capacidades Técnicas | Como visitante, quiero explorar las funcionalidades específicas del sistema, para validar si la herramienta cumple con los requerimientos que necesita mi sector en la empresa en la que opero. | 3 |
| 4 | US64 | Metodología y Validación Social | Como visitante, quiero conocer el proceso de trabajo que realiza la aplicación web y estadísticas del rubro, para confiar en que la solución es efectiva y está respaldada por datos reales. | 3 |
| 5 | US65 | Beneficios por Rol Operativo | Como visitante, quiero identificar qué herramientas específicas recibe cada nivel de mi organización, para planificar la adopción del sistema entre mis colaboradores. | 3 |
| 6 | US66 | Cierre y Conversión de Prospectos | Como visitante, quiero disponer de opciones claras para iniciar una prueba o contactar a ventas, para comenzar el proceso de implementación en mi empresa. | 2 |
| 7 | US16 | Visualización de métricas de impacto predictivo | Como visitante, quiero visualizar indicadores reales de siniestralidad en el Landing Page para comprender el impacto de la analítica predictiva. | 2 |
| 8 | US17 | Interacción con botones de conversión | Como visitante, quiero interactuar con los botones "Iniciar prueba gratuita" y "Hablar con ventas" para contactar con el servicio de RiskGuard. | 2 |
| 9 | US03 | Registro Rápido de Casi-Accidente | Como Operario de Planta, quiero registrar un casi-accidente desde mi celular en menos de 30 segundos para no interrumpir mi flujo de trabajo. | 5 |
| 10 | US04 | Adjuntar Evidencia Fotográfica al Reporte | Como Operario de Planta, quiero adjuntar una foto al momento de reportar un incidente para proporcionar evidencia visual al supervisor. | 3 |
| 11 | US05 | Selección de Sector al Registrar Incidente | Como Operario de Planta, quiero seleccionar el sector donde ocurrió el incidente para georreferenciar correctamente el riesgo. | 3 |
| 12 | US06 | Selección del Nivel de Urgencia del Incidente | Como Operario de Planta, quiero indicar el nivel de urgencia del incidente para que el sistema priorice correctamente la alerta. | 3 |
| 13 | US07 | Selección del Tipo de Incidente | Como Operario de Planta, quiero seleccionar el tipo de incidente de una lista predefinida para categorizar correctamente el riesgo. | 3 |
| 14 | US08 | Registro de Condición Insegura Vinculada a un Activo | Como Operario de Planta, quiero vincular mi reporte a un activo específico para indicar qué máquina presenta la condición insegura. | 3 |
| 15 | US09 | Descripción de Texto Libre en el Reporte | Como Operario de Planta, quiero ingresar una descripción en texto libre para dar más contexto al supervisor. | 2 |
| 16 | US10 | Confirmación de Recepción del Reporte | Como Operario de Planta, quiero recibir una confirmación visible después de enviar mi reporte para saber que la información llegó correctamente. | 3 |
| 17 | US15 | Edición de Reporte Antes del Envío | Como Operario de Planta, quiero poder revisar y corregir los datos de mi reporte antes de enviarlo para asegurar que la información es precisa. | 2 |
| 18 | US11 | Notificación de Atención del Reporte | Como Operario de Planta, quiero recibir una notificación cuando mi reporte haya sido revisado para saber que tuvo impacto real. | 3 |
| 19 | US12 | Historial de Reportes del Operario | Como Operario de Planta, quiero consultar el historial de mis reportes para hacer seguimiento del estado de cada uno. | 3 |
| 20 | US13 | Consulta del Detalle de un Reporte Enviado | Como Operario de Planta, quiero ver el detalle completo de un reporte que envié para conocer su estado actual y la acción tomada. | 2 |
| 21 | US14 | Visualización de Alertas Activas en el Sector | Como Operario de Planta, quiero ver las alertas activas en mi sector al ingresar a la aplicación para estar informado antes de iniciar mi turno. | 3 |
| 22 | US25 | Configuración de Sectores y Áreas Operativas | Como Supervisor de Seguridad, quiero administrar los sectores físicos de la planta para georreferenciar correctamente las incidencias reportadas. | 5 |
| 23 | US26 | Configuración y Gestión de Activos Industriales | Como Supervisor de Seguridad, quiero registrar y administrar la maquinaria de la planta para vincularla a su sector correspondiente. | 5 |
| 24 | US27 | Gestión y Administración de Personal Técnico | Como Supervisor de Seguridad, quiero registrar y administrar al personal de mantenimiento para disponer de técnicos calificados a quienes delegar tickets. | 5 |
| 25 | US28 | Asignación de Tickets de Acción Correctiva | Como Supervisor de Seguridad, quiero asignar un ticket de incidente a un técnico de mantenimiento para delegar la responsabilidad de la reparación. | 5 |
| 26 | US29 | Exploración Sectorizada y Filtrado de Alertas Activas | Como Supervisor de Seguridad, quiero acceder a las alertas activas seleccionando un sector específico para enfocar mi análisis por zona. | 5 |
| 27 | US30 | Verificación y Cierre de Medidas de Control | Como Supervisor de Seguridad, quiero evaluar la efectividad de las medidas correctivas implementadas para garantizar que el riesgo fue mitigado. | 5 |
| 28 | US18 | Visualización de Alerta por Riesgo Recurrente en Sector | Como Supervisor de Seguridad, quiero recibir una alerta cuando el mismo tipo de riesgo se repita más de 3 veces en 30 días para intervenir a tiempo. | 8 |
| 29 | US19 | Visualización de Mapa de Calor de Riesgos de la Planta | Como Supervisor de Seguridad, quiero ver un mapa de calor actualizado de la planta para priorizar mis recursos de inspección. | 8 |
| 30 | US31 | Visualización del Mapa de Calor Operativo | Como Supervisor de Seguridad, quiero visualizar la distribución de niveles de riesgo por sector para identificar qué áreas requieren intervención prioritaria. | 8 |
| 31 | US22 | Visualización de Resumen de Riesgos del Día | Como Supervisor de Seguridad, quiero ver cuántos riesgos nuevos se registraron hoy en cada sector para tener una visión rápida al inicio de mi turno. | 3 |
| 32 | US20 | Notificación de Riesgo Crítico Sin Atender | Como Supervisor de Seguridad, quiero que el sistema me notifique cuando un riesgo crítico lleve más de 24 horas sin ser atendido para escalarlo a tiempo. | 5 |
| 33 | US32 | Notificación Externa Automática por Incidentes Críticos | Como Supervisor de Seguridad, quiero recibir notificaciones automáticas por correo cuando el sistema registre un incidente crítico para garantizar respuesta inmediata. | 5 |
| 34 | US33 | Escalamiento Automático por Incumplimiento de SLA | Como Supervisor de Seguridad, quiero que el sistema escale automáticamente los tickets que superen su tiempo máximo de resolución para alertar a gerencia. | 8 |
| 35 | US21 | Filtrado de Patrones de Riesgo por Tipo de Peligro | Como Supervisor de Seguridad, quiero filtrar los patrones de riesgo detectados por tipo de peligro para analizar de forma segmentada cada categoría. | 3 |
| 36 | US23 | Marcar Alerta de Patrón Recurrente como Revisada | Como Supervisor de Seguridad, quiero marcar una alerta de patrón recurrente como revisada para mantener el dashboard organizado. | 2 |
| 37 | US34 | Programación de Mantenimiento Preventivo de Activos | Como Supervisor de Seguridad, quiero programar tickets de mantenimiento preventivo sobre máquinas específicas para evitar fallas críticas futuras. | 8 |
| 38 | US35 | Generación y Exportación de Reportes de Cumplimiento | Como Supervisor de Seguridad, quiero generar y exportar reportes consolidados del historial de incidentes para documentar el cumplimiento normativo. | 8 |
| 39 | US37 | Visualización del Dashboard Ejecutivo de Seguridad | Como Gerente, quiero ver un dashboard ejecutivo con los indicadores clave de seguridad para tener una visión consolidada del estado de la SST. | 8 |
| 40 | US38 | Visualización de Tendencias de Accidentabilidad | Como Gerente, quiero ver gráficas de tendencia de incidentes por mes para identificar si la accidentabilidad está mejorando o empeorando. | 5 |
| 41 | US40 | Seguimiento del Cumplimiento del Plan Anual de SST | Como Gerente, quiero ver el porcentaje de cumplimiento del plan anual de SST en tiempo real para detectar brechas antes de una inspección. | 5 |
| 42 | US41 | Visualización de Indicadores Predictivos de Riesgo | Como Gerente, quiero ver indicadores predictivos que anticipen posibles accidentes para justificar inversiones preventivas con datos concretos. | 8 |
| 43 | US39 | Exportación de Formatos de Auditoría para SUNAFIL | Como Gerente, quiero exportar automáticamente los formatos de auditoría exigidos por la Ley N° 29783 para prepararme ante inspecciones de SUNAFIL. | 8 |
| 44 | US45 | Generación de Reporte Mensual de Gestión de SST | Como Gerente, quiero generar un reporte mensual consolidado de seguridad con un solo clic para reducir el tiempo dedicado a informes manuales. | 5 |
| 45 | US42 | Notificación de Alerta Crítica No Resuelta a Gerencia | Como Gerente, quiero recibir una notificación cuando un riesgo crítico lleve más de 48 horas sin resolver para escalar el problema internamente. | 5 |
| 46 | US43 | Registro Histórico de Incidentes para Trazabilidad Legal | Como Gerente, quiero acceder al historial completo e inmutable de todos los incidentes para contar con evidencia ante auditorías de SUNAFIL. | 5 |
| 47 | US44 | Gestión de Cuentas de Usuario desde Administración | Como Administrador, quiero crear, editar y desactivar cuentas de usuario para mantener el control de acceso a la plataforma. | 5 |
| 48 | US46 | Configuración de niveles de riesgo | Como Administrador, quiero definir los niveles de riesgo del sistema para clasificar correctamente los incidentes detectados. | 3 |
| 49 | US47 | Configuración de umbrales de alerta | Como Administrador, quiero definir los umbrales de alerta del sistema para que se generen notificaciones cuando se superen ciertos valores. | 3 |
| 50 | US48 | Configuración de reglas de alertas | Como Administrador, quiero configurar reglas de generación de alertas para adaptar el comportamiento del sistema a distintos escenarios operativos. | 5 |
| 51 | US49 | Activación y desactivación de módulos del sistema | Como Administrador, quiero activar o desactivar módulos del sistema para personalizar su funcionamiento según las necesidades de la organización. | 3 |
| 52 | US50 | Configuración de horarios operativos | Como Administrador, quiero configurar los horarios de operación del sistema para adaptarlo a los turnos y jornadas laborales de la planta. | 3 |
| 53 | US51 | Registro de dispositivos | Como Administrador, quiero registrar dispositivos como sensores o cámaras para integrarlos al sistema de monitoreo. | 3 |
| 54 | US52 | Edición de dispositivos | Como Administrador, quiero editar la información de los dispositivos registrados para mantener sus datos actualizados. | 2 |
| 55 | US53 | Eliminación de dispositivos | Como Administrador, quiero eliminar dispositivos registrados para mantener el sistema sin información innecesaria. | 2 |
| 56 | US54 | Configuración de zonas de monitoreo | Como Administrador, quiero definir zonas de monitoreo dentro de la planta para segmentar las áreas según niveles de riesgo. | 3 |
| 57 | US55 | Configuración de parámetros del motor predictivo | Como Administrador, quiero configurar los parámetros del motor predictivo para mejorar la precisión en la detección de riesgos. | 5 |
| 58 | US56 | Configuración de prioridad de alertas | Como Administrador, quiero definir la prioridad de las alertas para atender primero las más críticas. | 3 |
| 59 | US57 | Configuración de notificaciones | Como Administrador, quiero configurar los canales de notificación del sistema para recibir alertas de forma oportuna. | 3 |
| 60 | US58 | Guardado de configuración del sistema | Como Administrador, quiero guardar los cambios realizados en la configuración para asegurar que los datos se mantengan persistentes. | 2 |
| 61 | US59 | Restaurar configuración por defecto | Como Administrador, quiero restaurar la configuración del sistema a sus valores por defecto para recuperar el funcionamiento original en caso de errores. | 2 |
| 62 | US60 | Visualización de configuración del sistema | Como Administrador, quiero visualizar la configuración actual del sistema para tener un control general de todos los parámetros definidos. | 2 |
| 63 | TS01 | Servicio de Notificaciones Push | Como desarrollador, quiero implementar el endpoint POST /api/v1/notificaciones/push para enviar alertas críticas en tiempo real a dispositivos móviles. | 8 |
| 64 | TS02 | Endpoint para Obtener Patrones de Riesgo Recurrentes | Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/patrones para mostrar alertas predictivas en el dashboard del supervisor. | 8 |
| 65 | TS03 | Endpoint para Obtener Datos del Mapa de Calor | Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/mapa-calor para alimentar el mapa de calor del dashboard en tiempo real. | 8 |
| 66 | TS04 | Endpoint para Obtener Riesgos Críticos Sin Atender | Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/no-atendidos para que el módulo de notificaciones escale automáticamente al supervisor. | 5 |
| 67 | TS05 | Endpoint para Marcar Alerta de Patrón como Revisada | Como desarrollador, quiero implementar el endpoint PATCH /api/v1/predictivo/alertas/{id}/revisada para retirar alertas del panel principal. | 3 |
| 68 | TS06 | Endpoint para Obtener Resumen Diario de Riesgos por Sector | Como desarrollador, quiero implementar el endpoint GET /api/v1/predictivo/resumen-diario para alimentar el panel de resumen del dashboard del supervisor. | 5 |
| 69 | TS07 | Endpoint de Cálculo de Matriz IPERC | Como desarrollador, quiero implementar el endpoint POST /api/v1/predictivo/iperc para calcular el nivel de criticidad del riesgo según la lógica IPERC. | 8 |
| 70 | TS08 | Endpoint para Obtener Indicadores del Dashboard Ejecutivo | Como desarrollador, quiero consumir el endpoint GET /api/v1/kpi_dashboard que retorna los indicadores clave de SST consolidados, para alimentar el tablero ejecutivo del gerente con datos actualizados en tiempo real. | 8 |
| 71 | TS09 | Endpoint para Obtener Tendencias Históricas de Accidentabilidad | Como desarrollador, quiero consumir el endpoint GET /api/v1/historical_trends que retorna la evolución mensual de incidentes agrupados por tipo y sector, para alimentar las gráficas de tendencia del tablero ejecutivo del gerente. | 8 |
| 72 | TS10 | Endpoint para Gestión de Reportes Generados | Como desarrollador, quiero consumir los endpoints GET y POST /api/v1/generated_reports y DELETE /api/v1/generated_reports/{id} para registrar, listar y eliminar reportes generados, mientras la generación del documento PDF o Excel se realiza en el cliente con jsPDF. | 8 |
| 73 | TS11 | Endpoint para Gestión de Alertas Críticas | Como desarrollador, quiero consumir los endpoints GET, PATCH y DELETE /api/v1/critical_alerts para listar, actualizar el estado y eliminar alertas críticas, para que el gerente pueda gestionar los riesgos no resueltos desde el tablero ejecutivo. | 5 |
| 74 | TS12 | Endpoint para Obtener el Plan Anual de SST y su Cumplimiento | Como desarrollador, quiero consumir el endpoint GET /api/v1/annual_ohs_plan que retorne el plan anual de SST con el porcentaje de cumplimiento global y el desglose por sector, para alimentar el indicador de seguimiento del tablero ejecutivo del gerente. | 5 |
| 75 | TS13 | Endpoint para Registro y Consulta de Inspecciones por Operario | Como desarrollador, quiero implementar los endpoints POST /api/v1/inspecciones y GET /api/v1/inspecciones/mine/{operarioId} para registrar inspecciones y consultar reportes por operario. | 8 |
| 76 | TS14 | Endpoint para Gestión de Catálogo de Peligros | Como desarrollador, quiero implementar los endpoints CRUD /api/v1/peligros para administrar el catálogo de tipos de peligro utilizados en inspecciones y evaluaciones de riesgo. | 5 |
| 77 | TS15 | Endpoint para Gestión de Sedes Operativas | Como desarrollador, quiero implementar los endpoints CRUD /api/v1/sedes para registrar, listar, actualizar y eliminar las sedes físicas de la planta industrial. | 5 |
| 78 | TS16 | Endpoint para Gestión de Áreas y Activos Industriales | Como desarrollador, quiero implementar los endpoints CRUD /api/v1/areas con filtro GET /active y /api/v1/activos con filtro GET /by-area/{areaId} para gestionar áreas y activos. | 8 |
| 79 | TS17 | Endpoint para Autenticación y Generación de Token JWT | Como desarrollador, quiero implementar los endpoints POST /api/v1/authentication/sign-in y sign-up para autenticar usuarios y generar tokens JWT con claims de rol. | 8 |
| 80 | TS18 | Endpoint para Gestión de Usuarios, Roles y Sesiones | Como desarrollador, quiero implementar los endpoints CRUD /api/v1/users, /api/v1/roles, /api/v1/sessions y /api/v1/access-logs para administrar cuentas, roles y auditoría. | 8 |
| 81 | TS19 | Endpoint para Gestión de Tickets, Técnicos y Mantenimiento Preventivo | Como desarrollador, quiero implementar los endpoints CRUD /api/v1/tickets, /api/v1/technicians, /api/v1/preventive-maintenances y /api/v1/assets para el dashboard del supervisor. | 8 |
| 82 | TS20 | Endpoint para Gestión de Zonas del Mapa de Calor y Reportes Archivados | Como desarrollador, quiero implementar los endpoints CRUD /api/v1/heat-map-zones y /api/v1/archived-reports para el dashboard de monitoreo del supervisor. | 5 |
| 83 | US01 | Autenticación de Operario | Como usuario, quiero iniciar sesión con mis credenciales asignadas para acceder a las funciones correspondientes a mi rol. | 3 |
| 84 | US02 | Cierre de Sesión del Operario | Como usuario, quiero cerrar sesión de forma segura para proteger mi cuenta en dispositivos compartidos. | 2 |
| 85 | US24 | Autenticación Segura de Supervisor | Como usuario, quiero iniciar sesión con mis credenciales preconfiguradas para acceder a las funciones de mi rol. | 3 |
| 86 | US36 | Autenticación Segura de Gerente o Administrador | Como usuario, quiero iniciar sesión con mis credenciales para acceder al dashboard ejecutivo. | 3 |
