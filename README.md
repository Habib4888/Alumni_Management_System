
# IIUC Alumni Portal

A web-based Alumni Management System for **International Islamic University Chittagong (IIUC)**. It connects alumni, current students and the university administration through a single role-based portal.

https://habib4888.github.io/Alumni_Management_System/

Built as a course project for *System Analysis, Design and Development*.

---

## Features

### For everyone
- Role-based login (Admin, Alumni, Student) with a registration and approval flow
- Dashboard tailored to each role
- Global search (press `/` to focus)
- Notifications panel
- Light and dark mode (dark is the default)
- Responsive layout that works on mobile

### Alumni
- **Alumni directory:** search and filter by department and batch, card or table view
- **Profile:** edit details, control visibility (public or private)
- **Events:** RSVP with capacity limits
- **Job board:** post jobs, apply with a note, close or reopen listings
- **Donations:** give to campaigns and receive a receipt
- **Discussion:** post, like, comment and report posts

### Admin
- Approve or reject new registrations
- Manage users (activate or deactivate accounts, export CSV)
- Publish, edit and delete events
- Moderate the discussion forum (dismiss reports, remove posts)
- Reports and analytics with charts
- Activity logs
- Reset demo data

### Student
- Browse the alumni directory
- View and RSVP to events
- Browse and apply for jobs
- Take part in discussions

---

## Demo accounts

Click one of the demo buttons on the login screen, or sign in manually.

| Role   | Email                             | Password   |
|--------|-----------------------------------|------------|
| Admin  | salma.chowdhury@iiuc.ac.bd        | `password` |
| Alumni | habibul.bari@iiuc-alumni.net      | `password` |
| Student| mizanur.c@iiuc-alumni.net         | `password` |

A pending registration is available to test the approval flow. Sign in as Admin and open **Approvals**.

---

## How to run

No installation or server is needed.

1. Download `index.html` (or `Alumni_Management_System_UI.html`).
2. Double-click it, or open it in any modern browser (Chrome, Edge, Firefox).
3. Sign in with a demo account.

> An internet connection is needed only to load the Google Fonts. Without it, the app still works with fallback fonts.

To restore the original demo data, sign in as Admin, open the user menu, and choose **Reset demo data**.

---

## Tech stack

- **HTML5**, **CSS3** (custom properties for theming, no framework)
- **Vanilla JavaScript** (no framework or build step)
- **localStorage** for data persistence in the browser
- **Google Fonts:** Fraunces and IBM Plex Sans

The whole application is a single self-contained file.

---

## Project structure

```
.
├── index.html        # The complete application (HTML, CSS and JavaScript)
└── README.md
```

---

## Data model

All data lives in `localStorage` under the key `iiuc_ams_v2`.

| Collection  | Purpose                                              |
|-------------|------------------------------------------------------|
| `users`     | Accounts, roles, status, and alumni profile fields   |
| `events`    | Events with RSVP lists and optional capacity         |
| `jobs`      | Job listings and applicants                          |
| `causes`    | Donation campaigns with goal and raised amount       |
| `donations` | Donation records with receipt numbers                |
| `posts`     | Discussion posts with likes, comments and flags      |
| `logs`      | Activity log entries                                 |
| `notes`     | Notifications                                        |

---

## Limitations

This is a **front-end prototype** built to demonstrate the user interface and workflows.

- Data is stored per browser. It is not shared between users or devices.
- Passwords are stored as plain text in the browser. A production system needs a backend, a database, and password hashing (bcrypt or Argon2).
- There is no real email sending. Password reset and notifications are simulated.
- Access control is enforced in the interface only. A production system must enforce it on the server.

### Planned next steps
- Backend API (Node.js or PHP) with a MySQL or PostgreSQL database
- Hashed passwords and token-based sessions
- Real email notifications and password reset
- Payment gateway integration for donations (bKash, Nagad, cards)

---

## Team

- E243014(Fahimul Islam Nahid)
- E243015(Md. Abdullah Nahin)
- E243042(Md.Habibul Bari)

**Course:** System Analysis, Design and Development
**Submitted to:** Abu Raihan Anchari Miskat, Adjunct Faculty, Department of Computer Communication Engineering, IIUC

---

## License

Academic project. All rights reserved by the authors unless otherwise stated.
>>>>>>> 7a31a56 (Updated README)
