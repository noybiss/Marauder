# Marauder - Team Status Monitor

A high-performance Flask-based resource planning and workload visualization platform. Architected and written by **OA (Omid Abduli)**.

---

## Executive Summary

**Marauder** is an availability management platform designed to track, visualize, and balance team workloads across historical, current, and future periods. Featuring a premium glassmorphic interface, real-time motivational analytics, and automated period management, it empowers organizations to optimize team capacity, proactively identify burnout risks, and streamline project assignments.

---

## Core Capabilities & Features

### 📊 Real-Time Workload & Capacity Grid
* **Visual Capacity Tracking**: Displays current workloads via structured, interactive status indicators:
  * 🟢 **Optimal Capacity (Green)**: High motivation, fully available for new project assignments.
  * 🟡 **Stable Load (Yellow)**: Busy, operating at normal capacity.
  * 🟠 **Intake Limit (Orange)**: Maximum capacity reached; warning threshold where no new tasks should be assigned.
  * 🔴 **Critical Overload (Red)**: Critical bottleneck; requires immediate management intervention to redistribute tasks.
* **Timeline Horizon Engine**: Automatically handles period creation and oldest record pruning to maintain a structured 16-week database.
* **Overload & Risk Analytics**: Displays real-time motivation ratios and system overload banners listing blocked resources for rapid decision-making.

### ⚙️ Secure Administrative Dashboard (`/admin`)
* **Role-Based Configuration**: Settings panel secured with password-protected API endpoints and in-memory credential storage.
* **Data Integrity & Edit Locks**: Restricts historical modifications. Administrators can completely lock past weeks or define a specific modification limit (e.g., allow edits only within the last 4 weeks).
* **Multi-lingual Localization**: Supports instant on-the-fly interface translation with complete dictionaries for:
  * 🇩🇪 **German (Deutsch)**
  * 🇬🇧/🇺🇸 **English**
  * 🇫🇷 **French (Français)**
  * 🇮🇹 **Italian (Italiano)**

### 📚 Integrated Help & FAQ Assistant
* **Self-Service Support Drawer**: A dedicated Help modal accessible directly from the dashboard header.
* **Instant Keyword Filter**: Search and filter operational instructions, capacity guidelines, and system support contacts in real-time.
* **CSV Dynamic Loading**: Dynamically loads FAQ definitions from a centralized file (`ampel_faq.csv`) for zero-code documentation maintenance.

### 💾 Performance-Optimized Infrastructure
* **Zero-Configuration Storage**: Relies on a robust, lightweight CSV-based datastore (`users.csv`) for zero-maintenance local deployment.
* **Cross-Origin Capability**: Backend built on Flask with CORS support to easily allow integration within local corporate networks.

---

## System Architecture & File Layout

```text
Marauder/
├── server.py          # REST API endpoints & automated database pruning
├── Interface.html     # Client-side visualization monitor (HTML5/CSS3/ES6)
├── admin.html         # Secure administrative control board
├── users.csv          # Local user/status database (comma-separated values)
├── ampel_faq.csv      # Central FAQ database
├── settings.json      # Dynamic application settings configuration (ignored in git)
├── requirements.txt   # Python ecosystem dependencies
└── .gitignore         # Version control exclusion file
```

---

## Deployment & Setup

### Prerequisites
* Python 3.7 or higher
* pip (Python Package Installer)

### Installation Steps

1. **Clone the directory**:
   ```bash
   cd Marauder
   ```

2. **Install requirements**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the platform server**:
   ```bash
   python server.py
   ```

4. **Access points**:
   * **Main Status Monitor**: `http://localhost:5005/`
   * **Administrative Control Board**: `http://localhost:5005/admin` *(Default access password: `admin`)*

---

## Project Credits

Architected, designed, and developed by **OA (Omid Abduli)**. Available for local deployment, scalability extensions, and team coordination optimization.
