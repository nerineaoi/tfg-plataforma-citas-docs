# PI_E0 – Initial Project Description 

## Integrated Project: Initial Description
**Appointment and Service Management Platform for Freelancers and Small Businesses**  
Ana Vertedor  
Web Application Development (DAW)  
December 1, 2025

---

## 1. Project Description
This project consists of a web application designed to help professionals manage appointments and services efficiently. It is aimed at freelancers who work with clients through scheduled sessions—such as psychotherapists, coaches, consultants, designers, or freelance developers.

The platform allows each professional to define their services, configure weekly availability, receive confirmed bookings, process payments, and send automatic reminders.

Unlike generic tools such as Booksy, Calendly, or Doodle, this platform goes beyond displaying availability and accepting bookings. It is specifically designed around the real needs of solo professionals, especially in fields without administrative assistance, where time management is critical.

The system includes advanced, configurable business rules (limits for changes, break times, slot blocking, recurring client slots, avoidance of fragmented days, etc.). It features intelligent slot generation to maintain a well-structured work rhythm. The platform supports customization with logo, legal texts, and basic tax data to automatically generate invoices.

The initial use case will focus on a real psychotherapist, while maintaining a generic, flexible architecture adaptable to multiple professional profiles through configuration rather than code changes.

### Target Professional Profiles
- **Psychotherapy**: online/in-person sessions, advance payment, controlled rescheduling.
- **Freelance/Consulting**: evaluation sessions, reviews, technical assistance, time blocking.

Shared workflow:
1. Professional configures their profile.
2. Client selects service and available slot.
3. Payment is processed.
4. Booking is confirmed.
5. Reminders are sent.
6. Professional manages the schedule.

---

## 2. Main Features

### a) Professional Management
- Registration/login  
- Profile settings (brand, contact, logo, legal texts, tax data)  
- Multi-professional support  

### b) Service & Schedule Configuration
- Definition of services (name, duration, modality, price)  
- Working hours (days, breaks, limits)  
- Day blocking  

### c) Calendar & Client Booking
- Public profile with available slots  
- Intelligent slot generation  
- Payment required for confirmation  

### d) Payments & Reservations
- Integration with PayPal/Stripe  
- Booking states: Pending, Paid/Confirmed, Cancelled  
- Cancellation rules  

### e) Notifications
- Automatic email reminders  
- Notification templates  

### f) Professional Dashboard
- Calendar (day/week/month)  
- Client list  
- Manual booking  
- Internal notes  

### g) Client Dashboard
- View upcoming appointments  
- Access session info  
- Optional history  

### h) Security & Privacy
- Data isolation  
- Secure credentials  
- HTTPS  
- Basic GDPR compliance  

---

## 3. Technologies

### Frontend
- HTML, CSS, JavaScript  
- Optional React  
- Responsive design  

### Backend
- Node.js (Express) or Python (FastAPI)  
- Business logic (scheduling, payments, notifications)  

### Database
- PostgreSQL or SQLite  

### Authentication & Security
- JWT or session-based  
- Encrypted passwords  
- Environment variables  

### Payments
- PayPal Checkout  
- Stripe (test)  

### Notifications
- Email via SMTP/external provider  

### Deployment
- Docker + Railway/Render  

### Design
- Figma wireframes  

---

## 4. Motivation & Usefulness
Freelancers often rely on scattered tools: calendars, spreadsheets, manual reminders, and messaging apps. Existing tools are not optimized for solo professionals and are often expensive or lack proper payment integration.

This platform centralizes:  
- appointment management  
- payments  
- reminders  
- client info  

It is practical and aligns with real DAW employment scenarios.

---

## 5. Conclusion
The project aims to create a functional, scalable platform for professionals who manage appointments. Using a real psychotherapist as a base case, it remains adaptable to many fields. The MVP focuses on core flows (services → availability → booking → payment → reminders), leaving advanced modules for later development.
