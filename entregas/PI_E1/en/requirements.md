# Functional and Non-Functional Requirements

This document describes the main functional and non-functional requirements of the appointment management platform for freelance professionals and small businesses.

---

## 1. Functional requirements

### FR1 – Professional management

- The system shall allow a professional to register and log in securely.
- The system shall allow the professional to recover or reset their password through a controlled mechanism (for example, a recovery email).

### FR2 – Professional profile

- The system shall allow the professional to edit their profile (name, description, speciality, basic contact details).
- The system shall display a public version of the professional’s profile, accessible to clients without authentication.

### FR3 – Service management

- The system shall allow the professional to define the services they offer (name, duration, price, online/presential).
- The system shall allow services to be enabled or disabled without permanently deleting them.

### FR4 – Availability management

- The system shall allow the professional to configure their availability (days and time slots).
- The system shall allow blocking specific days or time slots (holidays, breaks, unavailable periods).
- The system shall generate bookable time slots based on the availability and service duration.

### FR5 – Appointment booking by clients

- The system shall allow the client to select an available service from a professional.
- The system shall display free time slots based on the selected service.
- The system shall allow the client to enter their basic details (name, email) to complete the booking.
- The system shall register the appointment in the professional’s calendar.

### FR6 – Appointment modification and cancellation

- The system shall allow the professional to view a list of appointments and their details.
- The system shall allow the professional to cancel an appointment or mark a slot as unavailable.
- The system shall allow the client to cancel or request changes to an appointment according to the defined policy (for example, a minimum notice period).

### FR7 – Payment gateway integration (test mode)

- The system shall allow starting a payment process linked to a booking.
- The system shall receive the success/error result from the payment gateway in test mode.
- The system shall record the payment status associated with the appointment (pending, paid, error).

### FR8 – Notifications and reminders

- The system shall send a confirmation email to the client after a successful booking.
- The system shall send appointment reminder emails to the client with configurable notice.
- The system may notify the professional of new bookings, changes or cancellations.

### FR9 – Professional dashboard

- The system shall display a calendar of scheduled appointments for the professional.
- The system shall allow filtering appointments by date, status (pending, completed, cancelled) and service.
- The system may display a basic summary of activity (number of appointments in a period, most booked services, etc.) in future versions.

---

## 2. Non-functional requirements

### NFR1 – Usability

- The interface shall be simple and consistent, suitable for non-technical users.
- The platform shall be accessible from the main modern web browsers.
- The booking flow shall be designed to minimise user errors.

### NFR2 – Performance

- The main pages (professional profile and booking flow) shall load in a reasonable time over a standard home connection.
- Common operations (checking availability, creating a booking) shall complete within a few seconds, except when external services (payment, email) introduce delays.

### NFR3 – Security

- Access to the professional dashboard shall be protected by authentication.
- Passwords shall be stored as secure hashes in the database.
- Communication with the application shall use HTTPS in the deployment environment whenever possible.
- The application shall not store full card details; payments shall be handled by the external gateway.

### NFR4 – Reliability and data integrity

- The system shall prevent double bookings for the same slot and service.
- Create, update and cancel operations shall keep calendar, availability and payment status consistent.
- In case of payment gateway errors, the appointment shall be marked as unpaid or pending confirmation.

### NFR5 – Maintainability

- Backend code shall be organised into clear modules (scheduling, payments, notifications, etc.).
- Main API endpoints and the basic database structure shall be documented at a high level.
- Standard technologies shall be used (Python, Flask/FastAPI, SQLite) to ease future evolution.

### NFR6 – Basic scalability

- Although SQLite is used for the academic project, the design shall allow migration to another database engine if needed (e.g. PostgreSQL).
- The separation between frontend, API and database shall facilitate distributing the load

