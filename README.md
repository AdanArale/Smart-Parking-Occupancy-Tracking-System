# Smart Parking Occupancy Tracking System

A web-based system that tracks how full the campus parking area is, in real time.

> Software Engineering, Fall 2026 | Istanbul Medipol University | Group 9

---

## Problem

Students and staff enter the campus parking area without knowing how full it is. Drivers waste time searching even when it is full, and security staff have no simple way to follow the vehicle count or catch wrong entry/exit records.

## Solution

The app receives an **entry event** when a vehicle enters and an **exit event** when it leaves. It updates the current count and calculates occupancy:

```
occupancy % = (current vehicles / total capacity) x 100
```

A single dashboard shows the result to everyone.

## Features

- Record vehicle entry and exit events from the campus gate system
- Update the vehicle count after every valid event
- Show occupancy percentage in real time
- Show total capacity, occupied spaces, and available spaces on one dashboard
- Status indicator with color: **Available**, **Nearly Full**, **Full**
- Timestamped history of all entry and exit events
- Authorized users can set capacity and correct the count

## Users

| User | What they do |
|------|--------------|
| Security officers / parking admins | Monitor movements, correct records, set capacity |
| Students, academic staff, employees | Check occupancy before entering |

## Tech Stack

| Area | Tools |
|------|-------|
| Platform | Responsive web app (runs in any browser) |
| Back end | Python, Flask, REST API |
| Front end | HTML, CSS, JavaScript, Bootstrap |
| Database | SQLite (capacity, current count, event history) |
| Testing | pytest |
| Tools | Git, Visual Studio Code |

## Getting Started

> Adjust file names to match your actual code.

```bash
# 1. Clone the repo
git clone <your-repo-url>
cd <repo-folder>

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
flask run
```

Then open `http://127.0.0.1:5000` in your browser.

## Running Tests

```bash
pytest
```

## Project Structure

> Suggested layout. Update it to match your repo.

```
.
├── app.py              # Flask app and routes
├── database.py         # SQLite setup and queries
├── templates/          # HTML pages (dashboard)
├── static/             # CSS, JS
├── tests/              # pytest tests
├── requirements.txt
└── README.md
```

## Team (Group 9)

| Name | Role |
|------|------|
| Kabeer Ahmed Shabeer | Team leader |
| Ahmet Yasir Eminoğlu | Project idea and proposal |
| Adan Arale | Presentation |
| Berkant Savaş | All-rounder, supports the whole team |

## Status

Project Part 1 in progress. See the proposal and report for details.
