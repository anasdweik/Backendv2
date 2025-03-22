
Charity Pulse
Charity Pulse is a full-stack donation platform built with React (frontend) and Flask (backend), allowing users to register, log in, post donation items, and view donations.

🌐 Live Demo
(Add link here if deployed)

📁 Project Structure
arduino
Copy
Edit
donation-website/
├── backend/
│   ├── app.py
│   ├── config.py
│   ├── models.py
│   ├── routes.py
│   └── ...
├── frontend/
│   ├── public/
│   ├── src/
│   ├── package.json
│   └── ...
└── README.md
🛠️ Technologies Used
Frontend: React, React Router, Axios, Material UI (MUI)

Backend: Flask, SQLAlchemy, Flask-Login, Flask-CORS

Database: MySQL

Others: Context API for auth, bcrypt for password hashing

🚀 Getting Started
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/your-repo-name.git
cd donation-website
2. Setup the Backend
2.1 Create Virtual Environment
bash
Copy
Edit
python -m venv .venv
.venv\Scripts\activate    # On Windows
2.2 Install Requirements
bash
Copy
Edit
pip install -r requirements.txt
2.3 Update Database Credentials
Edit backend/config.py and make sure this line has your correct credentials:

python
Copy
Edit
SQLALCHEMY_DATABASE_URI = 'mysql+pymysql://root:yourpassword@localhost/donation_db'
2.4 Create the Database
Make sure MySQL server is running, then in your MySQL client:

sql
Copy
Edit
CREATE DATABASE donation_db;
2.5 Initialize the DB
bash
Copy
Edit
flask shell
>>> from models import db
>>> db.create_all()
>>> exit()
3. Setup the Frontend
bash
Copy
Edit
cd frontend
npm install
4. Run the Project
4.1 Build React for Production
bash
Copy
Edit
npm run build
4.2 Go back to Backend and Start Flask
bash
Copy
Edit
cd ../backend
python app.py
Now open http://localhost:5000 in your browser.

👥 Features
User Registration & Login

Protected Routes (like Profile)

Post and View Donations

Serve React via Flask

MySQL Database

JWT/Session-based Auth with Flask-Login

🧪 Notes
Make sure index.html is inside frontend/build/

React static files are served from Flask using this in app.py:

python
Copy
Edit
app = Flask(__name__, static_folder='../frontend/build', static_url_path='/')
💬 Contact
Made with ❤️ by Anas
GitHub: @anasdweik

