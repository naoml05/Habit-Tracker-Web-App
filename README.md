# 📅 Habit Tracker
 
> *Small actions, tracked daily, add up to lasting change.*
 
**Habit Tracker** is a full-stack web app for building habits and keeping streaks. Create the habits you care about, log them each day, and see your consistency at a glance on a calendar heatmap.
 
**Status:** 🔴 In Progress (core API underway, heatmap in development)
 
---
 
## 🧰 Tech Stack
 
| Layer    | Tech                 |
| -------- | -------------------- |
| Frontend | JavaScript, React    |
| Backend  | Node.js, Express     |
| Database | SQLite               |
 
---
 
## ✨ What It Does
 
Habits are hard to maintain when you can't see your progress. Habit Tracker keeps every habit and every check-in in one place, then turns that history into a visual record of your streaks.
 
### 📝 Habits
 
An Express REST API provides full **CRUD for habits**: create, view, update, and delete the routines you want to track.
 
### ✅ Daily Logs
 
Each time you complete a habit, a **log entry** is stored in SQLite and linked to that habit. Logs are the data behind every streak.
 
### 🔥 Streak Heatmap
 
A **React calendar heatmap** turns your logs into a visual history. Darker squares mean more activity, and unbroken runs of days show up as streaks.
 
---
 
## 🗺️ Architecture
 
```
        React Frontend
   (habit UI + calendar heatmap)
              │
              ▼
   ┌───────────────────┐
   │  Express REST API │  → habit CRUD + log CRUD
   └───────────────────┘
              │
              ▼
   ┌───────────────────┐
   │      SQLite       │  → habits table + logs table
   └───────────────────┘
              │
              ▼
   🔥 Streaks rendered on the heatmap
```
 
---
 
## 🛣️ Roadmap
 
- [x] Express REST API for habit CRUD
- [x] SQLite persistence for habits and logs
- [ ] Log CRUD endpoints
- [ ] React calendar heatmap for streaks
- [ ] Current and longest streak calculations
- [ ] Habit editing and archiving in the UI
- [ ] Tests and deployment
---
 
*Show up today, and let the heatmap do the rest.*
