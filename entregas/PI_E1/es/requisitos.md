# Requisitos funcionales y no funcionales

Este documento recoge los requisitos funcionales y no funcionales de la plataforma de gestión de citas para profesionales autónomos y pequeñas empresas.

---

## 1. Requisitos funcionales

A continuación se describen los principales requisitos funcionales del sistema.

### RF1 – Gestión de profesionales

- El sistema permitirá que un profesional se registre y pueda iniciar sesión de forma segura.
- El sistema permitirá que el profesional recupere o restablezca su contraseña mediante un mecanismo controlado (por ejemplo, enlace de recuperación por correo).

### RF2 – Perfil profesional

- El sistema permitirá que el profesional edite su perfil (nombre, descripción, especialidad, datos de contacto básicos).
- El sistema mostrará una versión pública del perfil, accesible para los clientes sin autenticación.

### RF3 – Gestión de servicios

- El sistema permitirá que el profesional defina los servicios que ofrece (nombre, duración, precio, modalidad presencial/online).
- El sistema permitirá activar o desactivar servicios sin necesidad de eliminarlos definitivamente.

### RF4 – Gestión de disponibilidad

- El sistema permitirá que el profesional configure su disponibilidad (días y franjas horarias).
- El sistema permitirá bloquear días completos o franjas concretas (vacaciones, festivos, horas no disponibles).
- El sistema generará huecos reservables en función de la disponibilidad y la duración de los servicios.

### RF5 – Visualización y reserva de citas por parte del cliente

- El sistema permitirá que el cliente seleccione un servicio disponible de un profesional.
- El sistema mostrará al cliente las franjas horarias libres en función del servicio elegido.
- El sistema permitirá que el cliente introduzca sus datos básicos (nombre, correo electrónico) para completar la reserva.
- El sistema registrará la cita en el calendario del profesional.

### RF6 – Modificación y cancelación de citas

- El sistema permitirá que el profesional consulte el listado de citas y su detalle.
- El sistema permitirá que el profesional cancele una cita o la marque como no disponible.
- El sistema permitirá que el cliente cancele o solicite cambio de cita dentro de las políticas definidas (por ejemplo, con una antelación mínima).

### RF7 – Integración con pasarela de pago (modo test)

- El sistema permitirá iniciar un proceso de pago asociado a una reserva de cita.
- El sistema recibirá la confirmación (éxito o error) de la pasarela de pago en modo test.
- El sistema registrará el estado del pago asociado a la cita (pendiente, pagado, error).

### RF8 – Notificaciones y recordatorios

- El sistema enviará un correo de confirmación al cliente tras completar la reserva.
- El sistema enviará un recordatorio de la cita al cliente con una antelación configurable.
- El sistema podrá notificar al profesional nuevas reservas, cambios o cancelaciones.

### RF9 – Panel de control del profesional

- El sistema mostrará al profesional un calendario con sus citas programadas.
- El sistema permitirá filtrar citas por fecha, estado (pendiente, realizada, cancelada) y servicio.
- El sistema mostrará un resumen básico de actividad (número de citas en un periodo, servicios más reservados, etc.) en versiones futuras.

---

## 2. Requisitos no funcionales

### RNF1 – Usabilidad

- La interfaz será sencilla y coherente, pensada para usuarios no técnicos.
- La plataforma será accesible desde los principales navegadores modernos.
- Se priorizará un flujo de reserva claro para minimizar errores del usuario.

### RNF2 – Rendimiento

- Las páginas principales (perfil del profesional y flujo de reserva) deberán cargarse en un tiempo razonable en conexiones domésticas estándar.
- Las operaciones comunes (consultar disponibilidad, crear una reserva) deberán completarse en pocos segundos, salvo incidencias externas (pasarela de pago, correo).

### RNF3 – Seguridad

- El acceso al panel del profesional estará protegido mediante autenticación.
- Las contraseñas se almacenarán cifradas (hash) en la base de datos.
- La comunicación con la aplicación deberá realizarse preferentemente sobre HTTPS en el entorno de despliegue.
- No se almacenarán datos completos de tarjeta en la aplicación; el pago se gestionará a través de la pasarela externa.

### RNF4 – Fiabilidad e integridad de datos

- El sistema deberá evitar dobles reservas para el mismo hueco y servicio.
- Las operaciones de creación, modificación y cancelación de citas deberán mantener la coherencia entre calendario, disponibilidad y estado del pago.
- En caso de error de la pasarela de pago, la cita quedará marcada como no pagada o pendiente de confirmación.

### RNF5 – Mantenibilidad

- El código del backend se organizará en módulos claros (gestión de agenda, pagos, notificaciones, etc.).
- Se documentarán a alto nivel los endpoints principales de la API y la estructura básica de la base de datos.
- Se utilizarán tecnologías estándar (Python, Flask/FastAPI, SQLite) para facilitar la futura evolución del proyecto.

### RNF6 – Escalabilidad básica

- Aunque se use SQLite en el TFG, el diseño permitirá migrar a otro motor de base de datos si fuese necesario (por ejemplo, PostgreSQL).
- La separación entre frontend, API y base de datos facilitará, en el futuro, la distribución de la carga.

### RNF7 – Cumplimiento legal (orientativo)

- El sistema deberá contemplar el uso de datos personales de acuerdo con la normativa vigente (por ejemplo, RGPD).
- Se informará al usuario del uso de sus datos personales en el contexto de la reserva de citas.
- El almacenamiento de datos se limitará a la información necesaria para la gestión de las citas y la facturación.
