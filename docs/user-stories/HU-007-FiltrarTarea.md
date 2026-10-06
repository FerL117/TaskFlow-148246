# HU-007-Filtrar tareas por estado

## Historia de usuario

Como integrante del equipo, quiero filtrar las tareas por estado, para encontrar rápidamente las actividades que se encuentran en una situación determinada.

## Criterios de Aceptación

### CA-001 - Filtrar tareas Pendientes

Given que existen tareas con estado Pendiente
When el usuario selecciona el filtro Pendiente
Then deben mostrarse únicamente las tareas con estado Pendiente

### CA-002 - Filtrar tareas Completadas

Given que existen tareas con estado Completada
When el usuario selecciona el filtro Completada
Then deben mostrarse únicamente las tareas con estado Completada

### CA-003 - Mostrar todas las tareas

Given que existen tareas registradas
When el usuario selecciona la opción para mostrar todas
Then deben mostrarse las tareas independientemente de su estado

### CA-004 - Sin resultados

Given que existen tareas registradas
And ninguna coincide con el estado seleccionado
When el usuario aplica el filtro
Then no deben mostrarse tareas que no correspondan
And debe informarse que no existen tareas con ese estado

### CA-005 - El filtro no modifica las tareas

Given que existen tareas registradas
When el usuario aplica un filtro
Then únicamente debe cambiar la visualización de las tareas
And las tareas no deben modificarse

## Reglas del Negocio

RN-001: El filtro debe utilizar el estado actual de cada tarea.

RN-002: El filtro Pendiente debe mostrar únicamente tareas pendientes.

RN-003: El filtro Completada debe mostrar únicamente tareas completadas.

RN-004: La opción Todos debe mostrar todas las tareas existentes.

RN-005: Filtrar no debe modificar la información de las tareas.

## Dependencias

Esta historia depende funcionalmente de:

* HU-001 - Crear una tarea.
* HU-004 - Consultar el estado de las tareas.

## Fuera de Alcance

* Filtrar por múltiples criterios
* Filtrar por fecha
* Filtrar por prioridad
* Filtrar por categoría
* Filtrar por usuario
* Ordenamiento de tareas
