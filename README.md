# 🚗 Snapp Application

A C++ simulation of a simplified ride dispatch system. This project models the core logic of a logistics platform where a central controller assigns and tracks ride missions, similar to systems like **Snapp** or **Uber**.

---

## 📦 Overview

This system supports:

- 👥 Driver registration and mission assignment  
- 🔁 Mission lifecycle tracking (start, progress, completion)  
- 🕒 Time-based scheduling and reward calculation  
- 🔒 Prevention of duplicate mission assignments  

---

## 🔁 Mission Lifecycle

Each mission includes:

- A unique **Mission ID**  
- A **Start Timestamp**  
- A **Reward Amount**  
- A **Completion Status**, based on time or distance logic  

---

## 👤 Driver Functionality

Drivers can:

- 📥 Add missions to their personal queue  
- 📃 View current and completed missions  
- ✅ Update status for missions that meet completion criteria  
- 🚫 Avoid duplicate mission assignments  

---

## 🧱 Class Architecture

### `Snap`
- Acts as the system controller  
- Parses user commands  
- Routes operations to the appropriate driver or mission handler  

### `Driver`
- Manages a time-sorted list of missions  
- Verifies mission completion based on rules  
- Displays structured mission information  

### `Mission`
- Stores metadata like ID, time, and reward  
- Determines completion using logical conditions  

---

## 💬 Supported Commands

Input via `cin`, example commands:
```bash
add_mission
show_missions
check_completed_mission
assign_driver
exit
```

Command formats are parsed in the `Snap` class.

---

## 🖨️ Sample Output

```
missions status for driver 1:
mission: 1001
start timestamp: 162000
end timestamp: 162600
reward: 500
status: completed
```

---

## 🎯 Project Highlights

- Emphasizes object-oriented design
- Sorted mission insertion for performance
- Clean, test-friendly output formatting
- Practical simulation of ride-sharing dispatch logic

---

> 🏫 Developed as an academic project in C++ exploring system design and real-world logic modeling.
