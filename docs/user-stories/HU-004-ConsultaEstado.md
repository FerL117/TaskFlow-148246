# HU-004-Consultar el estado de las tareas

## Historia de usuario

Como integrante del equipo, quiero consultar las tareas y conocer su estado actual, para identificar la situación de las actividades pendientes y realizadas.

## Criterios de Aceptación

### CA-001 - Visualizar tareas

Given que existen tareas registradas
When el usuario consulta las tareas
Then deben mostrarse las tareas disponibles
And debe mostrarse el estado actual de cada tarea

### CA-002 - Mostrar estado Pendiente

Given que existe una tarea con estado Pendiente
When el usuario consulta las tareas
Then la tarea debe mostrar el estado Pendiente

### CA-003 - Mostrar estado Completada

Given que existe una tarea con estado Completada
When el usuario consulta las tareas
Then la tarea debe mostrar el estado Completada

### CA-004 - Consultar sin tareas registradas

Given que no existen tareas registradas
When el usuario consulta las tareas
Then no debe mostrarse una tarea inexistente
And debe informarse que no existen tareas registradas

### CA-005 - Información consistente

Given que existen tareas registradas
When el usuario consulta las tareas
Then cada tarea debe mostrar su información correspondiente
And el estado mostrado debe coincidir con el estado actual de la tarea

## Reglas del Negocio

RN-001: Toda tarea registrada debe tener un estado.

RN-002: Una tarea nueva inicia con estado Pendiente.

RN-003: El estado de cada tarea debe poder identificarse visualmente.

RN-004: La consulta debe mostrar únicamente tareas existentes.

RN-005: El estado mostrado debe corresponder al estado actual de la tarea.

## Dependencias

Esta historia depende funcionalmente de:

* HU-001 - Crear una tarea.

## Fuera de Alcance

* Filtrar tareas por estado
* Buscar tareas específicas
* Editar información de una tarea
* Eliminar tareas
* Ordenar tareas
* Asignar tareas a personas
* Prioridades
