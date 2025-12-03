# Wireframes / Screen Sketches

This document presents an initial overview of the navigation and main screens of the platform.
The wireframes are schematic and represent general structure, not final design.

---

## 1. Main screens

### 1.1. Public professional page

```text
+----------------------------------------+
|     Professional name                  |
|  Photo / Avatar (optional)             |
|  Short description                     |
|----------------------------------------|
|  Services offered                      |
|    - Service A (duration, price)       |
|    - Service B (...)                   |
|----------------------------------------|
|  Button: Book appointment              |
+----------------------------------------+
```
---

### 1.2. Service and date selection (client)

```text
+----------------------------------------+
|  Choose a service                      |
|   [Service A] [Service B]              |
|----------------------------------------|
|  Choose a date                         |
|   < Previous month   Next month >      |
|   Calendar with available days         |
+----------------------------------------+
```
---

### 1.3. Time slot selection and client details

```text
+----------------------------------------+
|  Available time slots                  |
|    [10:00] [11:00] [11:30] [...]       |
|----------------------------------------|
|  Client details                        |
|    Name:  [...........]                |
|    Email: [...........]                |
|----------------------------------------|
|  Button: Confirm booking               |
+----------------------------------------+
```
---

### 1.4. Payment screen (test mode)

```text
+----------------------------------------+
|  Appointment summary                   |
|  Service: X                            |
|  Date: DD/MM/YYYY - HH:MM              |
|----------------------------------------|
|  Button: Proceed to payment            |
+----------------------------------------+
```
---

### 1.5. Professional dashboard

```text
+----------------------------------------+
|  Sidebar menu                          |
|   - Calendar                           |
|   - Services                           |
|   - Availability                       |
|   - Profile                            |
|----------------------------------------|
|  Appointment calendar                  |
|   [Monthly / Weekly view]              |
|   List of appointments per day         |
+----------------------------------------+
```
---

## 2. Navigation flow (summary)

Client:

1. Opens public professional page.  
2. Selects service → date → available time slot.  
3. Enters personal details → confirms booking.  
4. Completes payment (test mode).  
5. Receives confirmation email.

Professional:

1. Logs in.  
2. Views their calendar.  
3. Manages services and availability.  
4. Updates public profile.
