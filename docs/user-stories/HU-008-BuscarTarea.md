# HU-008-Buscar tareas específicas

## Historia de usuario

Como integrante del equipo, quiero buscar una tarea específica, para localizarla rápidamente entre las tareas registradas.

## Criterios de Aceptación

### CA-001 - Buscar por título

Given que existen tareas registradas
And el usuario proporciona un término de búsqueda
When realiza la búsqueda
Then deben mostrarse las tareas cuyo título coincida con el término de búsqueda

### CA-002 - Coincidencia parcial

Given que existe una tarea cuyo título contiene el término buscado
When el usuario realiza la búsqueda
Then la tarea debe aparecer entre los resultados

### CA-003 - Búsqueda sin resultados

Given que existen tareas registradas
And ninguna coincide con el término de búsqueda
When el usuario realiza la búsqueda
Then no deben mostrarse tareas que no coincidan
And debe informarse que no se encontraron resultados

### CA-004 - Búsqueda vacía

Given que existen tareas registradas
When el usuario realiza una búsqueda sin proporcionar un término
Then deben mostrarse las tareas disponibles

### CA-005 - La búsqueda no modifica las tareas

Given que existen tareas registradas
When el usuario realiza una búsqueda
Then únicamente debe cambiar la visualización de los resultados
And ninguna tarea debe modificarse

## Reglas del Negocio

RN-001: La búsqueda debe utilizar la información existente de las tareas.

RN-002: La búsqueda debe permitir coincidencias parciales en el título.

RN-003: Las tareas que no coincidan con el término buscado no deben mostrarse como resultados.

RN-004: Una búsqueda sin término debe permitir consultar nuevamente las tareas disponibles.

RN-005: Buscar una tarea no debe modificar sus datos.

## Dependencias

Esta historia depende funcionalmente de:

* HU-001 - Crear una tarea.
* HU-004 - Consultar el estado de las tareas.

## Fuera de Alcance

* Búsqueda avanzada
* Búsqueda por múltiples criterios
* Búsqueda por descripción
* Búsqueda por usuario
* Búsqueda por fecha
* Búsqueda por prioridad
* Ordenamiento de resultados
