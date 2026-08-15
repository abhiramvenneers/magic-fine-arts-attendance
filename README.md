# Magic Fine Arts Technical Service LLC
## Employee Attendance & Salary Recording System

A mobile-friendly Progressive Web App (PWA) built specifically for **Magic Fine Arts Technical Service LLC** to record daily site attendance, track site productivity (SqM completed & material bags used), calculate employee salaries with overtime pay, and manage site & employee rosters.

---

## 🌟 Key Features

1. **Role-Based Access Control**:
   - **👑 Admin (Owner/HR)** (`admin@magicfineart.ae`): Access to all sites, employees, basic salary rates, overtime pay calculations, payment status marking (`Paid`/`Pending`), and report exports.
   - **👷 Site Supervisor** (`supervisor@magicfineart.ae`): Access to mark daily attendance for active sites/shifts and log daily site progress. Employee basic salary rates and monthly totals are hidden.

2. **Shift & Site Attendance Entry**:
   - Simultaneous **Day** and **Night** shift tracking per site with separate crews.
   - Auto-fill normal shift hours (e.g. Day `07:00 - 15:30`, Night `21:00 - 05:30`).
   - Auto-calculated overtime hours for time worked beyond normal shift hours.
   - Work type categorization: *Normal Plaster*, *Decorative Plaster*, *Art Work*, and *Custom Free-Text Work*.

3. **Site Daily Progress & Material Log**:
   - Logged **once per site per shift** (not per worker) to prevent triple-counting.
   - Tracks **Area Completed (SqM)** and **Material Bags Used**.
   - Auto-computes consumption efficiency metric (**Bags / SqM**).

4. **Automated Monthly Salary Sheet**:
   - Fixed monthly basic salary (AED).
   - Overtime rate fixed company-wide at **AED 6.5 / hour**.
   - Auto-summed monthly overtime pay = `OT Hours × 6.5 AED`.
   - Gross Pay = `Monthly Basic Salary + Overtime Pay`.
   - Payment status tracking (`Pending` / `Paid`) with settlement date picker.
   - Individual printable / PDF-ready **Salary Slip** generator with signature blocks.

5. **PWA & Offline Capability**:
   - Works on both iOS and Android via browser ("Add to Home Screen").
   - Works 100% offline out-of-the-box using local storage (`localStorage`).
   - Integrated with Google Firebase SDK (Firestore + Firebase Auth compat) for cross-device cloud synchronization.

---

## 🚀 Setup & Usage Guide

### 1. Running Locally
Open `index.html` in any modern web browser or serve it using any HTTP server:
```bash
# Serve local web app
npx serve e:\new_practice_projects\magic-fine-arts-attendance
```

### 2. Account Logins
Tap the **Account** button on the top right header to switch roles or log in:
- **Admin Mode**: Full control over salaries, rates, employee rosters, and export tools.
- **Supervisor Mode**: Streamlined interface for recording daily site attendance and progress.
