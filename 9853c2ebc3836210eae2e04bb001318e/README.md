# 🏢 ServiceNow - Event Space Booking System

### 🚀 Overview
The **Event Space Booking System** is a custom ServiceNow application designed to streamline how employees reserve internal rooms for meetings, workshops, and events.  
It provides an intuitive interface, secure access controls, automated booking validations, and maintenance management for internal event spaces.

---

## 📚 Project Details

**Event Name:** ServiceNow Fundamentals Hackathon-1  
**Location:** Center of Excellence, Hyderabad, India  
**Application Scope:** `Event Space Booking`

---

## 🎯 Objective
To design and implement a **custom room booking system** in ServiceNow that allows employees to:
- Book event rooms easily
- Check availability dynamically
- Enforce access restrictions
- Automate booking and maintenance processes

---

## ⚙️ Features

### 1. **Table & Module Setup**
- **Custom Tables:**
  - `Event Room` – Stores all bookable rooms  
  - `Event Booking` – Tracks bookings made by users  
  - `Room Maintenance` – Manages maintenance schedules  

- **User Roles:**
  - `event_user` → Create/view own bookings  
  - `event_admin` → Full control over rooms and bookings  
  - `facilitator` → Manage maintenance schedules  

- **Modules Created:**
  - Book a Room (New Record)
  - My Bookings (User-specific list)
  - Manage Rooms
  - Maintenance Schedule
  - All Bookings

---

### 2. **Forms & Lists**
- Custom views for each role (Employee, Admin, Maintenance)
- Employees see only their own bookings  
- Admins see all data  
- Maintenance team has restricted access

---

### 3. **Client Script & UI Policies**
- **Client Script:**  
  Displays a message showing how many days ago the user last booked a room (via Script Include using GlideAjax).

- **UI Policies:**  
  - Room field shown only after selecting dates  
  - Notes mandatory when cancelling  
  - Check-in Time read-only  
  - Start/End dates must be future and valid

---

### 4. **Business Rules**
- Auto-update status to **Confirmed** on successful booking  
- Sync room status with maintenance window  
- Auto-cancel bookings during maintenance  

---

### 5. **Access Control Rules (ACLs)**
| Role | Permissions |
|------|--------------|
| `event_user` | Create/view/cancel own bookings |
| `event_admin` | Manage all bookings & rooms |
| `facilitator` | Manage maintenance only |

---

### 6. **UI Actions**
- **Check-In Button:** Updates Check-in Time & sets Status = Completed  
- **Cancel Booking:** Prompts cancellation reason and updates status  

---

### 🧩 Challenges Implemented
- **Booking Restriction:** Prevent double booking for same date  
- **Room Availability:** Show only available and non-maintenance rooms  

---

## 🧠 Evaluation Criteria
✅ Table Relationships & Structure  
✅ Dynamic UI Design & Logic  
✅ Client Script + Script Include usage  
✅ UI Policy Accuracy  
✅ Business Rule Automation  
✅ Role-Based ACL Security  
✅ Working UI Actions  

---

## 💡 Technologies Used
- **Platform:** ServiceNow (Scoped Application)
- **Scripting:** GlideScript (Server-side) & GlideAjax (Client-side)
- **Configuration:** Tables, Forms, ACLs, UI Policies, Business Rules, UI Actions

---

## 🏁 Getting Started
To deploy this app in ServiceNow:
1. Create a new **Scoped Application** named `Event Space Booking`
2. Create the tables and fields listed above
3. Configure roles and ACLs
4. Add Client Scripts, UI Policies, and Business Rules
5. Test booking, maintenance, and access control workflows

---

## 📷 Demo
<img width="2877" height="1168" alt="image" src="https://github.com/user-attachments/assets/077219c0-dc93-4115-9995-8e709e006ed8" />

---


---

