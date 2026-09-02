# 📄 Planeación del Sistema

## Desglose de trabajo: Épicas, Historias de Usuario y Tareas

La implementación de los requerimientos identificados de TechCup se desglosa de la siguiente manera:

### 1. Épica:

| Campo | Descripción |
|------|-------------|
| **ID** | EP-01 |
| **Título** | Gestion de equipos e inscripcion a torneos |
| **Descripción** | TechCup nesecita esta epica para permitir que los capitanes creen y administren sus equipos, los inscriban en el torneo activo y realicen el pago de la inscripcion mediante PSE, mientras los organizadores validan dichos pagos y aprueban las inscripciones. Esto centraliza el proceso de registro, que hoy no existe de forma sistematizada en la Escuela. |
| **Stakeholder** | Organizadores del torneo (Decanatura de Ingenieria de Sistemas) |

### 2. Historias de usuario:

| Campo | Descripción |
|------|-------------|
| **ID** | HU-01 |
| **Título** | Crear o sleccionar equipo |
| **Descripción** | COMO Capitan, QUIERO crear un nuevo equipo o seleccionar uno ya registrado, PARA PODER inscribirlo en el torneo activo en el periodo academico actual. |
| **Prioridad** | *[Baja]* *[Media]* *[Alta]* |
| **Estimación** | ** |

| Campo | Descripción |
|------|-------------|
| **ID** | HU-02 |
| **Título** | Registrar equipo en el torneo activo |
| **Descripción** | Como capitán, quiero registrar mi equipo en el torneo que se encuentra activo, para asegurar su participación en la competencia y asegurar nuestro cupo frente a los organizadores y logistica del torneo. |
| **Prioridad** | *[Baja]* *[Media]* *[Alta]* |
| **Estimación** | ** |

| Campo | Descripción |
|------|-------------|
| **ID** | HU-03 |
| **Título** | Pagar inscripcion mediante PSE |
| **Descripción** | COMO capitan QUIERO pagar el valor de la inscripcion de mi equipo a traves de PSE, PARA PODER completar el proceso de registro en el torneo atraves de la plataforma bancaria de mi preferencia. |
| **Prioridad** | *[Baja]* *[Media]* *[Alta]* |
| **Estimación** | *13* |
**Video de Planning Poker:** https://youtu.be/nrVU0FgRNZI

| Campo | Descripción |
|------|-------------|
| **ID** | HU-04 |
| **Título** | Validar pago y aprobar inscripcion |
| **Descripción** | COMO organizador QUIERO revisar y validar el pago realizado por un equipo, PARA PODER aprobar su inscripcion en el torneo y tenerlo en cuenta en la planeacion y logistica del torneo. |
| **Prioridad** | *[Baja]* *[Media]* *[Alta]* |
| **Estimación** | *13* |

### 3. Tareas:

| Campo | Descripción |
|------|-------------|
| **ID** | TR-01 |
| **Título** | Diseñar interfaz de creacion/seleccion de equipo |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | Diseñar la pantalla donde el capitan puede crear un equipo nuevo o ver/seleccionar equipos ya existentes. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-02 |
| **Título** | Implementar creacion de equipo(backend) |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | Desarrollar el endpoint y la logica para registrar un nuevo equipo en el sistema. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-03 |
| **Título** | Implementar listado/seleccion de equipos |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | Desarrollar la funcionalidad para consultar y seleccionar equipos previamente creados por el capitan. |
| **Tareas requisito** | TR-02 |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-04 |
| **Título** | Validar existencia de torneo activo |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | Implementatar la verificacion de que exista un torneo en estado Active antes de permitir la inscripcion. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-05 |
| **Título** | Mostrar informacion del torneo y valor de inscripcion |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | Desarrollar la vista que muestra al capitan los datos del torneo activo y el costo de la incripcion. |
| **Tareas requisito** | TR-04 |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-06 |
| **Título** | Implementar registo del equipo al torneo |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | Desarrollar la logica que asocia el equipo seleccionado con el torneo activo, validando que cumpla las condiciones de inscripcion  |
| **Tareas requisito** | TR-04, TR-02 |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-07 |
| **Título** | Integrar pasarela de pago PSE |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | Configurar e integrar el servicio de pagos PSE en el sistema |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-08 |
| **Título** | Implementar procesamiento y registro del pago |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | Desarrollar la logica para procesar la respuesta de PSE y almacenar la informacion del pago asociado al equipo. |
| **Tareas requisito** | TR-07, TR-06 |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-09 |
| **Título** | Notificar confirmacion de pago al capitan |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | Implementar la notificacion/mensaje de confirmacion mostrado al capitan tras completar el pago. |
| **Tareas requisito** | TR-08 |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-10 |
| **Título** | Implementar vista de revision de pagos |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | Desarrollar la pantalla donde el organizador puede consultar los pagos realizados por cada equipo. |
| **Tareas requisito** | TR-08 |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-11 |
| **Título** | Implementar validacion y aprobacion de inscripcion |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | Desarrollar la logica que permite al organizador aprobar o rechazar la incripcion segun la validez del pago. |
| **Tareas requisito** | TR-10 |

| Campo | Descripción |
|------|-------------|
| **ID** | TR-12 |
| **Título** | Registrar estado final de inscripcion |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | Implementar el guardado del estado final de la inscripcion (aprobada o rechazada) en el sistema. |
| **Tareas requisito** | TR-11 |
