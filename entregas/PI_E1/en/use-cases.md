# Main Use Cases

Below are the primary use cases of the appointment management platform for freelancers and small businesses.

---

## UC1 — Register as a professional

**Actor:** Professional  
**Description:** The professional creates an account by entering basic information.  
**Outcome:** The system registers the new professional and allows them to log in.

---

## UC2 — Log in

**Actor:** Professional  
**Description:** The professional enters their credentials to access their dashboard.  
**Outcome:** Access is granted if the credentials are valid.

---

## UC3 — Edit professional profile

**Actor:** Professional  
**Description:** The professional updates their public information (name, description, speciality, contact details).  
**Outcome:** Updated profile visible to clients.

---

## UC4 — Manage services

**Actor:** Professional  
**Description:** The professional creates, edits or disables the services they offer.  
**Outcome:** Services are updated and available for clients.

---

## UC5 — Configure availability

**Actor:** Professional  
**Description:** The professional defines their schedule (days, time slots, breaks, blocked days).  
**Outcome:** The system generates bookable time slots based on this availability.

---

## UC6 — View appointment calendar

**Actor:** Professional  
**Description:** The professional views upcoming appointments and appointment details.  
**Outcome:** Access to the full calendar with basic filtering (date, status, service).

---

## UC7 — Cancel or modify an appointment

**Actor:** Professional  
**Description:** The professional cancels an appointment or marks a slot as unavailable.  
**Outcome:** Appointment updated and notifications sent to the client.

---

## UC8 — View the professional profile (client)

**Actor:** Client  
**Description:** The client accesses the professional’s public page without authentication.  
**Outcome:** Information, services and general availability are displayed.

---

## UC9 — Book an appointment

**Actor:** Client  
**Description:** The client selects a service, chooses an available time slot and enters their details.  
**Outcome:** The appointment is registered and a confirmation email is sent.

---

## UC10 — Make a payment (test mode)

**Actor:** Client  
**Description:** After booking, the client completes the payment process via the configured gateway (test mode).  
**Outcome:** The gateway returns a status (success/error) and the system updates the appointment.

---

## UC11 — Cancel appointment (client)

**Actor:** Client  
**Description:** The client cancels their appointment within the allowed policy window.  
**Outcome:** Appointment is cancelled and the professional receives a notification.

---

## UC12 — Send notifications

**Actor:** System (internal module)  
**Description:** The system sends automatic emails (confirmation, reminders, changes).  
**Outcome:** Notifications delivered to client and/or professional.
