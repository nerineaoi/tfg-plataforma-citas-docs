# Casos de uso / Funcionalidades principales

A continuación se describen los principales casos de uso del sistema de gestión de citas para profesionales autónomos y pequeñas empresas.

---

## CU1 — Registrarse como profesional

**Actor:** Profesional  
**Descripción:** El profesional crea una cuenta en la plataforma proporcionando sus datos básicos.  
**Resultado:** El sistema registra al nuevo profesional y permite iniciar sesión.

---

## CU2 — Iniciar sesión

**Actor:** Profesional  
**Descripción:** El profesional introduce sus credenciales para acceder a su panel.  
**Resultado:** Acceso al panel del profesional si las credenciales son correctas.

---

## CU3 — Editar perfil profesional

**Actor:** Profesional  
**Descripción:** El profesional modifica su información pública (nombre, descripción, especialidad, datos de contacto).  
**Resultado:** Perfil actualizado y visible para los clientes.

---

## CU4 — Gestionar servicios

**Actor:** Profesional  
**Descripción:** El profesional crea, modifica o desactiva los servicios que ofrece.  
**Resultado:** Servicios actualizados y disponibles para los clientes.

---

## CU5 — Configurar disponibilidad

**Actor:** Profesional  
**Descripción:** El profesional establece su horario (días, franjas, descansos, bloqueos).  
**Resultado:** El sistema genera huecos reservables según la disponibilidad definida.

---

## CU6 — Ver calendario de citas

**Actor:** Profesional  
**Descripción:** El profesional consulta sus próximas citas y su detalle.  
**Resultado:** Acceso al calendario con filtrado básico (fecha, estado, servicio).

---

## CU7 — Cancelar o modificar una cita

**Actor:** Profesional  
**Descripción:** El profesional cancela una cita o la marca como no disponible.  
**Resultado:** La cita queda actualizada y se notifican los cambios al cliente.

---

## CU8 — Consultar perfil del profesional (cliente)

**Actor:** Cliente  
**Descripción:** El cliente accede a la página pública del profesional sin necesidad de registrarse.  
**Resultado:** Visualización de información, servicios y disponibilidad general.

---

## CU9 — Reservar una cita

**Actor:** Cliente  
**Descripción:** El cliente selecciona un servicio, elige un hueco disponible e introduce sus datos.  
**Resultado:** La cita queda registrada y se envía un correo de confirmación.

---

## CU10 — Realizar un pago (modo test)

**Actor:** Cliente  
**Descripción:** Tras reservar, el cliente realiza el pago mediante la pasarela configurada (modo test).  
**Resultado:** La pasarela devuelve un estado (éxito/error) y el sistema actualiza la cita.

---

## CU11 — Cancelar cita como cliente

**Actor:** Cliente  
**Descripción:** El cliente cancela la cita según las políticas establecidas (por ejemplo, con antelación mínima).  
**Resultado:** La cita queda anulada y el profesional recibe una notificación.

---

## CU12 — Enviar notificaciones

**Actor:** Sistema (módulo interno)  
**Descripción:** El sistema envía correos automáticos de confirmación, recordatorio y cambios de cita.  
**Resultado:** Cliente y profesional reciben comunicaciones según corresponda.

