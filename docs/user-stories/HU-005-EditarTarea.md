# HU-005-Editar información de una tarea

## Historia de usuario

Como integrante del equipo, quiero editar la información de una tarea existente, para corregir o actualizar sus datos cuando sea necesario.

## Criterios de Aceptación

### CA-001 - Editar correctamente

Given que existe una tarea registrada
And el usuario proporciona información válida
When solicita editar la tarea
Then la información de la tarea debe actualizarse correctamente

### CA-002 - Tarea inexistente

Given que no existe la tarea que el usuario desea editar
When intenta editarla
Then la tarea no debe modificarse
And debe informarse que la tarea no existe

### CA-003 - Título obligatorio

Given que el usuario desea editar una tarea
And elimina el título
When intenta guardar los cambios
Then la tarea no debe actualizarse
And debe informarse que el título es obligatorio

### CA-004 - Longitud mínima del título

Given que el usuario proporciona un título con menos de 3 caracteres
When intenta guardar los cambios
Then la tarea no debe actualizarse
And debe informarse que el título no cumple con la longitud mínima

### CA-005 - Longitud máxima del título

Given que el usuario proporciona un título con más de 80 caracteres
When intenta guardar los cambios
Then la tarea no debe actualizarse
And debe informarse que el título no cumple con la longitud máxima

### CA-006 - Descripción opcional

Given que existe una tarea registrada
And el usuario elimina la descripción
When guarda los cambios
Then la tarea debe actualizarse correctamente

### CA-007 - Descripción demasiado extensa

Given que el usuario proporciona una descripción mayor a 300 caracteres
When intenta guardar los cambios
Then la tarea no debe actualizarse
And debe informarse la restricción correspondiente

## Reglas del Negocio

RN-001: Solo pueden editarse tareas existentes.

RN-002: Toda tarea debe conservar un título válido.

RN-003: El título debe contener entre 3 y 80 caracteres.

RN-004: La descripción es opcional.

RN-005: La descripción tendrá como máximo 300 caracteres.

RN-006: La identificación de la tarea no debe cambiar al editarla.

RN-007: El estado de la tarea debe conservarse al editar su información.

## Dependencias

Esta historia depende funcionalmente de:

* HU-001 - Crear una tarea.

## Fuera de Alcance

* Cambiar el estado de una tarea
* Asignar tareas a personas
* Fechas límite
* Prioridades
* Categorías
* Archivos adjuntos
* Subtareas
* Notificaciones
