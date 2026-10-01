# SPEC-000 — Foundation

## 1. Propósito

Establecer la base técnica y organizativa de **TaskFlow Lite**, definiendo su estructura inicial, tecnologías, restricciones y convenciones de desarrollo.

Esta especificación busca proporcionar una base mínima y consistente para desarrollar posteriormente las funcionalidades del producto de manera incremental.

## 2. Alcance

Esta SPEC contempla únicamente la configuración inicial del proyecto:

* Definir la estructura de directorios y archivos base.
* Establecer el uso de HTML5, CSS3 y JavaScript ES Modules.
* Preparar el proyecto para una futura persistencia mediante LocalStorage.
* Definir convenciones básicas para Git.
* Establecer criterios técnicos mínimos para considerar terminada la fase Foundation.
* Permitir la ejecución local del proyecto desde VSCode.

No se implementarán todavía historias funcionales ni capacidades propias de la gestión de tareas.

## 3. Estructura inicial del proyecto

La estructura propuesta será:

```text
TaskFlow-Lite/
├── src/
│   ├── index.html
│   ├── css/
│   │   └── styles.css
│   └── js/
│       └── main.js
├── .gitignore
└── README.md
```

### Responsabilidad inicial

* `src/index.html`: documento HTML principal de la aplicación.
* `src/css/styles.css`: estilos globales iniciales.
* `src/js/main.js`: punto de entrada JavaScript mediante ES Modules.
* `.gitignore`: archivos y directorios que no deben incluirse en Git.
* `README.md`: información básica para ejecutar y comprender el proyecto.

La estructura podrá evolucionar mediante futuras SPECs conforme se incorporen funcionalidades.

## 4. Restricciones técnicas

* Utilizar **HTML5** para la estructura de la interfaz.
* Utilizar **CSS3** para la presentación visual.
* Utilizar **JavaScript ES Modules** para la lógica del cliente.
* No utilizar frameworks frontend.
* No utilizar backend.
* No utilizar bases de datos externas.
* La persistencia futura se realizará mediante **LocalStorage**.
* El proyecto deberá poder ejecutarse localmente desde **VSCode**.
* El código fuente de la aplicación deberá mantenerse dentro de `src/`.
* No se implementarán historias funcionales durante esta fase.
* Las funcionalidades deberán incorporarse posteriormente de manera incremental.

## 5. Convenciones de Git

Se utilizará Git para controlar las versiones del proyecto.

### Convención de commits

Los commits deberán utilizar prefijos descriptivos:

* `feat:` — incorporación de una funcionalidad.
* `fix:` — corrección de un defecto.
* `docs:` — modificación de documentación.
* `style:` — cambios de formato o estilos sin modificar comportamiento.
* `refactor:` — reorganización del código sin cambiar su comportamiento.
* `chore:` — tareas de mantenimiento o configuración.

Ejemplos:

```text
docs: agregar SPEC-000 foundation
feat: agregar registro de tareas
fix: corregir actualización de estado
```

Los commits deberán representar cambios pequeños y coherentes, evitando mezclar funcionalidades diferentes en un mismo commit.

## 6. Definition of Done técnica inicial

La fase Foundation se considerará terminada cuando:

* [ ] La estructura inicial del proyecto esté creada.
* [ ] El proyecto utilice HTML5, CSS3 y JavaScript ES Modules.
* [ ] No existan frameworks ni backend.
* [ ] `src/` contenga el código fuente de la aplicación.
* [ ] El proyecto pueda abrirse y ejecutarse localmente desde VSCode.
* [ ] La aplicación cargue correctamente su HTML, CSS y JavaScript.
* [ ] Git esté configurado para el proyecto.
* [ ] Exista un `.gitignore` apropiado.
* [ ] Exista documentación inicial en `README.md`.
* [ ] La especificación `SPEC-000-foundation.md` esté documentada.
* [ ] No se hayan implementado historias ni funcionalidades de negocio.

## 7. Fuera de alcance

Durante esta fase quedan explícitamente fuera de alcance:

* Registro de tareas.
* Edición de tareas.
* Eliminación de tareas.
* Actualización de estados.
* Búsqueda o filtrado de tareas.
* Persistencia funcional mediante LocalStorage.
* Autenticación de usuarios.
* Backend o API.
* Base de datos.
* Frameworks frontend.
* Integraciones con servicios externos.
* Despliegue en producción.
* Historias de usuario funcionales.

Estas capacidades podrán abordarse posteriormente mediante SPECs o historias independientes.
