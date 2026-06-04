# College Scout — React + Node.js

A clean React + Node.js project with a smooth intro transition inspired by editorial portfolio websites.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Folder Structure](#folder-structure)
3. [How to Run](#how-to-run)
4. [Available Scripts](#available-scripts)
5. [Frontend Files](#frontend-files)
6. [Backend Files](#backend-files)
7. [API Endpoints](#api-endpoints)
8. [Animation Flow](#animation-flow)
9. [Where to Edit Text](#where-to-edit-text)

## Project Overview

This project uses:

- React + Vite for the frontend
- Framer Motion for the intro animation
- Node.js + Express for the backend API
- CSS split into a proper stylesheet
- Component-based file structure

## Folder Structure

```text
college-scout-react-node
├── client
│   ├── index.html
│   ├── package.json
│   └── src
│       ├── App.jsx
│       ├── main.jsx
│       ├── styles.css
│       ├── components
│       │   ├── CollegeList.jsx
│       │   ├── Hero.jsx
│       │   ├── Intro.jsx
│       │   ├── MotionHelpers.jsx
│       │   ├── Navbar.jsx
│       │   └── WorkInProgress.jsx
│       └── data
│           └── animation.js
├── server
│   ├── .env.example
│   ├── index.js
│   ├── package.json
│   └── routes
│       ├── collegeRoutes.js
│       └── contactRoutes.js
├── package.json
└── README.md
```

## How to Run

Open the project folder in VS Code, then run:

```bash
npm run install-all
npm run dev
```

Frontend:

```text
http://localhost:5173
```

Backend:

```text
http://localhost:5000
```

## Available Scripts

From the main project folder:

```bash
npm run install-all
```

Installs root, frontend, and backend dependencies.

```bash
npm run dev
```

Runs React and Node.js together.

```bash
npm run build
```

Builds the React frontend.

## Frontend Files

- `client/src/App.jsx` controls intro timing and page layout.
- `client/src/components/Intro.jsx` contains the moving intro title animation.
- `client/src/components/Hero.jsx` contains the main landing section.
- `client/src/components/Navbar.jsx` contains the top navigation.
- `client/src/components/CollegeList.jsx` fetches colleges from the backend.
- `client/src/styles.css` contains all styling.

## Backend Files

- `server/index.js` starts Express.
- `server/routes/collegeRoutes.js` returns sample college data.
- `server/routes/contactRoutes.js` handles contact form requests.

## API Endpoints

```text
GET /api/health
GET /api/colleges
POST /api/contact
```

Example POST body for contact:

```json
{
  "name": "Aadarshan",
  "email": "test@example.com",
  "message": "I want to know more about colleges."
}
```

## Animation Flow

1. `Welcome to` appears first.
2. `College Scout.` pops in below it.
3. Both texts move together to the final hero position.
4. The title settles on the left in the same font as the main header.
5. Navbar, green label, paragraph, buttons, and college cards appear around it slowly.
6. Work-in-progress page returns using a smooth downward pull animation instead of a fade.

## Where to Edit Text

Edit the main hero text in:

```text
client/src/components/Hero.jsx
```

Edit college data in:

```text
server/routes/collegeRoutes.js
```

## Latest Fixes

- Fixed the intro so `Welcome to` and `College Scout.` are both visible before the title moves.
- Matched the intro font with the main hero heading.
- Changed the title movement so it settles on the left first, then surrounding content appears.
- Added a `WorkInProgress.jsx` overlay with a smooth downward return animation.
