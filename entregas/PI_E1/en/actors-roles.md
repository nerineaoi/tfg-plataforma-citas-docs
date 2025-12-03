# System Actors and Roles

The appointment management platform involves the following actors:

---

## 1. Professional
The user who offers services (therapy, consulting, coaching, or any professional activity).

**Main privileges:**
- Log in and authenticate.
- Configure offered services (price, duration, modality).
- Manage availability (time slots, breaks, blocked days).
- Edit professional profile.
- View their calendar.
- Manage appointments (view, confirm, cancel).
- View basic client information.
- Receive notifications for new bookings or cancellations.

---

## 2. Client
The user who books a service from a professional.

**Main privileges:**
- View the professional’s public page.
- Select an available service.
- Book an appointment.
- Make the payment (test mode during the project).
- Receive automatic confirmation.
- Modify or cancel appointments (depending on policies).
- Receive automatic reminders by email.

---

## 3. Payment System (external actor)
External service responsible for processing payments (PayPal or Stripe in test mode).

**Responsibilities:**
- Process transactions.
- Send payment confirmation to the backend.
- Return success or error status.

---

## 4. Notification System (internal actor)
Internal module responsible for sending automatic communications.

**Responsibilities:**
- Send confirmation emails.
- Send reminder emails.
- Notify changes or cancellations.

