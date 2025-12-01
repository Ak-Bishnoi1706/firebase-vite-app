🛒 Admin Dashboard – E‑Commerce Management
An Admin Dashboard built with HTML, CSS, JavaScript, Firebase, and Firestore to manage customers and orders in an e‑commerce application.
This project provides a simple interface for administrators to view, update, and delete orders, as well as navigate to customer details.

🚀 Features
🔐 Authentication
- Admin login/logout flow
- Logout button redirects back to index.html
📦 Orders Management
- Fetch orders from Firestore (orders collection)
- Filter orders by customer ID (via URL query parameter)
- Render orders in a table with:
- Order ID, Customer, Product, Date, Status, Total
- Status dropdown (Pending, Shipped, Delivered, Cancelled)
- Delete button to remove orders
- View button to navigate to customer details
👤 Customer View
- Redirect to customers.html?id={customerId}
- Highlight rows belonging to the selected customer for 3 seconds
🔎 Search
- Search box to filter orders by ID, customer name, date, or status

🛠️ Tech Stack
- Frontend: HTML, CSS, Bootstrap, Vanilla JavaScript
- Backend: Firebase Firestore
- Development: Local with vite

📂 Project Structure
e-commerce/
└── major project/
    └── firebase-vite-app/
        ├── index.html
        ├── style.css
        ├── main.js
        ├── customers.html
        ├── orders.html
        ├── firebase-debug.log
        ├── package-lock.json
        ├── package.json
        └── public/
            └── image.png

- index.html → Your landing/login page.
- style.css → Global styles for dashboard and pages.
- main.js → Entry point for Firebase + Vite app logic.
- customers.html → Customer details view.
- orders.html → Orders management view.
- firebase-debug.log → Firebase logs (auto-generated).
- package.json & package-lock.json → Node/Vite dependencies.
- public/image.png → Static assets (logo, icons, etc.).

⚙️ Setup Instructions
- GITHUB REPO https://github.com/AK-Bishnoi1706/firebase-vite-app.git
cd e-commerce/major project/firebase-vite-app
- Configure Firebase
- Create a Firebase project in Firebase Console 
- Enable Firestore Database

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID"
};

- Use Vite's dev server:
- npm install
- npm run dev
- Then open the local server link (usually http://localhost:5173) in your browser.
- Firestore Collection Setup Ensure Firestore has an orders collection with fields:
- customerId (Number/String)
- customer (String)
- product (String)
- date (String)
- status (String)
- total (Number)

🧩 Future Enhancements
- Add authentication with Firebase Auth
- Pagination for large order datasets
- Export orders to CSV/Excel
- Customer profile with order history

👩‍💻 Author
Developed by Anita Bishnoi – BCA student passionate about full‑stack web development and premium UI/UX dashboards.
- GitHub: AK-Bishnoi1706
