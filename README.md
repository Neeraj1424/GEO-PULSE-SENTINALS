# OPEN-PLANT-DOCTOR
AI-powered plant disease detection system using MERN + l machine earning to identify crop diseases, estimate severity, and suggest treatments for farmers.  Alternative (slightly stronger positioning):  Open-source AI platform for plant disease detection with severity analysis and treatment recommendations, built using MERN and machine  learning
🌱 OpenPlant Doctor
AI-Powered Plant Disease Detection System (MERN Stack)
📌 Overview

OpenPlant Doctor is a MERN-based web application that helps farmers detect plant diseases using a simple leaf image.

The platform allows users to:

Upload a plant leaf image

Detect plant type and disease

Estimate severity level

Receive organic and chemical treatment recommendations

View preventive measures

The system is built with scalability, simplicity, and real-world agricultural usability in mind.

🎯 Problem Statement

Farmers often struggle to identify plant diseases early. Misdiagnosis can lead to:

Crop damage

Overuse of pesticides

Reduced yield

Financial loss

Most existing tools are either complex, not farmer-friendly, or require constant high-speed internet.

OpenPlant Doctor provides a simple, AI-powered, open-source solution built on MERN architecture.

🚀 Core Features

📸 Leaf image upload

🤖 AI-based disease detection

📊 Severity classification (Mild / Moderate / Severe)

🌿 Organic treatment suggestions

🧪 Chemical treatment suggestions

🛡 Preventive guidance

📱 Responsive UI

🔓 Open-source and extensible design

🛠 Tech Stack (MERN)
Frontend

React.js

Tailwind CSS (optional)

Axios (API communication)

Backend

Node.js

Express.js

Database

MongoDB (stores treatment data, disease info, user logs)

AI Integration

Python-based ML model (served via REST API)

Model: MobileNet / EfficientNet (PlantVillage dataset)

🧠 System Architecture
Client (React)
      ↓
Express API (Node.js)
      ↓
MongoDB (Disease & Treatment Data)
      ↓
AI Model Service (Python - Inference API)
Flow:

User uploads leaf image via React frontend.

Image is sent to Express backend.

Backend forwards image to AI model service.

AI returns:

Plant name

Disease class

Confidence score

Backend calculates severity level.

MongoDB fetches treatment recommendations.

Results are returned to frontend.

📊 Severity Classification Logic
Infection %	Severity Level
0–10%	Mild 🟢
10–30%	Moderate 🟡
30%+	Severe 🔴
📂 Project Structure
openplant-doctor/
│
├── client/                 # React Frontend
│   ├── src/
│   └── public/
│
├── server/                 # Node + Express Backend
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── middleware/
│   └── config/
│
├── ai-service/             # Python AI Inference Service
│   ├── model/
│   └── app.py
│
├── .env
├── package.json
└── README.md
⚙️ Installation Guide
1️⃣ Clone Repository
git clone https://github.com/your-username/openplant-doctor.git
cd openplant-doctor
2️⃣ Backend Setup
cd server
npm install
npm run dev

Create a .env file inside /server:

PORT=5000
MONGO_URI=your_mongodb_connection_string
AI_SERVICE_URL=http://localhost:8000
3️⃣ Frontend Setup
cd client
npm install
npm start
4️⃣ AI Service Setup
cd ai-service
pip install -r requirements.txt
python app.py
🌍 Impact

Enables early disease detection

Reduces unnecessary pesticide usage

Improves crop health

Supports small and marginal farmers

Promotes open agricultural AI

🔓 Contributing

We welcome contributions in:

Adding new crops & diseases

Improving model accuracy

Enhancing UI/UX

Expanding treatment database

Multilingual support

Steps:

Fork the repository

Create a new branch

Commit changes

Submit a pull request

🔮 Future Scope

Offline mobile version (ONNX / TensorFlow Lite)

WhatsApp-based plant diagnosis bot

Regional language interface

Real-time outbreak analytics

Farmer feedback dataset expansion

📜 License

This project is licensed under the MIT License.
