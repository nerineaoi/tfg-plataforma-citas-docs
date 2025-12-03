# Planned Technologies

This section describes the main technologies planned for the development of the appointment management platform.

---

## 1. Frontend (client)

- **HTML5**  
  Used for the structure of the pages and booking forms.

- **CSS3**  
  Used for visual design, layout and basic responsive behaviour.

- **Vanilla JavaScript**  
  Used to add client-side interactivity (basic validation, small dynamic updates, etc.).

> In later stages a frontend library or framework (e.g. React) could be considered, but it is not required for the scope of this project.

---

## 2. Backend (server / REST API)

- **Python 3**  
  Main backend language, chosen for its simplicity, maturity and ecosystem.

- **Flask** or **FastAPI** (one of them)  
  Lightweight framework to build the REST API, responsible for:
  - Professional authentication.
  - Service and availability management.
  - Creating and querying appointments.
  - Payment gateway integration.
  - Triggering notification emails (via an internal module).

The final choice between Flask and FastAPI will be made at the beginning of the implementation phase, but the architecture is designed to work with either.

---

## 3. Database

- **SQLite**  
  - Simple relational database engine integrated with Python.  
  - Sufficient for the expected scale in an academic context.  
  - Makes deployment and testing easier without requiring an external database server.

The design will allow migration to another engine in the future (e.g. PostgreSQL) if the project grows.

---

## 4. External integrations

- **Payment gateway** (Stripe or PayPal in test mode)  
  To simulate real payments without processing live transactions.

- **Email service**  
  Using an SMTP solution (for example, the hosting provider’s mail server or an external service) to send:
  - Booking confirmation emails.
  - Appointment reminders.
  - Change or cancellation notifications.

---

## 5. Tooling and version control

- **Git** + **GitHub**  
  - Version control for the project.  
  - Private repository for the source code.  
  - Public repository for TFG documentation.

- **Development environment**  
  - Editor/IDE: VS Code or similar.  
  - Python virtual environment to isolate project dependencies.
