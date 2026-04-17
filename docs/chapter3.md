# Capítulo III: Requirements Specification

## 3.1. User Stories

## Epics

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
        <td align="center"></td>
    </tr>
</table>


## User Stories
<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US01</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Autenticación de Operario</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero iniciar sesión en RiskGuard con mis credenciales asignadas, para acceder a las funciones correspondientes a mi rol.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El acceso debe realizarse mediante correo y contraseña preconfigurados.</li>
        <li>El sistema valida el formato del correo antes de enviar la petición.</li>
        <li>En caso de error, muestra el mensaje "Correo o contraseña incorrectos".</li>
        <li>Tras inicio de sesión exitoso, redirige al operario a su vista de funciones.</li>
        <li>Tras 5 intentos fallidos consecutivos, la cuenta se bloquea por 15 minutos.</li>
      </ol>
      <b>Escenario 1:</b> Inicio de sesión exitoso<br/>
      <ul>
        <li><b>Given</b> que el Operario se encuentra en la pantalla de inicio de sesión,</li>
        <li><b>When</b> ingresa su correo y contraseña correctos y hace clic en "Ingresar",</li>
        <li><b>Then</b> el sistema valida las credenciales,</li>
        <li><b>And</b> redirige al operario a su vista principal de funciones.</li>
      </ul>
      <b>Escenario 2:</b> Credenciales inválidas<br/>
      <ul>
        <li><b>Given</b> que el Operario se encuentra en la pantalla de inicio de sesión,</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US02</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Cierre de Sesión del Operario</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero cerrar sesión de forma segura desde la aplicación, para proteger mi cuenta en dispositivos compartidos del área de trabajo.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema incluye una opción de "Cerrar sesión" accesible desde el menú principal.</li>
        <li>Al cerrar sesión, el sistema invalida el token de autenticación del operario.</li>
        <li>Tras cerrar sesión, el sistema redirige al operario a la pantalla de inicio de sesión.</li>
        <li>Si el operario tiene un reporte en proceso no enviado, el sistema solicita confirmación antes de cerrar sesión.</li>
      </ol>
      <b>Escenario 1:</b> Cierre de sesión exitoso<br/>
      <ul>
        <li><b>Given</b> que el Operario se encuentra en cualquier pantalla de la aplicación,</li>
        <li><b>When</b> hace clic en "Cerrar sesión" desde el menú,</li>
        <li><b>Then</b> el sistema invalida su token de autenticación,</li>
        <li><b>And</b> redirige al operario a la pantalla de inicio de sesión.</li>
      </ul>
      <b>Escenario 2:</b> Cierre con reporte en proceso<br/>
      <ul>
        <li><b>Given</b> que el Operario tiene un formulario de reporte con datos ingresados sin enviar,</li>
        <li><b>When</b> intenta cerrar sesión,</li>
        <li><b>Then</b> el sistema muestra el mensaje "Tienes un reporte sin enviar. ¿Deseas salir de todas formas?",</li>
        <li><b>And</b> ofrece las opciones "Continuar reportando" y "Salir sin guardar".</li>
      </ul>
      <b>Escenario 3:</b> Intento de acceso tras cerrar sesión<br/>
      <ul>
        <li><b>Given</b> que el Operario cerró sesión correctamente,</li>
        <li><b>When</b> intenta acceder a una URL protegida directamente,</li>
        <li><b>Then</b> el sistema detecta que no hay token válido,</li>
        <li><b>And</b> redirige automáticamente a la pantalla de inicio de sesión.</li>
      </ul>
    </td>
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US03</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Registro Rápido de Casi-Accidente</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero registrar un casi-accidente desde mi celular en menos de 30 segundos, para asegurarme de que la información llegue al sistema sin interrumpir mi flujo de trabajo.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El formulario tiene un máximo de 4 campos obligatorios: tipo de incidente, sector, descripción breve y nivel de urgencia.</li>
        <li>El sistema muestra el formulario en menos de 2 segundos tras hacer clic en "Nuevo Reporte".</li>
        <li>Al enviar, el sistema confirma la recepción con un mensaje visible de éxito.</li>
        <li>El reporte queda registrado con fecha, hora y usuario automáticamente.</li>
        <li>El operario puede acceder al formulario desde la pantalla principal sin pasos previos.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US04</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Adjuntar Evidencia Fotográfica al Reporte</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero adjuntar una foto desde mi celular al momento de reportar un incidente, para proporcionar evidencia visual que facilite la evaluación del riesgo por parte del supervisor.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El formulario de reporte incluye un botón opcional para adjuntar foto.</li>
        <li>El sistema acepta imágenes en formato JPG o PNG con un tamaño máximo de 5 MB.</li>
        <li>Si la imagen supera el tamaño permitido, el sistema muestra un mensaje de error claro.</li>
        <li>La imagen queda vinculada al reporte y visible para el supervisor en el detalle del ticket.</li>
        <li>El operario puede eliminar la foto adjunta antes de enviar el reporte.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US05</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Selección de Sector al Registrar Incidente</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero seleccionar el sector de la planta donde ocurrió el incidente al momento de reportarlo, para que el sistema pueda georreferenciar el riesgo correctamente y el supervisor identifique la zona afectada.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El formulario incluye un campo de selección con la lista de sectores activos registrados en el sistema.</li>
        <li>El sistema no muestra sectores con estado "Inactivo" en la lista.</li>
        <li>El sector es un campo obligatorio para enviar el reporte.</li>
        <li>El sector seleccionado queda registrado en el ticket del incidente.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US06</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Selección del Nivel de Urgencia del Incidente</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero indicar el nivel de urgencia del incidente que estoy reportando, para que el sistema priorice correctamente la alerta hacia el supervisor.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El formulario incluye un campo de selección con tres niveles: Bajo, Medio y Alto.</li>
        <li>El nivel de urgencia es un campo obligatorio para enviar el reporte.</li>
        <li>El nivel seleccionado queda registrado en el ticket y determina la prioridad de la alerta generada.</li>
        <li>Los niveles están diferenciados visualmente por color: verde, amarillo y rojo.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US07</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Selección del Tipo de Incidente</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero seleccionar el tipo de incidente de una lista predefinida al momento de reportar, para categorizar correctamente el riesgo y facilitar el análisis posterior del sistema.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El formulario incluye un campo de selección con tipos predefinidos: Condición insegura, Casi-accidente, Falla de equipo, Riesgo ergonómico, Riesgo químico y Otro.</li>
        <li>El tipo de incidente es obligatorio para enviar el reporte.</li>
        <li>El tipo seleccionado queda registrado en el ticket y es usado por el motor de reglas para calcular el nivel de riesgo.</li>
        <li>Si se selecciona "Otro", se habilita un campo de texto adicional obligatorio.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US08</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Registro de Condición Insegura Vinculada a un Activo</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero vincular mi reporte a un activo específico de la planta, para indicar con precisión qué máquina o equipo presenta la condición insegura.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El formulario incluye un campo opcional para vincular el reporte a un activo del sector seleccionado.</li>
        <li>La lista de activos se filtra automáticamente según el sector elegido.</li>
        <li>Solo se muestran activos con estado "Activo".</li>
        <li>Si no se selecciona activo, el reporte se registra igualmente vinculado solo al sector.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US09</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Descripción de Texto Libre en el Reporte</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero ingresar una descripción en texto libre al momento de reportar un incidente, para detallar con mis propias palabras lo que observé y dar más contexto al supervisor.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El formulario incluye un campo de texto libre con un límite de 300 caracteres.</li>
        <li>El campo muestra un contador de caracteres restantes en tiempo real.</li>
        <li>La descripción es obligatoria para enviar el reporte.</li>
        <li>El sistema no permite enviar una descripción con solo espacios en blanco.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US10</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Confirmación de Recepción del Reporte</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero recibir una confirmación visible después de enviar mi reporte, para saber que la información llegó correctamente al sistema y no quedó perdida.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema muestra un mensaje de confirmación inmediatamente después del envío exitoso.</li>
        <li>La confirmación incluye el número de ticket asignado al reporte.</li>
        <li>En caso de fallo en el envío, el sistema muestra un mensaje de error con opción de reintentar.</li>
        <li>La confirmación permanece visible hasta que el operario la cierre manualmente.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US11</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Notificación de Atención del Reporte</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero recibir una notificación cuando mi reporte haya sido revisado o atendido por el supervisor, para saber que mi reporte tuvo un impacto real y no fue ignorado.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema envía una notificación al operario cuando el supervisor cambia el estado del ticket a "En Progreso" o "Resuelto".</li>
        <li>La notificación muestra el número de ticket y el nuevo estado asignado.</li>
        <li>Las notificaciones se acumulan en un centro de notificaciones accesible desde la pantalla principal.</li>
        <li>El operario puede marcar las notificaciones como leídas.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US12</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Historial de Reportes del Operario</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero consultar el historial de los reportes que he enviado, para hacer seguimiento del estado de cada uno y verificar que fueron atendidos.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema muestra únicamente los reportes enviados por el operario autenticado.</li>
        <li>Cada entrada del historial muestra: número de ticket, fecha, sector, tipo de incidente y estado actual.</li>
        <li>El operario puede filtrar su historial por estado: Pendiente, En Progreso o Resuelto.</li>
        <li>El operario puede acceder al detalle completo de cada reporte haciendo clic sobre él.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US13</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Consulta del Detalle de un Reporte Enviado</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero ver el detalle completo de un reporte que envié, para conocer la descripción registrada, el sector, la foto adjunta y el estado actual de atención.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El detalle muestra todos los campos ingresados al momento del reporte.</li>
        <li>Si se adjuntó foto, esta se muestra en el detalle.</li>
        <li>El estado actual del ticket se muestra de forma destacada con color según nivel.</li>
        <li>Si el ticket fue resuelto, se muestra la descripción de la acción correctiva tomada.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US14</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Visualización de Alertas Activas en el Sector</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero ver las alertas activas en mi sector al ingresar a la aplicación, para estar informado de los riesgos identificados en mi zona de trabajo antes de iniciar mi turno.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>La pantalla principal muestra un resumen de alertas activas del sector asignado al operario.</li>
        <li>Cada alerta indica tipo de riesgo, nivel de urgencia y estado actual.</li>
        <li>Las alertas se muestran ordenadas por nivel de urgencia de mayor a menor.</li>
        <li>Si no hay alertas activas en el sector, el sistema muestra el mensaje "Tu sector opera dentro de los parámetros seguros".</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US15</td>
    <td><b>Epic ID</b></td><td>EP01</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Edición de Reporte Antes del Envío</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como Operario de Planta, quiero poder revisar y corregir los datos de mi reporte antes de enviarlo, para asegurarme de que la información registrada es precisa y completa.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El operario puede modificar cualquier campo del formulario antes de hacer clic en "Enviar".</li>
        <li>Los cambios se reflejan en tiempo real en el formulario.</li>
        <li>El sistema no guarda datos parciales hasta que el operario confirme el envío.</li>
        <li>El operario puede cancelar el reporte en cualquier momento antes del envío.</li>
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
  </tr>
</table>

---


<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US16</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Visualización de Métricas de Impacto Predictivo</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">
      Como visitante, quiero visualizar indicadores reales de siniestralidad y beneficios del sistema en la Landing Page de RiskGuard, para comprender el impacto de la analítica predictiva en la reducción de riesgos industriales.
    </td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema muestra métricas reales como 50%, 83% y 90.7% relacionadas a reducción de accidentes y mejora del clima laboral.</li>
        <li>Las métricas se presentan en formato visual mediante tarjetas o gráficos.</li>
        <li>La sección está ubicada dentro del flujo principal del landing.</li>
        <li>El contenido es visible sin necesidad de autenticación.</li>
        <li>La visualización es responsive para desktop y dispositivos móviles.</li>
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
  </tr>
</table>

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US17</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Interacción con Botones de Conversión</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">
      Como visitante, quiero interactuar con los botones “Iniciar prueba gratuita” y “Hablar con ventas”, para contactar con el servicio de RiskGuard.
    </td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>Debe existir al menos un CTA visible en el landing.</li>
        <li>El sistema redirige correctamente al hacer clic.</li>
        <li>Funciona en desktop y móvil.</li>
        <li>Registra la interacción del usuario.</li>
        <li>Debe permitir múltiples clics sin error.</li>
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
  </tr>
</table>

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US18</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Visualización de Alerta por Riesgo Recurrente en sector</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como supervisor de seguridad, quiero recibir una alerta cuando el mismo tipo de riesgo se repita más de 3 veces en 30 días en una misma sector, para intervenir antes de que ocurra un accidente.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema detecta automáticamente cuando un mismo tipo de riesgo supera 3 ocurrencias en una misma sector dentro de los últimos 30 días.</li>
        <li>La alerta muestra el tipo de riesgo, el sector afectada, el número de ocurrencias y la fecha del primer reporte del período.</li>
        <li>La alerta es visible en el dashboard principal sin necesidad de buscarla.</li>
        <li>Si el riesgo tiene menos de 3 ocurrencias en el período, el sistema no genera ninguna alerta de recurrencia.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US19</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Visualización de Mapa de Calor de Riesgos de la Planta</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como supervisor de seguridad, quiero ver un mapa de calor actualizado de la planta con la concentración de riesgos activos por zona, para priorizar mis recursos de inspección donde más se necesitan.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El mapa muestra todas las sectors de la planta con un color que representa su nivel de concentración de riesgos activos</li>
        <li>Las sectors con mayor concentración de riesgos críticos se destacan con la intensidad de color más alta.</li>
        <li>Al hacer clic en un sector del mapa, el sistema muestra el detalle de los riesgos activos de esa zona.</li>
        <li>El mapa se actualiza automáticamente cuando se registra un nuevo riesgo o se resuelve uno existente.</li>
        <li>Si ninguna sector tiene riesgos activos, todas las zonas aparecen en el nivel de intensidad más bajo con un mensaje informativo.</li>
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
  </tr>
</table>

---
<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US20</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Notificación de Riesgo Crítico Sin Atender</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como supervisor de seguridad, quiero que el sistema me notifique cuando un riesgo crítico lleve más de 24 horas sin ser atendido, para escalar la situación a gerencia a tiempo.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema evalúa periódicamente los riesgos críticos activos y verifica si tienen acción correctiva asignada.</li>
        <li>Cuando un riesgo crítico supera las 24 horas sin acción correctiva asignada, el sistema envía una notificación al supervisor de seguridad.</li>
        <li>La notificación indica el nombre del sector, el tipo de riesgo y el tiempo transcurrido desde su registro.</li>
        <li>Si el riesgo tiene acción correctiva asignada dentro del plazo, no se genera ninguna notificación de escalamiento.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>US21</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Filtrado de Patrones de Riesgo por Tipo de Peligro</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como supervisor de seguridad, quiero filtrar los patrones de riesgo detectados por tipo de peligro (físico, químico, ergonómico, otros), para analizar de forma segmentada cuál categoría representa mayor amenaza en la planta.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El panel de patrones incluye un filtro por tipo de peligro con las categorías: físico, químico, ergonómico, otros.</li>
        <li>Al aplicar el filtro, el sistema muestra únicamente los patrones recurrentes de la categoría seleccionada.</li>
        <li>Si no existen patrones de la categoría seleccionada en el período, el sistema muestra un mensaje informativo.</li>
        <li>El supervisor de seguridad puede combinar el filtro de tipo de peligro con el selector de sector.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>TS22</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Servicio de Notificaciones Push</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como desarrollador, quiero implementar el endpoint POST /api/v1/notificaciones/push para enviar alertas críticas en tiempo real a los dispositivos móviles.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El sistema envía notificaciones push en tiempo real.</li>
        <li>Integra servicios externos (Firebase, etc.).</li>
        <li>Maneja reintentos automáticos.</li>
        <li>Permite cola de mensajes si el usuario está offline.</li>
        <li>Registra cada envío en logs.</li>
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
  </tr>
</table>


---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>TS23</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Endpoint para Obtener Patrones de Riesgo Recurrentes</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/patrones que devuelva los patrones de riesgo recurrentes por sector y período, para mostrar las alertas predictivas en el dashboard del supervisor de seguridad.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El endpoint GET /api/v1/predictivo/patrones acepta el identificador del sector y el número de días como parámetros de consulta obligatorios.</li>
        <li>El endpoint retorna los patrones detectados con tipo de riesgo, frecuencia de ocurrencia y fecha de primera ocurrencia en el período.</li>
        <li>Si el sector no tiene registros suficientes, el endpoint retorna una respuesta HTTP 200 con lista vacía y un mensaje descriptivo.</li>
        <li>Si el sector enviada no existe en el sistema, el endpoint retorna HTTP 404 indicando que el recurso no fue encontrado.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>TS24</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Endpoint para Obtener Datos del Mapa de Calor</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/mapa-calor que retorne la concentración de riesgos activos por sector clasificada por nivel de intensidad, para alimentar el mapa de calor del dashboard en tiempo real.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El endpoint GET /api/v1/predictivo/mapa-calor retorna todas las sectores registradas con su nivel de intensidad calculado</li>
        <li>El nivel de intensidad se calcula en base a la cantidad de riesgos activos sin resolver de cada sector.</li>
        <li>Si ninguna sector tiene riesgos activos, el endpoint retorna todas las sectors con nivel de intensidad bajo y HTTP 200.</li>
        <li>El endpoint no requiere parámetros adicionales y retorna siempre el estado actual de toda la planta.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>TS25</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Endpoint para Obtener Riesgos Críticos Sin Atender</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como desarrollador, quiero consumir el endpoint GET /api/v1/predictivo/no-atendidos que retorne los riesgos críticos sin acción correctiva asignada que superen el tiempo indicado, para que el módulo de notificaciones escale automáticamente al supervisor de seguridad.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El endpoint GET /api/v1/predictivo/no-atendidos acepta el número de horas como parámetro obligatorio para definir el umbral de tiempo sin atención.</li>
        <li>El endpoint retorna los riesgos críticos activos sin acción correctiva que superen el umbral, incluyendo sector, tipo de riesgo, nivel de criticidad y horas transcurridas sin atención.</li>
        <li>Si todos los riesgos han sido atendidos dentro del plazo, el endpoint retorna HTTP 200 con lista vacía.</li>
        <li>Si el parámetro de horas no es enviado o tiene un valor inválido, el endpoint retorna HTTP 400 indicando que el parámetro es requerido.</li>
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
  </tr>
</table>

---

<table align="center">
  <tr>
    <td><b>User Story ID</b></td><td>TS26</td>
    <td><b>Epic ID</b></td><td>EP02</td>
  </tr>
  <tr>
    <td><b>Título</b></td>
    <td colspan="3">Endpoint de Cálculo de Matriz IPERC</td>
  </tr>
  <tr>
    <td><b>Descripción</b></td>
    <td colspan="3">Como desarrollador, quiero implementar el endpoint POST /api/v1/predictivo/iperc que reciba los índices de probabilidad y severidad, para calcular el nivel de criticidad del riesgo según la lógica IPERC del sistema.</td>
  </tr>
  <tr>
    <td colspan="4">
      <b>Criterios de aceptación:</b>
      <ol>
        <li>El endpoint recibe los parámetros <b>probability_index</b> y <b>severity_index</b>.</li>
        <li>El sistema valida que los valores estén dentro del rango permitido.</li>
        <li>Se calcula el nivel de riesgo.</li>
        <li>Se retorna el color asociado al nivel de riesgo.</li>
        <li>El tiempo de respuesta es menor a 2 segundos.</li>
        <li>Se manejan errores de validación y errores internos.</li>
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
  </tr>
</table>

---
<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US01</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Autenticación Segura de Supervisor</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b>Como Supervisor de Seguridad, quiero iniciar sesión en la plataforma utilizando mis credenciales preconfiguradas, para acceder a las funciones establecidas de acuerdo mi rol</td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El acceso debe realizarse obligatoriamente mediante un correo y contraseña previamente establecidos en la base de datos durante el despliegue del sistema.</li>
                <li>El sistema debe validar en el frontend que el correo tenga un formato válido antes de enviar la petición.</li>
                <li>En caso de error de autenticación, el sistema debe mostrar el mensaje indicando "Correo o contraseña incorrectos" .</li>
                <li>Las contraseñas en la base de datos deben estar encriptadas (hasheadas).</li>
                <li>Tras un inicio de sesión exitoso, el sistema debe generar un token de seguridad y redirigir al supervisor a la pantalla de funciones segun su rol</li>
                <li>Como medida de seguridad, tras 5 intentos fallidos de inicio de sesión consecutivos, la cuenta debe bloquearse temporalmente por 15 minutos</li>
            </ol>
            <b>Escenario 1:</b> Inicio de sesión exitoso<br/>
            <ul>
                <li><b>Given</b> que el Supervisor se encuentra en la pantalla de inicio de sesión de RiskGuard</li>
                <li><b>When</b> ingresa su correo corporativo preconfigurado y su contraseña correcta,</li>
                <li><b>And</b> hace clic en el botón "Ingresar",</li>
                <li><b>Then</b> el sistema valida las credenciales,</li>
                <li><b>And</b> autoriza el acceso y redirige al usuario a la vista principal en donde se encuentran sus funciones como supervisor</li>
            </ul>
            <b>Escenario 2:</b> Intento fallido por credenciales inválidas<br/>
            <ul>
                <li><b>Given</b> que el Supervisor se encuentra en la pantalla de inicio de sesión de RiskGuard</li>
                <li><b>When</b> ingresa alguna credencial de manera incorrecta</li>
                <li><b>And</b> hace clic en el botón "Ingresar",</li>
                <li><b>Then</b> el sistema deniega el acceso a la plataforma,</li>
                <li><b>And</b> muestra una mensaje indicando "Correo o contraseña incorrectos", manteniendo los campos limpios para un nuevo intento.</li>
            </ul>
            <b>Escenario 3:</b> Bloqueo preventivo por múltiples intentos fallidos consecutivos<br/>
            <ul>
                <li><b>Given</b> que el Supervisor intenta acceder al sistema,</li>
                <li><b>When</b> acumula 5 intentos de autenticación fallidos consecutivos,</li>
                <li><b>And</b> hace clic en el botón "Ingresar",</li>
                <li><b>Then</b> el sistema bloquea temporalmente las peticiones para ese usuario,</li>
                <li><b>And</b> muestra el mensaje indicando "Demasiados intentos fallidos. Por favor, intente nuevamente en 15 minutos".</li>
            </ul>
        </b></td>
    </tr>
</table>

---

<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US02</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Configuración de Sectores y Áreas Operativas</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3">Como Supervisor de Seguridad, quiero administrar y gestionar los sectores fisicos de la planta, para georreferenciar correctamente las incidencias reportadas y organizar el catálogo de activos.</b></td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema debe contar con un módulo de "Gestión de Sectores" accesible desde el apartado de funciones de Supervisor de seguridad</li>
                <li>El formulario de creación debe solicitar obligatoriamente nombre del sector y descripcion</li>
                <li>El sistema debe validar que no se puedan registrar dos sectores con el mismo nombre exacto para evitar conflictos en la base de datos</li>
                <li>Los sectores creados deben listarse en una tabla con opciones para "Editar" o "Desactivar".</li>
                <li>Un sector no se puede eliminar definitivamente si tiene historial de riesgos asociados; solo se puede cambiar su estado a "Inactivo" para que no aparezca en los nuevos formularios de los operarios</li>
            </ol>
            <b>Escenario 1:</b> Registro exitoso de nuevo scetor<br/>
            <ul>
                <li><b>Given</b> que el Supervisor se encuentra en el módulo de "Gestión de Sectores",</li>
                <li><b>When</b> hace clic en "Nuevo Sector", ingresa un nombre en especifico y una descripcion,</li>
                <li><b>Then</b> el sistema registra el nuevo sector en la base de datos con estado "Activo",</li>
                <li><b>And</b> actualiza la tabla de sectores mostrando el nuevo sector en la primera fila</li>
            </ul>
            <b>Escenario 2:</b> Validación de sector duplicado<br/>
            <ul>
                <li><b>Given</b> que el Supervisor se encuentra en el módulo de "Gestión de Sectores",</li>
                <li><b>When</b> hace clic en "Nuevo Sector", ingresa un nombre en especifico y una descripcion,</li>
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
        </b></td>
    </tr>
</table>

---

<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US03</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Configuración y Gestión de Activos Industriales</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3">Como Supervisor de Seguridad, quiero registrar y administrar la maquinaria y equipos de la planta, para vincularlos a su scetor operativo correspondiente y permitir la asignación precisa de reportes de inspección a cada activo</b></td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema requiere obligatoriamente un código identificador único, nombre, descripción y el identificador de un sector previamente registrado para crear un nuevo activo</li>
                <li>El sistema rechaza el registro o actualización de un activo si el sector de destino se encuentra en estado "Inactivo"</li>
                <li>El sistema valida la unicidad del código identificador en toda la base de datos antes de procesar el registro de un nuevo activo.</li>
                <li>El sistema permite la actualización de los datos del activo, incluyendo su transferencia o reubicación hacia un sector diferente que se encuentre activo</li>
                <li>El sistema cambio de estado a "Inactivo" en lugar de una eliminación total cuando se solicita remover un activo que posee historial de inspecciones previas</li>
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
        </b></td>
    </tr>
</table>

---

<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US04</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Gestión y Administración de Personal Técnico</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3">Como Supervisor de Seguridad, quiero registrar y administrar al personal de mantenimiento en el sistema, para disponer de una lista actualizada de técnicos calificados a quienes delegar los tickets de acción correctiva</b></td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema requiere obligatoriamente el número de documento de identidad, nombres completos, especialidad técnica y estado operativo ("Activo" o "Inactivo") para procesar el registro de un nuevo técnico.</li>
                <li>El sistema rechaza el registro de un nuevo técnico si el número de documento de identidad ingresado ya existe en la base de datos.</li>
                <li>El sistema permite la actualización de los datos de contacto y la especialidad del personal técnico registrado.</li>
                <li>El sistema cambia de estado a "Inactivo" en lugar de una eliminación total cuando el supervisor da de baja a un técnico, preservando la integridad del historial de los tickets que resolvió en el pasado.</li>
                <li>El sistema filtra y expone exclusivamente al personal en estado "Activo" durante el proceso de asignación de tickets de acción correctiva</li>
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
        </b></td>
    </tr>
</table>

---

<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US05</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Asignación de Tickets de Acción Correctiva</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3">Como Supervisor de Seguridad, quiero asignar un ticket de incidente a un técnico de mantenimiento específico, para delegar la responsabilidad de la reparación y cambiar el estado de la alerta a un proceso de mitigación activo.</b></td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema requiere obligatoriamente el identificador de un técnico de mantenimiento con estado "Activo" para procesar la asignación del ticket</li>
                <li>El sistema actualiza automáticamente el estado del ticket de "Pendiente" a "En Progreso" una vez que la asignación es procesada con éxito</li>
                <li>El sistema registra de forma inmutable la fecha, hora y el identificador del técnico asignado en el historial de trazabilidad del ticket.</li>
                <li>El sistema permite la reasignación de un ticket que se encuentra "En Progreso" hacia un técnico diferente, registrando el cambio en el historial.</li>
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
        </b></td>
    </tr>
</table>

---

<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US06</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Exploración Sectorizada y Filtrado de Alertas Activas</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b>Como Supervisor de Seguridad, quiero acceder a las alertas activas seleccionando previamente un sector específico, para enfocar mi análisis en un sector a la vez y aplicar filtros de riesgo sobre sus incidentes correspondientes.</td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema requiere la selección de un sector físico válido (previamente registrado) antes de desplegar la lista de alertas activas.</li>
                <li>El sistema recupera y despliega exclusivamente los tickets de incidentes que están referenciados al sector previamente seleccionado.</li>
                <li>El sistema permite aplicar filtros secundarios sobre los resultados del sector, basándose en el nivel de riesgo y el estado de resolución del ticket </li>
                <li>El sistema actualiza el conjunto de resultados del sector en evaluación cuando se modifican los parámetros de filtrado secundario.</li>
                <li>El sistema retorna un mensaje de estado informativo cuando el sector seleccionado no posee alertas activas o cuando los filtros secundarios aplicados no producen coincidencias</li>
            </ol>
            <b>Escenario 1:</b> Acceso a un sector con múltiples alertas<br/>
            <ul>
                <li><b>Given</b> que el supervisor necesita evaluar una zona específica de la planta,</li>
                <li><b>When</b> selecciona un sector en especifico para su exploración,</li>
                <li><b>Then</b> el sistema procesa la solicitud y retorna únicamente los tickets de incidentes asociados a dicho sector,</li>
                <li><b>And</b> mantiene ocultas las alertas pertenecientes a otras áreas operativas</li>
            </ul>
            <b>Escenario 2:</b> Filtrado dentro de un sector específicos<br/>
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
        </b></td>
    </tr>
</table>

<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US07</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Verificación y Cierre de Medidas de Control</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b>Como Supervisor de Seguridad, quiero evaluar la efectividad de las medidas correctivas implementadas, para garantizar que el riesgo ha sido mitigado satisfactoriamente antes de proceder al cierre definitivo del incidente en el sistema</td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema permite el proceso de verificación exclusivamente para aquellos tickets que se encuentran en estado "Medida Implementada".</li>
                <li>El sistema requiere la selección de un veredicto final (Aprobación o Rechazo) para completar la evaluación de la medida de control.</li>
                <li>El sistema valida el ingreso de un comentario de justificación técnica únicamente cuando el veredicto seleccionado es un rechazo</li>
                <li>El sistema actualiza el estado del ticket a "Cerrado" y registra la marca de tiempo final cuando se procesa una aprobación.</li>
                <li>El sistema revierte el estado del ticket a "En Progreso" cuando se procesa un rechazo, manteniendo la vinculación con el técnico responsable para su reevaluación.</li>
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
                <li><b>And</b> emite una mensaje indicando que le falto sustentar el motivo del rechazo.</li>
            </ul>
        </b></td>
    </tr>
</table>
<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US08</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Visualización del Mapa de Calor Operativo</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b>Como Supervisor de Seguridad, quiero visualizar la distribución de los niveles de riesgo de los sectores de la planta, para identificar de forma inmediata qué sectores requieren intervención prioritaria</td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema recupera el último nivel de criticidad (IPERC) calculado por el motor predictivo para todos los sectores físicos registrados en estado "Activo"</li>
                <li>El sistema clasifica cada sector evaluado cruzando su puntaje de riesgo con los umbrales del sistema</li>
                <li>El sistema asigna un indicador paramétrico de estado (clasificación visual) a cada sector basándose exclusivamente en el nivel de riesgo más alto de los incidentes activos en esa ubicación.</li>
                <li>El sistema permite la selección de un sector específico dentro de la visualización espacial para recuperar y exponer el listado de tickets activos que originan su estado actual</li>
                <li>El sistema procesa la disminución del nivel de alerta de un sector automáticamente cuando todos los tickets críticos asociados a dicha ubicación alcanzan el estado "Cerrado"</li>
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
        </b></td>
    </tr>
</table>

<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US09</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3">Notificación Externa Automática por Incidentes Críticos</b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b>Como Supervisor de Seguridad, quiero recibir notificaciones automáticas a través de canales externos cuando el sistema registre un incidente de riesgo crítico, para garantizar un tiempo de respuesta inmediato ante emergencias sin requerir un monitoreo activo de la plataforma</td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li>El sistema ejecuta el envío automático de un mensaje de alerta a la dirección de correo configurada del supervisor inmediatamente después de la creación de un ticket con nivel de riesgo "Critico"</li>
                <li>El sistema incluye en el cuerpo del mensaje el identificador del ticket, la clasificación del riesgo, el nombre del sector afectado y la marca de tiempo del incidente.</li>
                <li>El sistema omite la ejecución del protocolo de notificación externa cuando los incidentes evaluados poseen un nivel de riesgo diferente a "Critico"</li>
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
        </b></td>
    </tr>
</table>



## 3.2. Impact Mapping



## 3.3. Product Backlog
