# Requisitos funcionales y no funcionales

Este documento recoge los requisitos funcionales y no funcionales de la plataforma de gestión de citas para profesionales autónomos y pequeñas empresas.

---

## 1. Requisitos funcionales

A continuación se describen los principales requisitos funcionales del sistema.

En esta sección se detallan las funciones que debe ofrecer la plataforma para cumplir su propósito básico: permitir a profesionales y clientes gestionar citas con pago integrado, dentro de unas reglas de agenda y cancelación configurables.

### RF1. Registro de profesionales
- El sistema permite que un profesional se registre creando una cuenta con sus datos básicos y acceder posteriormente a su panel privado.

### RF2. Registro de clientes
- El sistema permite que un cliente cree una cuenta para poder reservar citas, acceder a su panel y consultar su historial.

### RF3. Autenticación y cambio de modo
- El sistema permite iniciar sesión como cliente o como profesional y, en cuentas con ambos roles, cambiar de modo desde el propio panel sin crear usuarios duplicados.

### RF4. Gestión del perfil profesional
- El profesional puede configurar y actualizar su perfil público (nombre o marca, logo, descripción breve, datos de contacto visibles, dirección profesional cuando proceda).

### RF5. Gestión de datos de cuenta y datos fiscales
- El profesional puede modificar sus datos internos de cuenta (correo, contraseña, idioma, zona horaria) e introducir los datos fiscales necesarios para la facturación.
El cliente puede actualizar sus datos de perfil y de acceso.

### RF6. Gestión de servicios
- El profesional puede crear, modificar, desactivar o reactivar los servicios que ofrece, definiendo nombre, duración, modalidad (online/presencial) y precio.

### RF7. Configuración de disponibilidad y reglas de agenda
- El profesional puede definir su disponibilidad semanal, descansos mínimos, bloqueos puntuales (festivos, vacaciones, ausencias) y límites básicos de agenda.

### RF8. Generación de huecos reservables
- El sistema genera automáticamente los huecos de agenda disponibles en función de la configuración del profesional y de las citas ya registradas, evitando solapes.

### RF9. Exploración y búsqueda de profesionales
- El cliente puede explorar el listado de profesionales disponibles y filtrarlos por criterios básicos (tipo de servicio, modalidad, rango de precios, idioma, etc.), así como acceder a su perfil público.

### RF10. Reserva de cita por parte del cliente
- El cliente puede seleccionar un servicio, elegir fecha y hora dentro de los huecos disponibles e introducir sus datos para crear una reserva en estado pendiente de pago o confirmación.

### RF11. Gestión de citas desde el panel del profesional
- El profesional puede consultar su calendario, crear citas manuales para un cliente concreto, modificar o cancelar reservas existentes, marcar citas como realizadas y añadir notas internas simples.

### RF12. Gestión de citas desde el panel del cliente
El cliente puede consultar sus próximas citas y su historial, así como modificar o cancelar reservas dentro de los límites establecidos por la política del profesional.

### RF13. Procesamiento de pagos online
- El sistema permite que el cliente realice el pago a través de la pasarela configurada. Solo se confirma definitivamente una cita cuando el pago se completa correctamente; el sistema registra el estado del pago.

### RF14. Aplicación de política de cancelación y reembolso
- Cuando una cita pagada se modifica o cancela, el sistema aplica automáticamente la política configurada por el profesional (plazos, reembolsos totales o parciales, pérdida de importe, etc.) y actualiza el estado del pago.

### RF15. Generación y consulta de facturas
- Cuando una cita pasa a estado pagada o completada, el sistema genera una factura asociada.
El profesional puede consultar el historial de facturas y descargarlas o enviarlas al cliente, y el cliente puede descargar sus propias facturas desde su panel.

### RF16. Notificaciones automáticas
- El sistema envía correos automáticos de confirmación, recordatorio y avisos de cambio o cancelación al cliente y al profesional, según el estado de cada cita.

### RF17. Historial y trazabilidad básica
- El sistema mantiene el historial de citas, pagos y facturas de cada profesional y cliente, de forma que puedan consultarse desde los paneles correspondientes.

### RF18. Gestión básica por parte del administrador
- El administrador puede crear cuentas de profesionales en casos excepcionales, activar o desactivar usuarios (clientes o profesionales) y consultar de forma agregada la actividad del sistema (citas, pagos, incidencias) para tareas de supervisión y soporte.

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
