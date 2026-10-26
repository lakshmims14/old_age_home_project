# Old Age Home Management System (MERN Stack)

A full stack web application for managing an old age home. It lets staff keep resident records, medical details, meal plans, appointments, birthdays and activities in one place, with login-protected pages.

Built with MongoDB, Express, React and Node.js (the MERN stack).

## Features

- **Login and registration** with JWT authentication and hashed passwords
- **Protected pages:** the dashboard is only available after logging in
- **Admin panel** for managing the system
- **Resident records:** add and view residents with name, date of birth, gender, admission date, room, emergency contact, medical history, dietary needs, allergies, photo and documents
- **Medical details:** each resident can have multiple diseases, and each disease can have multiple medicines with dosage and frequency
- **Meal plans** for residents
- **Appointments** tracking
- **Birthdays** list
- **Activities:** an activity gallery, activity details and participation tracking (such as art, games, music, walking and yoga)
- **Feedback:** a feedback page and a staff feedback list
- **Responsive navigation bar and sidebar** built with Material UI

## Tech Stack

- **Frontend:** React, Vite, React Router, Material UI
- **Backend:** Node.js, Express
- **Database:** MongoDB with Mongoose
- **Authentication and security:** JSON Web Tokens (JWT), bcrypt password hashing, CORS
- **File uploads:** Multer (resident photos and documents)
- **Configuration:** dotenv

## Project Structure

```
backend_old/                    # Node.js + Express API
  index.js                      # server entry point
  db.js                         # MongoDB connection
  model/                        # Mongoose models (for example Resident)
  utils/                        # helper functions
  package.json
old_age_home_app_frontend/      # React app (Vite)
  public/                       # images
  src/                          # components, routes and styles
  package.json
```

## Resident Data Model

Each resident is stored with:

| Field | Description |
| --- | --- |
| name, dob, gender | basic details (gender: male, female or other) |
| admissionDate, room | when the resident joined and where they stay |
| emergencyContact | contact person's details |
| history, allergies, dietary | medical history and care needs |
| diseases | list of diseases, each with a list of medicines (name, dosage, frequency) |
| photo, document | uploaded file names |
| createdAt, updatedAt | timestamps updated automatically |

## Getting Started

You need Node.js and a MongoDB database (local or MongoDB Atlas).

1. Clone the repository
   ```
   git clone https://github.com/lakshmims14/old_age_home_project.git
   cd old_age_home_project
   ```
2. Set up the backend
   ```
   cd backend_old
   npm install
   ```
   Create a `.env` file in `backend_old` with your own values:
   ```
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   PORT=5000
   ```
   Check the variable names in `db.js` and `index.js` and use the same ones. Then start the server:
   ```
   node index.js
   ```
3. Set up the frontend (in a second terminal)
   ```
   cd old_age_home_app_frontend
   npm install
   npm run dev
   ```
4. Open the address shown in the terminal (usually `http://localhost:5173`), register a user and log in.

## What I Learned

- Building a full stack app with the MERN stack
- Designing MongoDB schemas with nested data using Mongoose
- Securing routes with JWT authentication and password hashing
- Handling file uploads with Multer
- Building a multi-page React app with protected routes using React Router and Material UI

## Author

**Lakshmi MS** - Python Full Stack Developer (fresher)
[LinkedIn](https://www.linkedin.com/in/lakshmi-m-s-aa97a2293/) | [GitHub](https://github.com/lakshmims14)
