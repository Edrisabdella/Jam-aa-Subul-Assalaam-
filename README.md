# Jam'aa Subul-Assalaam Dargaggoota Waaccuu — Platform & Application

## 🌐 Overview

**Jam'aa Subul-Assalaam** is a complete, fully functional internal management platform for the Waaccuu Youth Association. Built as a **single HTML5 file**, it delivers over **70 interactive pages** that cover all aspects of the Jama'aa's operations—from member registration and committee management to Qiraatii teaching, finance tracking, online meetings, and administrative approvals.

The platform is designed to be self-contained, using `localStorage` for data persistence, making it easy to deploy on any static hosting service (Render, Netlify, GitHub Pages, etc.) without needing a backend server. However, it is structured to be upgradable to a full-stack solution with a Node.js backend and PostgreSQL database.

---

## 🚀 Key Features

- **Member Management** – Register, approve, view, and manage members with role-based access.
- **Admin Approval Workflow** – Amir or Admin Committee approves pending members using a secure password (`Jamaa*****`).
- **7 Committees** – Fully listed with leaders, contact details (email & phone), and dedicated pages.
- **Donation Center** – Display bank accounts (CBE, CBO, Awash, Rammis) with copy functionality, submit donations with optional receipt uploads, and view donation history.
- **Finance Module** – Track membership fees, contributions, monthly reports, and financial summaries.
- **Qiraatii Teaching Room** – Upload and manage lessons, audio, and video materials (Admin/Sheek/Ustaz only). Students can view and download.
- **Online Meeting Room** – Integrate Google Meet or Jitsi links; default Jitsi room provided.
- **Digital Library** – Placeholder for Qur'an, Hadiis, Tafsiir, Audio/Video, and PDF books.
- **Events & Notifications** – Schedule events, send internal notifications, and view recent activity.
- **Dashboard** – Real-time statistics (members, donations, reports, meetings) with quick action buttons.
- **Profile & Settings** – User profile view, dark/light mode toggle, language selector, and data backup/clear.
- **Audit Log** – Track all significant actions for transparency and security.
- **Responsive Design** – Works on desktop, tablet, and mobile devices.
- **Dark Mode** – Toggle between light and dark themes.

---

## 📋 Included Pages (70+)

The platform includes the following sections, each with multiple sub-pages and dynamic content:

| Module                | Pages                                                                 |
|-----------------------|-----------------------------------------------------------------------|
| **Home**              | Hero, Vision, Mission, Stats, Bank Accounts                           |
| **Dashboard**         | Overview, Quick Actions, Recent Activity                              |
| **Members**           | List, Add, Edit (via registration), Approve, Delete                   |
| **Register**          | Member registration form with committee selection                     |
| **Approvals**         | Pending members list, Amir approval panel                             |
| **Committees**        | All 7 committees with leaders and contacts                           |
| **Donations**         | Bank accounts, donation form, history                                 |
| **Finance**           | Membership fee records, total contributions, payer list               |
| **Qiraatii Room**     | Lessons, Audio, Video tabs; upload for Admin/Teachers                 |
| **Meeting Room**      | Google Meet / Jitsi iframe integration                                |
| **Library**           | Qur'an, Hadiis, Tafsiir, Audio, Video, PDF (placeholders)             |
| **Events**            | List and manage upcoming events                                       |
| **Notifications**     | View all system notifications                                         |
| **Reports**           | Weekly and monthly reports, generate sample reports                   |
| **Gallery**           | Image gallery placeholder                                             |
| **Profile**           | User account details, membership status                               |
| **Settings**          | Dark mode, language, clear data, backup                               |
| **Admin Panel**       | System status, audit log, backup creation                             |
| **Login/Logout**      | Simple email/password authentication (local)                          |

---

## 🏛️ Committees & Leadership

The platform includes the following seven committees with their leaders as per the constitution:

1. **Koree Bulchinsaa Jama'aa** – Amir: Engineer Jemal Nuure, Vice: Ustaaz Abdulaziz Sileshi, Secretary: Hundee Yuusuf
2. **Koree Hawaasummaa** – Amir: Dr Lammi, Vice: Roba Abrahim
3. **Koree Maallaqaa** – Amir: Hiriirsaa Jamaal, Vice: Shafi Abdella, Secretary: Abdeta Tofik, Auditors: Ibrahim Abdulahi & Yasin Abdella
4. **Koree Toohannoo fi Hordoffii** – Amir: Shamshu Aliyi, Vice: Arif Yeshixila, Secretary: Adinan Hashim
5. **Koree Qiraatii** – Amir: Roba Muhe, Vice: Abdusemed Usmail
6. **Koree Da'awaa fi Irshad** – Amir: Jafar Usmail, Vice: Ammaar
7. **Koree Qindeeysituu Araddootaa** – Amir: Abdurezak Aliyi, Vice: Falmata Yusuf, Secretary: Abdi Ibrahim

Each leader's contact details (email and phone) are displayed and clickable for direct communication.

---

## 💰 Bank Accounts

The following accounts are displayed in the Donation and About sections, with a copy-to-clipboard button:

| Bank        | Account Number        |
|-------------|-----------------------|
| CBE         | 1000631440014         |
| CBO         | 1003700549944         |
| Awash Bank  | 014251470950000       |
| Rammis Bank | 1010000332401         |

---

## 🔐 Roles & Permissions

- **Guest** – View public pages (Home, About, Committees).
- **Member** – Registered and approved; can view members, donate, access Qiraatii materials (view only), join meetings, and manage profile.
- **Teacher/Sheek/Ustaz** – Can upload materials to the Qiraatii room (in addition to member permissions).
- **Admin/Amir** – Full control: approve members, manage all content, view audit logs, and perform administrative actions.

The Amir password for bulk approval is **`Jamaa*****`** (hardcoded, not displayed on the UI).

---

## 🧩 Data Persistence

All data (members, donations, Qiraatii materials, notifications, etc.) is stored in the browser's `localStorage` using a `jsams_` prefix. This allows the platform to work entirely offline and be deployed as a static site. Data can be backed up as a JSON file via the Admin panel.

---

## 🛠️ Technologies Used

- **HTML5** – Structure and semantics.
- **CSS3** – Custom properties, flexbox, grid, animations, dark/light mode.
- **JavaScript (Vanilla)** – All logic, DOM manipulation, state management, local storage, file handling.
- **Font Awesome** – Icons for UI enhancement.
- **Google Fonts** – System fonts for performance.

---

## 📦 Deployment

### Option 1: Single HTML File Deployment

1. Download the `index.html` file.
2. Upload it to any static hosting service:
   - **Render** – Use the "Static Site" option.
   - **Netlify** – Drag and drop the file.
   - **GitHub Pages** – Add the file to a repository and enable Pages.
   - **Vercel** – Deploy as a static site.

### Option 2: Full-Stack Upgrade (Future)

The platform is designed to be extended with:
- **Backend**: Node.js + Express
- **Database**: PostgreSQL
- **Authentication**: JWT, Firebase
- **File Storage**: Cloudinary
- **Mobile App**: Flutter

The current single-file version serves as a **proof-of-concept** and a fully functional starter, but can be migrated to a production-grade MERN or PERN stack.

---

## 🔧 Usage Guide

### For Members
1. **Register** – Fill out the registration form; wait for admin approval.
2. **Login** – Use your registered email and password.
3. **Profile** – View and update your information.
4. **Donate** – Submit donations and upload receipts.
5. **Qiraatii** – Access lessons, audio, and video materials uploaded by teachers.
6. **Meetings** – Join online meetings via the embedded iframe.
7. **Events** – Check upcoming activities.

### For Committee Leaders
- View your committee's page with contact details.
- If you are a teacher/Sheek/Ustaz, you can upload Qiraatii materials.

### For Amir / Admin
- **Approvals** – Review pending members and approve them individually or bulk-approve with the Amir password.
- **Audit Log** – Monitor all actions performed on the platform.
- **Backup** – Download a JSON backup of all data.
- **Settings** – Toggle dark mode, clear data, etc.

---

## 📂 Project Structure (Single File)

Although the entire application is in one HTML file, it is organized internally as:

- **CSS** – Inline styles with variables for theming.
- **HTML** – All pages are `div.page` elements, shown/hidden via JavaScript.
- **JavaScript** – State management, rendering functions, event handlers, and utilities.

---

## 🧪 Testing & Validation

- **Cross-browser**: Works on Chrome, Firefox, Edge, Safari.
- **Responsive**: Tested on mobile, tablet, and desktop.
- **Data Integrity**: All actions are logged; data persists across sessions.

---

## 🚧 Future Enhancements

- Connect to a real backend with PostgreSQL.
- Email/SMS notifications.
- Google Calendar integration for events.
- Advanced search and filtering.
- Mobile app (Flutter) for Android and iOS.
- Payment gateway integration (Chapa, Telebirr, etc.).
- Multi-language support (Afaan Oromo, Arabic, Amharic).

---

## 📄 License

This project is proprietary and intended for the exclusive use of **Jam'aa Subul-Assalaam Dargaggoota Waaccuu**. Redistribution or commercial use without permission is prohibited.

---

## 🙏 Acknowledgments

- The Jama'aa leadership and members for their vision.
- All contributors who helped design and review the platform.

---

## 📬 Contact

For support or inquiries, please contact the Jama'aa administration at:
**Email**: jamaasubulassalaam@gmail.com  
**Website**: [https://jam-aa-subul-assalaam.onrender.com](https://jam-aa-subul-assalaam.onrender.com)

---

*Built with ❤️ for the community.*