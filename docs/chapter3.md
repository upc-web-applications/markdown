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
        <td align="center"></td>
    </tr>
    <tr>
        <td align="center"><b>EP02</b></td>
        <td align="center"></td>
    </tr>
    <tr>
        <td align="center"><b>EP03</b></td>
        <td align="center">Gestión de Alertas y Mitigación de Incidentes</td>
    </tr>
    <tr>
        <td align="center"><b>EP04</b></td>
        <td align="center"></td>
    </tr>
    <tr>
        <td align="center"><b>EP05</b></td>
        <td align="center"></td>
    </tr>
</table>

## User Stories

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
<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US04</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b></td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3"></b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b></td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ol>
            <b>Escenario 1 </b> <br/>
            <ul>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
            </ul>
        </b></td>
    </tr>
</table>
<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US05</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b>Gestión de Alertas y Mitigación de Incidentes</td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3"></b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b></td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ol>
            <b>Escenario 1 </b> <br/>
            <ul>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
            </ul>
        </b></td>
    </tr>
</table>
<table align="center">
    <tr>
        <td><b>User Story ID</b></td>
        <td>US06</b></td>
        <td><b>Epic ID</b></td>
        <td>EP03</b>Gestión de Alertas y Mitigación de Incidentes</td>
    </tr>
    <tr>
        <td><b>Título</b></td>
        <td colspan="3"></b></td>
    </tr>
    <tr>
        <td><b>Descripción</b></td>
        <td colspan="3"></b></td>
    </tr>
    <tr>
        <td colspan="4">
            <b>Criterios de aceptación:</b> <br/>
            <ol>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ol>
            <b>Escenario 1 </b> <br/>
            <ul>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
                <li><b></b> </li>
            </ul>
        </b></td>
    </tr>
</table>



## 3.2. Impact Mapping



## 3.3. Product Backlog
