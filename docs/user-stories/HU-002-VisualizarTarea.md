# HU-002-VisualizarTarea

## Historia de usuario
Como integrante del equipo, quiero visualizar las tareas registradas, para conocer rápidamente qué tareas existen. 

## Criterios de Aceptación 
### CA-001 - Visualizar las tareas
Given que el usuario registró una tarea
When el usuario quiera saber qué tareas tiene
Then se desplegará el registro de tareas

### CA-002 - MOstrar estados y fecha de entrega
Given que el usuario quiere conocer que tareas tiene
And no recuerda el estado de la tarea
When se despliegue el registro de tareas
Then las tareas tambien deben mostrar su estado y su ID
And mostrar las fechas de creacion y entrega 

## Reglas del Negocio
RN-001: Todas las tareas deben tener estado.
RN-002: Todas las tareas deben tener titulo.
RN-003: Todas las tareas deben tener fecha de entrega.
RN-004: Cada tarea debe de poder identificarse de manera unica.
RN-005: Debe conocerse cuando fue creada la tarea.

## Dependencias
Esta historia de usuario depende funcionalmente de HU-001-CrearTarea.

## Fuera de Alcance
* Asignar tareas a personas
* Archivos adjuntos
* SubTareas

 
