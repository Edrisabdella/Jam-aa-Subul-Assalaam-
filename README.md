# Jam-aa-Subul-Assalaam-
Jam'aa Subul-Assalaam Dargaggoota Waaccuu 
🕌 Jam'aa Subul-Assalaam – Full‑Stack Platform
A comprehensive digital platform for Jam'aa Subul-Assalaam Dargaggoota Waaccuu – managing members, committees, donations, teaching, and administration – all in one modern, internally‑functional application.

https://i.ibb.co/PsGDsNnn/jamaa-subul-salam.jpg

📌 Overview
This platform serves as the central hub for the Jam'aa Subul-Assalaam community. It enables member registration, committee coordination, donation tracking, Quran teaching (with voice recording), training material sharing, online meeting scheduling, and an admin panel for approvals – all backed by a secure Node.js + MongoDB backend.

The frontend is a single, responsive HTML page that communicates via REST APIs, making it easy to deploy and maintain.

✨ Key Features
👥 Member Management
Self‑registration – anyone can sign up (pending approval).

Admin approval – the Amir (or committee) approves members using a secure password (Jamaadmin).

Role‑based profiles – members can have roles like Amiira, Itti Aana, Barreessaa, etc.

Real‑time member list with status badges (pending / approved / rejected).

🏛️ Seven Committee Rooms
Each committee has:

Leaders' contact details (email & phone) displayed.

Dedicated file upload space – members can upload reports, documents, etc.

Full CRUD – upload, view, download, and delete files (admin).

🤲 Donation & Finance
Donation progress bar – track total raised against a goal (500,000 ETB).

Donation history – list of all donations with amounts and messages.

Receipt upload – members can upload proof of membership fee payments (image files).

📖 Quran Teaching Room
Voice recording – Ustaaz can record directly in the browser and save the audio.

Video/audio upload – share recitations, lectures, and teaching materials.

Student tracking – register students with their reading level (Beginner to Master).

📚 Training Materials
Upload educational resources (PDF, video, audio) categorized as:

Quran

Hadiis

Kitaab

General

Download and delete functionality.

🎥 Meeting Room
Schedule online meetings by adding Google Meet links with date/time.

All meetings are listed with join buttons.

🔐 Admin Panel
Secure login with the Amir’s password (Jamaadmin).

Approve or reject pending member registrations.

Full data export/import (JSON) for backup and migration.

Clear all data (reset) option.

🛠️ Tech Stack
Layer	Technology
Backend	Node.js, Express, MongoDB (Mongoose)
Frontend	Vanilla HTML5, CSS3, JavaScript (Fetch API)
Auth	Simple token‑based admin authentication
File Storage	Base64 encoding in MongoDB (ready to switch to Cloudinary/S3)
Deployment	Render, Heroku, or any Node.js host
📦 Repository
GitHub: https://github.com/Edrisabdella/Jam-aa-Subul-Assalaam-.git

Email Contact: jamaasubulassalaam@gmail.com

🚀 Getting Started
Prerequisites
Node.js (v14+)

MongoDB Atlas account (or local MongoDB instance)

Git

Installation
Clone the repository

bash
git clone https://github.com/Edrisabdella/Jam-aa-Subul-Assalaam-.git
cd Jam-aa-Subul-Assalaam-
Install dependencies

bash
npm install
Set up environment variables
Create a .env file in the root directory:

env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
ADMIN_PASSWORD=Jamaadmin   # Change this in production
Run the server

bash
npm start
For development with auto‑reload:

bash
npm run dev
Open your browser at http://localhost:5000

🔧 Environment Variables
Variable	Description	Default
PORT	Port the server listens on	5000
MONGODB_URI	MongoDB connection string (Atlas recommended)	(required)
ADMIN_PASSWORD	Password for admin panel access	Jamaadmin
📡 API Endpoints (REST)
All endpoints are prefixed with /api.

Method	Endpoint	Description	Auth
POST	/admin/login	Login with password → returns token	Public
GET	/members	List all approved members	Public
POST	/members/register	Register a new member (pending)	Public
GET	/members/pending	List pending members	Admin Token
PUT	/members/approve/:id	Approve a pending member	Admin Token
DELETE	/members/reject/:id	Reject a pending member	Admin Token
DELETE	/members/:id	Delete an approved member	Admin Token
GET	/donations	Get all donations	Public
POST	/donations	Create a donation	Public
DELETE	/donations/all	Delete all donations	Admin Token
GET	/receipts	List all uploaded receipts	Public
POST	/receipts	Upload a receipt (base64 image)	Public
GET	/committees/:committee	Get files for a specific committee	Public
POST	/committees	Upload a file to a committee	Public
DELETE	/committees/:id	Delete a committee file	Admin Token
GET	/quran	List all Quran teaching materials	Public
POST	/quran	Upload a Quran teaching file	Public
DELETE	/quran/:id	Delete a Quran file	Admin Token
GET	/students	List all students	Public
POST	/students	Add a student	Public
GET	/training	List training materials	Public
POST	/training	Upload training material	Public
DELETE	/training/:id	Delete training material	Admin Token
GET	/meetings	List all meetings	Public
POST	/meetings	Create a meeting	Public
DELETE	/meetings/:id	Delete a meeting	Admin Token
GET	/admin/export	Export all data as JSON	Admin Token
POST	/admin/import	Import data from JSON	Admin Token
DELETE	/admin/clear	Clear all data	Admin Token
Admin Token – obtained after login; include in x-admin-token header.

🌐 Deployment (Render)
Push your repository to GitHub.

On Render, create a New Web Service and connect your repo.

Set:

Build Command: npm install

Start Command: node server.js

Add environment variables:

MONGODB_URI – your Atlas connection string

ADMIN_PASSWORD – your secure password

Deploy! The app will be live at your Render URL.

📖 Usage Guide
For Members
Register – fill in the form under the “Members” page; your request goes to pending.

Donate – use the “Donations” page; your donation appears instantly.

Upload Receipt – in “Finance”, upload a screenshot of your payment.

Access Committee Rooms – switch to the desired committee, upload or download files.

Quran Teaching – students can be added; Ustaaz can record voice or upload lessons.

Training Materials – browse and download resources.

Join Meetings – click the “Join” button to open Google Meet links.

For Admins (Amir / Committee)
Login – go to “Admin Panel”, enter password Jamaadmin (change via env).

Approve/Reject – pending members appear; approve or reject them.

Manage Data – export/import data for backup, or clear all data.

🔒 Security Considerations
The admin token is stored in localStorage – for production, consider using HTTP‑only cookies.

All file data is stored as base64 in MongoDB – this is fine for moderate usage; for large files, switch to cloud storage.

Input validation is basic – add more robust validation in production.

🤝 Contributing
Contributions are welcome!
If you'd like to improve the platform, please:

Fork the repository.

Create a feature branch.

Commit your changes.

Push and open a Pull Request.

For major changes, please open an issue first to discuss what you would like to change.

📄 License
This project is open‑source and available under the MIT License.

📬 Contact
For any questions, suggestions, or support, reach out to:

Email: jamaasubulassalaam@gmail.com

GitHub Issues: https://github.com/Edrisabdella/Jam-aa-Subul-Assalaam-/issues

May Allah bless this effort and make it a source of benefit for the community. 🤲