# Requisitos funcionales, no funcionales y reglas de negocio

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

RNF1 - Navegadores compatibles
- La plataforma debe funcionar correctamente en los navegadores modernos más utilizados (Chrome, Firefox, Edge y Safari).
El diseño debe ser responsive y usable en pantallas de diferentes tamaños.


### RNF2 - Rendimiento y tiempos de respuesta
- Las operaciones habituales (cargar agenda, consultar servicios, crear una reserva…) deben completarse en menos de 2 segundos bajo carga normal.
Las acciones que dependan de servicios externos (correo o pasarela de pago) deben mostrar feedback al usuario mientras se procesan.


### RNF3 - Seguridad de acceso y contraseñas
- Las contraseñas deben almacenarse mediante hashing seguro.
El sistema debe proteger el acceso a zonas privadas mediante autenticación obligatoria y validar sesiones activas.


### RNF4 - Protección de datos personales
- Los datos de clientes y profesionales deben tratarse siguiendo buenas prácticas de privacidad.
El acceso a los datos de las cuentas solo debe permitirse a su propietario o al administrador en casos justificados (soporte técnico).


### RNF5 - Persistencia y consistencia de datos
- Toda la información de usuarios, citas, pagos, disponibilidad y facturas debe almacenarse en una base de datos SQLite de forma persistente, garantizando la integridad de las relaciones y evitando solapes en las reservas.


### RNF6 - Disponibilidad del servicio
- El sistema debe ser capaz de funcionar sin fallos críticos en la lógica principal (registro, reservas, paneles y agenda) durante el uso normal por parte de clientes y profesionales.


### RNF7 - Conexión con servicios externos
- La comunicación con la pasarela de pago (modo test) y el servicio de correo debe realizarse mediante llamadas seguras y controladas, gestionando errores y respuestas inesperadas.


### RNF8 - Mantenibilidad y modularidad del código
- El backend debe estar estructurado por módulos (usuarios, agenda, servicios, pagos, facturas) para facilitar ampliaciones futuras sin alterar el funcionamiento existente.
- El proyecto debe estar versionado mediante Git y organizado en ramas y commits descriptivos.


### RNF9 - Usabilidad y experiencia de usuario
- La navegación debe ser clara, con menús diferenciados para clientes y profesionales.
- Los paneles deben mostrar información organizada (calendario, historial, facturas) y ofrecer mensajes claros ante errores o acciones incompletas.


### RNF10 - Automatismos sin intervención manual
- Los procesos automáticos (recordatorios, cancelaciones por falta de pago, generación de facturas) deben ejecutarse sin intervención del profesional, garantizando consistencia entre citas, pagos y facturas.


### RNF11 - Escalabilidad básica
- Aunque la versión inicial utiliza SQLite, la arquitectura debe permitir migrar en el futuro a otro gestor de base de datos sin reescribir toda la aplicación.

## 4.3 Reglas de Negocio

### RN1. Una cita solo puede reservarse en un hueco disponible
Una cita solo puede crearse dentro de los intervalos generados automáticamente según la disponibilidad configurada por el profesional.


### RN2. No puede haber solapamiento de citas
El sistema debe impedir que se reserven dos citas que ocupen parcial o totalmente el mismo slot de tiempo para un mismo profesional.


### RN3. El precio de la sesión depende del servicio configurado
El importe de cualquier pago se calcula exclusivamente a partir de los datos del servicio (precio, duración y modalidad).


### RN4. Una cita solo pasa a estado “confirmada” tras un pago correcto
Las citas en modo test se confirman únicamente si la pasarela responde “pago correcto”.


### RN5. La política de cancelación del profesional determina si hay reembolso
El sistema debe aplicar las reglas configuradas por el profesional (horas mínimas de aviso, reembolso total o sin reembolso).


### RN6. Cada pago está asociado a exactamente una cita
Un pago no puede relacionarse con múltiples citas ni existir sin referencia a una cita.


### RN7. Cada factura está asociada a exactamente un pago
Una factura sólo se genera automáticamente cuando existe un pago confirmado.


### RN8. El administrador no puede modificar datos críticos
El administrador únicamente puede consultar datos o corregir aspectos menores para diagnóstico, sin alterar reservas, pagos ni facturas.


### RN9. Un usuario puede tener uno o varios roles
Un mismo usuario puede actuar como cliente y profesional, pero mantiene una única cuenta.


### RN10. El sistema genera notificaciones automáticamente según eventos
Los recordatorios, confirmaciones, cancelaciones automáticas y facturas deben generarse sin intervención manual.
