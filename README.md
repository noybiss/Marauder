# Marauder - Team Status Monitor

A Flask-based availability tracker and status monitor for teams. Designed and written by **OA (Omid Abduli)**.

---

## Overview

**Marauder** is a web-based availability management tool designed to track, coordinate, and visualize team member statuses across past, current, and future periods. Utilizing an intuitive, color-coded grid and responsive dark/light modes, it provides high visibility into team workload, potential overloads, and motivation.

---

## Features

- **🔴 Color-Coded Availability Indicator Grid**:
  - 🟢 **Green (Super)**: High motivation, available to help other teams.
  - 🟡 **Yellow (OK)**: Busy, but everything is under control.
  - 🟠 **Orange (Full)**: High pressure, no capacity for new tasks.
  - 🔴 **Red (Overloaded)**: Completely blocked, requires immediate intervention.
  - ⚪ **Gray (Unset)**: No status defined.
- **⚙️ Dynamic Admin Panel (`/admin`)**:
  - Secure configurations protected by verification.
  - **Switch Languages**: Localize the entire monitor dynamically into German, English, French, or Italian.
  - **Lock Past Weeks**: Option to prevent normal team members from editing historical week records.
  - **Limit Past Edits**: Allow changes only within a specified number of past week periods (e.g., last 2 periods).
  - **Configure Future Horizon**: Add future week periods to plan tasks in advance.
- **📊 Real-time Motivation & Overload Analytics**:
  - Dynamic workload summary bar charts.
  - Visual overload alert banner listing blocked team members.
- **💾 CSV Data Persistence**:
  - Saves all status updates automatically into a local `users.csv` database.
  - No database setup required.
- **✨ Premium Dark & Light Themes**:
  - Cohesive glassmorphic components, responsive grid layouts, and smooth animations.

---

## File Structure

```
Marauder/
├── server.py          # Flask backend & REST API endpoints
├── Interface.html     # Main status tracker UI (HTML/CSS/JS)
├── admin.html         # Admin configurations dashboard
├── users.csv          # Local user/status database
├── settings.json      # Saved admin configuration file (auto-generated)
├── requirements.txt   # Python dependency packages
└── .gitignore         # Version control exclusion file
```

---

## Quick Start

### Prerequisites

- Python 3.7+
- pip (Python package installer)

### Setup & Run

1. **Navigate to the directory**:
   ```bash
   cd "Marauder"
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the server**:
   ```bash
   python server.py
   ```

4. **Access the application**:
   - Status Monitor: `http://localhost:5005/`
   - Admin Panel: `http://localhost:5005/admin` (default authorization password: `admin`)

---

## Admin Controls & Settings

The Admin page allows managers to customize the monitor's behavior:
- **Language Selection**: Translates all tooltips, modals, labels, and error messages.
- **Past Week Modifications**: Enforces locks so users cannot retroactively alter past weeks, supporting data integrity.
- **Future Weeks count**: Dictates how many future period columns to display on the main grid (e.g., set to `1` or `2` to show upcoming week intervals).

---

## Author Credits

Designed, implemented, and maintained by **OA (Omid Abduli)**. Available for redistribution and open-source contribution under version control.
