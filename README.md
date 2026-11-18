# Group Project Accountability & Contribution Tracker

**Course:** MGIS130 — Information Systems & Technology (Fall 2026)  
**Track:** Web-App Track  
**Author:** [Your Name]  
**Live Demo:** [https://your-username.github.io/your-repo-name/](https://your-username.github.io/your-repo-name/)

---

## Overview

In university business and MIS team projects, divide-and-conquer workflows frequently break down—leading to unequal work distribution, missed interim deadlines, and last-minute scrambling before final submissions. 

The **Group Project Accountability Tracker** is a responsive web application designed to bring transparency and quantitative tracking to student group projects. Teams can log tasks with estimated effort hours, monitor real-time individual contribution ratios against a fair-share target, and generate formatted accountability reports for instructor review.

---

## Three-Layer System Architecture

This application is structured around a three-layer MIS architecture:

1. **Data Layer (Information Storage):**
   - Captures team rosters, project deliverables, assigned owners, estimated effort hours, due dates, and completion states via structured web forms.
   - Persists all application state locally in JSON format using browser `localStorage`, ensuring zero data loss across page refreshes without external backend dependencies.
   - Includes a pre-loaded sample dataset (*MGIS130 Capstone Team*) and a one-click reset function for live demonstration and testing.

2. **Processing Layer (Business Logic):**
   - **Contribution Ratio Engine:** Calculates each teammate's share of total completed effort hours relative to an equal target share ($\frac{100\%}{N\text{ members}}$) and dynamically flags members who are falling behind or carrying an uneven workload.
   - **Project Velocity & Deadline Logic:** Computes overall completion percentages by effort weight and compares task due dates against the current date to flag overdue deliverables.
   - **Peer-Evaluation Formatter:** Aggregates completed task logs and member contribution ratios into a plain-text status report ready for clipboard export.

3. **User Interface Layer (Presentation):**
   - Clean, responsive dashboard built with semantic HTML5, custom CSS3 variables/grid layouts, and vanilla JavaScript DOM manipulation.
   - Interactive task checklists that immediately recalculate overall progress bars and individual member status badges on toggle.
   - Dedicated modal view with one-click clipboard copy for submitting status updates to myCourses.

---

## Key Features

- **Real-Time Velocity Gauge:** Tracks overall project completion based on completed effort hours vs. total planned hours.
- **Fair-Share Accountability Meters:** Automatically adjusts target contribution percentages as team members are added or removed.
- **Overdue Deliverable Alerts:** Highlights uncompleted tasks past their due date in red.
- **One-Click Instructor Report Export:** Generates a structured summary of individual effort hours, task counts, and completion logs.
- **Demo Reset Control:** Restores default sample project data anytime during testing or live presentation.

---

## Project Structure

```text
├── index.html      # Semantic HTML structure and dashboard layout
├── style.css       # Custom styling, responsive grid, and status badges
├── script.js       # Data layer (localStorage), business logic, and DOM updates
└── README.md       # Project documentation and setup guide
(Note: If using the single-file deployment, all styling and logic are contained directly within index.html.)

Running Locally & Deployment
Run Locally
Clone this repository:

Bash
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your
