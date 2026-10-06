# HU-001-Crear una tarea

## Historia de usuario
Como integrante del equipo, quiero registrar una nueva tarea con titulo y descripción, para documentar el trabajo que quiero realizar.

## Criterios de Aceptación 
### CA-001 - Crear Correctamente
Given que el usuario proporciona el título valido
When solicita crear la tarea
Then la tarea debe agregarse
And debe de iniciar con un estado Pendiente

### CA-002 - Titulo Obligatorio
Given que el usuario desea crear una tarea
And no proporciona el titulo
When intenta registrar la tarea
Then la tarea no debe ser creada
And debe recibir información indicando que el título es obligatorio

### CA-003 - Longitud mínima del título
Given que el usuario desea crear una tarea
And proporciona un titulo con menos de 3 caracteres 
When intenta registrar la tarea
Then la tarea no debe ser creada
And debe informarse que el titulo no cumple con la longitud minima

### CA-004 - Longitud maxima del titulo
Given que el usuario desea crear una tarea
And proporciona un titulo con mas de 80 caracteres 
When intenta registrar la tarea
Then la tarea no debe ser creada
And debe informarse que el titulo no cumple con la longitud maxima

### CA-005 - Descripcion opcional
Given que el usuario proporciona un titulo valido
And no proporciona descripcion 
When registra la tarea
Then la tarea debe crearse correctamente

### CA-006 - Descripcion demasiado extensa
Given que el usuario proporciona una descripcion mayor a 300 caracteres 
When intenta crear la tarea
Then la tarea no debe ser creada
And debe informarse la restriccion correspondiente

## Reglas del Negocio
RN-001: Todas las tareas deben tener titulo.
RN-002: El titulo debe contener entre 3 y 80 caracteres.
RN-003: La descripcion es opcional.
RN-004: La descripcion tendra como maximo 300 caracteres.
RN-005: Toda tarea nueva inicia como Pendiente.
RN-006: Cada tarea debe de poder identificarse de manera unica.
RN-007: Debe conocerse cuando fue creada la tarea.

## Dependencias
Esta historia de usuario no depende funcionalmente de otra HU.

## Fuera de Alcance
* Asignar tareas a personas
* Fechas Limite
* Prioridades
* Categorías
* Archivos adjuntos
* SubTareas
* Notificaciones
 
