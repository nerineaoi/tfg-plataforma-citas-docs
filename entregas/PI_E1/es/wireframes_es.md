# Wireframes / Boceto de pantallas

Este documento recoge un primer boceto de la navegación y las pantallas principales de la plataforma.  
Los wireframes son esquemáticos y representan la estructura general sin diseño final.

---

## 1. Pantallas principales

### 1.1. Página pública del profesional

```text
+----------------------------------------+
|  Nombre del profesional                |
|  Foto / Avatar (opcional)              |
|  Descripción corta                     |
|----------------------------------------|
|  Servicios ofrecidos                   |
|    - Servicio A (duración, precio)     |
|    - Servicio B (...)                  |
|----------------------------------------|
|  Botón: Reservar cita                  |
+----------------------------------------+
```
---

### 1.2. Selección de servicio y fecha (cliente)

```text
+----------------------------------------+
|  Seleccionar servicio                  |
|   [Servicio A] [Servicio B]            |
|----------------------------------------|
|  Seleccionar fecha                     |
|   < Mes anterior   Mes siguiente >     |
|   Calendario con días disponibles      |
+----------------------------------------+
```

---

### 1.3. Selección de hora y datos del cliente

```text
+----------------------------------------+
|  Horas disponibles                     |
|    [10:00] [11:00] [11:30] [...]       |
|----------------------------------------|
|  Datos del cliente                     |
|    Nombre: [...........]               |
|    Email:  [...........]               |
|----------------------------------------|
|  Botón: Confirmar reserva              |
+----------------------------------------+
```
---

### 1.4. Pantalla de pago (modo test)

```text
+----------------------------------------+
|  Resumen de la cita                    |
|  Servicio: X                           |
|  Fecha: DD/MM/AAAA - HH:MM             |
|----------------------------------------|
|  Botón: Proceder al pago               |
+----------------------------------------+
```
---

### 1.5. Panel del profesional

```text
+----------------------------------------+
|  Menú lateral                          |
|   - Agenda                             |
|   - Servicios                          |
|   - Disponibilidad                     |
|   - Perfil                             |
|----------------------------------------|
|  Calendario de citas                   |
|   [Vista mensual / semanal]            |
|   Citas listadas por día               |
+----------------------------------------+
```
---

## 2. Flujo de navegación (resumen)

1. Cliente accede al perfil público del profesional.  
2. Selecciona servicio → fecha → hora disponible.  
3. Introduce sus datos → confirma reserva.  
4. Realiza pago (modo test).  
5. Recibe correo de confirmación.

El profesional:

1. Inicia sesión.  
2. Consulta su calendario.  
3. Gestiona servicios y disponibilidad.  
4. Actualiza su perfil público.
