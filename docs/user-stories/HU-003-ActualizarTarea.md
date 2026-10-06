# HU-003-ActualizarTarea

## Historia de usuario
Como integrante del equipo, quiero actualizar el estado de una tarea, para reflejar el progreso actual de cada actividad.

## Criterios de Aceptación 
### CA-001 - Actualizar Estado de la tarea
Given que el usuario quiere cambiar el estado de una tarea
When solicite cambiar el estado de una tarea
Then la tarea debe cambiar al estado que el usuario seleccione
And debe de reflejarse en el registro de tareas

### CA-002 - Estados Permitidos
Given que el usuario desea cambiar el estado
And los estados son Pendiente, Completado y Cancelado
When el usuario seleccione una de esas opciones
Then la tarea debe ser actualizada
And reflejarse en el registro de tareas

### CA-002 - Estados Permitidos
Given que el usuario cambio el estado de la tarea
Then el usuario debe recibir una notificacion de que la tarea se modifico correctamente
And agregar una fecha de modificacion a la tarea

## Reglas del Negocio
RN-001: Todas las tareas deben tener estado.
RN-002: Toda tarea nueva inicia como Pendiente.
RN-003: Cada tarea debe de poder identificarse de manera unica.
RN-004: Debe conocerse cuando fue modificada la tarea.

## Dependencias
Esta historia de usuario depende funcionalmente de HU-001-CrearTarea.

## Fuera de Alcance
* Asignar tareas a personas
* Fechas Limite
* Prioridades
* SubTareas
* Notificaciones
 
