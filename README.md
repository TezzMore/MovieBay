# MovieBay 🎬

A Netflix-style streaming platform built with MERN stack. Users can browse movies/series, watch trailers, and manage their accounts. Admins get a separate dashboard to manage content.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)

## What's inside

- JWT authentication (login/register with encrypted passwords)
- Role-based access (user vs admin)
- Movie/series categorization with carousels
- Random featured content on homepage
- Watch page for trailers
- Admin panel for CRUD operations on movies & lists

## Project structure

├── api/ # Backend
│ ├── models/ # MongoDB schemas
│ ├── routes/ # Express routes
│ └── index.js # Server entry
│
├── client/ # React frontend
│ ├── src/
│ │ ├── components/ # Navbar, Featured, List, etc.
│ │ ├── pages/ # Home, Watch, Login, Register
│ │ └── context/ # Auth context + reducers
│ └── public/
│
└── admin/ # Admin dashboard (separate React app)


## Getting started

### Prerequisites
- Node.js 
- MongoDB (local or Atlas)
- npm or yarn

### Backend setup

```bash
cd api
npm install

Create .env in api/:
MONGO_URL=your_mongodb_connection_string
SECRET_KEY=your_jwt_secret

npm start

Server runs on http://localhost:8800

Client setup:
cd client
npm install
npm start

Opens on http://localhost:3000


Admin setup

cd admin
npm install
npm start

Opens on http://localhost:3001

API endpoints
| Method | Route              | Description      | Auth  |
| ------ | ------------------ | ---------------- | ----- |
| POST   | /api/auth/register | Create account   | -     |
| POST   | /api/auth/login    | Login            | -     |
| GET    | /api/movies/random | Get random movie | Token |
| GET    | /api/movies/:id    | Get movie by ID  | Token |
| POST   | /api/movies        | Create movie     | Admin |
| PUT    | /api/movies/:id    | Update movie     | Admin |
| DELETE | /api/movies/:id    | Delete movie     | Admin |
| GET    | /api/lists         | Get all lists    | Token |
| POST   | /api/lists         | Create list      | Admin |

Tech used
Frontend: React, React Router, Axios, Context API, SCSS

Backend: Node.js, Express, MongoDB, Mongoose, JWT, bcrypt

Admin: React, Material UI
