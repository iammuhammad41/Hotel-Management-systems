# Hotel Management System  
**Oracle Forms 10g & Oracle Database 10g**

A modular, centralized application to manage all aspects of hotel operations—guest check‑in/out, reservations, billing, housekeeping, inventory and reporting—built with Oracle Forms 10g/Reports on an Oracle 10g database.


## 📖 Project Overview

This Hotel Management System provides:

- **Secure Login & Role‑Based Access**  
- **Guest Registration & Profile Management**  
- **Room Reservation & Availability Calendar**  
- **Front‑Desk Check‑In / Check‑Out**  
- **Billing & Payments**  
- **Housekeeping Scheduling & Status**  
- **Inventory & Purchase Orders**  
- **Staff & User Administration**  
- **Reports & Analytics**  



## 📂 Repository Contents

- `login_test.fmb` / `login_test.fmx`  
  – Login & authentication form  

> _(Additional `.fmb` & `.fmx` modules can be added per feature, but all are confidential files.)_


## 🏗️ Main Modules & Forms

| Module                     | Forms Source (`.fmb`)      | Forms Executable (`.fmx`)     | Description                                      |
|:---------------------------|:---------------------------|:------------------------------|:-------------------------------------------------|
| **Login & Security**       | `login_test.fmb`           | `login_test.fmx`              | User authentication & role management            |
| **Guest Registration**     | `guest_reg.fmb`            | `guest_reg.fmx`               | Capture guest demographics & contact details     |
| **Room Reservations**      | `reservation.fmb`          | `reservation.fmx`             | Book, modify, cancel room reservations           |
| **Front‑Desk**             | `checkin_checkout.fmb`     | `checkin_checkout.fmx`        | Manage check‑in, check‑out and room assignments  |
| **Billing & Payments**     | `billing.fmb`              | `billing.fmx`                 | Generate invoices, accept payments, refunds      |
| **Housekeeping**           | `housekeeping.fmb`         | `housekeeping.fmx`            | Track room status, schedule cleaning tasks       |
| **Inventory Management**   | `inventory.fmb`            | `inventory.fmx`               | Stockroom items, reorder alerts, supplier orders |
| **Staff Administration**   | `staff_mgmt.fmb`           | `staff_mgmt.fmx`              | Employee profiles, roles, shift schedules        |
| **Reports & Analytics**    | `reports_menu.fmb`         | `reports_menu.fmx`            | Financial, occupancy, operational dashboards     |


## 🛠️ Prerequisites

1. **Oracle Database 10g**  
2. **Oracle Forms 10g Developer & Runtime**  
3. **Oracle Reports 10g** (for any `.rdf`/`.rep` modules)  
4. **PL/SQL** (for triggers & stored procedures)  
5. **Forms Server** configured with Forms Services  


## 🚀 Installation & Deployment

1. **Database Schema**  
   - Run `schema.sql` to create tables:  
     `USERS`, `GUESTS`, `ROOMS`, `RESERVATIONS`, `BILLS`, `INVENTORY`, `HOUSEKEEPING`, etc.  
   - Grant privileges to the application schema user.

2. **Compile Forms**  
   - Open each `.fmb` in Oracle Forms Developer → **Compile** → **Generate Form Module** → produce `.fmx`.  
   - Deploy all `.fmx` files to your Forms Server directory.

3. **Configure Forms Services**  
   - Add entries in `formsweb.cfg` for each form name.  
   - Ensure `FORMS_PATH` includes your deployment directory.

4. **Compile & Register Reports**  
   - Compile any `.rdf`/`.rep` modules and register them on the Reports Server.

5. **Launch Application**  
   - Access via browser/Java Applet, e.g.:  
     ```
     http://<forms-server>:<port>/forms/frmservlet?config=default&form=login_test.fmx
     ``` 
