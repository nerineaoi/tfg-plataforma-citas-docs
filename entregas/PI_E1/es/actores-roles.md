# Actores y roles del sistema

En la plataforma de gestión de citas intervienen los siguientes actores:

---

## 1. Profesional
Usuario que ofrece servicios (psicoterapia, asesoría u otro tipo de actividad profesional).

**Privilegios principales:**
- Iniciar sesión y autenticarse.
- Configurar sus servicios (precio, duración, modalidad).
- Gestionar su disponibilidad (horarios, descansos, días bloqueados).
- Editar su perfil profesional.
- Consultar su calendario.
- Gestionar citas (ver, confirmar, cancelar).
- Ver información básica de sus clientes.
- Recibir notificaciones relacionadas con nuevas reservas o cancelaciones.

---

## 2. Cliente
Usuario que reserva un servicio ofrecido por un profesional.

**Privilegios principales:**
- Visualizar la página pública del profesional.
- Seleccionar un servicio disponible.
- Reservar una cita.
- Realizar el pago (modo test durante el TFG).
- Recibir confirmación automática.
- Cambiar o cancelar citas según políticas.
- Recibir recordatorios automáticos por correo.

---

## 3. Sistema de pago (actor externo)
Servicio externo encargado de gestionar el pago seguro (PayPal o Stripe en modo test).

**Responsabilidades:**
- Procesar transacciones.
- Confirmar el pago al servidor backend.
- Generar estados de éxito o error.

---

## 4. Sistema de notificaciones (actor interno)
Módulo interno responsable de enviar comunicaciones automáticas al cliente o al profesional.

**Responsabilidades:**
- Enviar correos de confirmación.
- Enviar recordatorios previos a la cita.
- Notificar cambios o cancelaciones.
