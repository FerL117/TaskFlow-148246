# HU-006-Eliminar una tarea

## Historia de usuario

Como integrante del equipo, quiero eliminar una tarea que ya no necesita seguimiento, para mantener únicamente las actividades relevantes.

## Criterios de Aceptación

### CA-001 - Eliminar correctamente

Given que existe una tarea registrada
When el usuario solicita eliminarla
Then la tarea debe dejar de aparecer entre las tareas disponibles

### CA-002 - Tarea inexistente

Given que la tarea indicada no existe
When el usuario intenta eliminarla
Then no debe modificarse ninguna otra tarea
And debe informarse que la tarea no existe

### CA-003 - Confirmación de eliminación

Given que existe una tarea registrada
When el usuario solicita eliminarla
Then debe solicitarse confirmación antes de eliminarla

### CA-004 - Cancelar eliminación

Given que existe una tarea registrada
And el usuario solicita eliminarla
When el usuario cancela la eliminación
Then la tarea debe conservarse
And debe permanecer disponible para consulta

### CA-005 - Eliminar únicamente la tarea seleccionada

Given que existen varias tareas registradas
When el usuario elimina una tarea específica
Then únicamente la tarea seleccionada debe eliminarse
And las demás tareas deben conservarse

## Reglas del Negocio

RN-001: Solo pueden eliminarse tareas existentes.

RN-002: La eliminación debe afectar únicamente a la tarea seleccionada.

RN-003: La eliminación debe requerir confirmación del usuario.

RN-004: Una tarea eliminada no debe aparecer en la consulta de tareas.

RN-005: Cancelar la eliminación debe conservar la tarea sin modificaciones.

## Dependencias

Esta historia depende funcionalmente de:

* HU-001 - Crear una tarea.

## Fuera de Alcance

* Eliminación masiva
* Recuperación de tareas eliminadas
* Papelera de reciclaje
* Historial de eliminaciones
* Confirmación mediante usuario o contraseña
* Auditoría de cambios
