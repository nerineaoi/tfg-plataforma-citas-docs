# Tecnologías previstas

En esta sección se describen las tecnologías previstas para el desarrollo de la plataforma de gestión de citas.

---

## 1. Frontend (cliente)

- **HTML5**  
  Para la estructura de las páginas y los formularios de reserva.

- **CSS3**  
  Para el diseño visual, maquetación y estilos responsivos básicos.

- **JavaScript (vanilla)**  
  Para añadir interactividad en el lado del cliente (validaciones básicas, actualización dinámica de algunos elementos, etc.).

> En fases posteriores podría valorarse el uso de algún framework o biblioteca adicional (por ejemplo, React), pero no es imprescindible para el alcance del TFG.

---

## 2. Backend (servidor / API REST)

- **Python 3**  
  Lenguaje principal del backend, elegido por su sencillez, madurez y amplio ecosistema.

- **Flask** o **FastAPI** (uno de los dos)  
  Framework ligero para crear la API REST que gestionará:
  - Autenticación de profesionales.
  - Gestión de servicios y disponibilidad.
  - Creación y consulta de citas.
  - Integración con la pasarela de pago.
  - Envío de notificaciones (a través de un módulo interno).

La elección final entre Flask o FastAPI se concretará al inicio de la fase de desarrollo, pero la arquitectura está pensada para que cualquiera de los dos encaje.

---

## 3. Base de datos

- **SQLite**  
  - Base de datos relacional sencilla e integrada
