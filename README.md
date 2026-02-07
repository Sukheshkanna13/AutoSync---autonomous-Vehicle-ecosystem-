<h1 align="center">🚗 Glytch AutoSync</h1>

<p align="center">
  <em>Autonomous Vehicle Agent Ecosystem & Digital Twin</em>
</p>

<p align="center">
  <b>Real-Time Telemetry</b> • <b>Predictive Maintenance</b> • <b>AI Diagnostics</b>
</p>

<div align="center">
  <img src="https://img.shields.io/badge/Status-Prototype-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/AI-Predictive-blue?style=for-the-badge" />
</div>

---

### 📖 Overview
**Glytch AutoSync** is an intelligent vehicle ecosystem that bridges the gap between raw automotive data and actionable insights. By creating a **Digital Twin** of the vehicle, the system ingests real-time OBD-II telemetry via WebSockets to perform live health monitoring.

At its core, a **Backend Neural Core** (FastAPI) processes data streams to predict failures before they happen, while the **Frontend Control Center** (React) provides drivers with an interactive AI assistant and visualization of their vehicle's status.

---

### 🏗️ System Architecture
The system follows a high-performance, event-driven architecture designed for low latency and high availability.

![Architecture Diagram](https://github.com/user-attachments/assets/2ee7a356-74c8-4c56-9f97-bd8df32b08b4)

### 🚀 Key Features

* **⚡ Real-Time Telemetry:** Ingests live RPM, Temperature, and DTC (Diagnostic Trouble Codes) via WebSockets.
* **🧠 Predictive ML Engine:** Uses `.keras` and `.pkl` models to calculate failure probabilities for critical components.
* **🚘 Digital Twin Dashboard:** A React-based visualization that mirrors the physical state of the car in real-time.
* **🤖 AI Chat Assistant:** A conversational agent that answers queries like *"Why is my engine light on?"* or *"Book a service."*
* **🚨 Voice Alert Service:** Automated voice calls/alerts for critical failures (e.g., engine overheating).

---

### 💻 Tech Stack

<div align="center">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/WebSockets-010101?style=for-the-badge&logo=socket.io&logoColor=white" />
  <br />
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white" />
  <img src="https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <br />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white" />
</div>

---

### 🔄 Process Flow

1.  **Data Ingestion:** The `OBD-II Simulation` module streams vehicle metrics to the `Backend Neural Core`.
2.  **Analysis:** The **AI Analysis Engine** processes the stream against the **Model Vault** (historical data models).
3.  **Inference:** The **Predictive Engine** calculates the probability of component failure.
4.  **Action:**
    * **Low Risk:** Updates the **Digital Twin** visualization.
    * **High Risk:** Triggers the **Voice Alert Service** and prompts the user to book maintenance via the **Booking Manager**.

---

### 🛠️ Getting Started

```bash
# Clone the repository
git clone [https://github.com/Sukheshkanna13/Glytch-AutoSync.git](https://github.com/Sukheshkanna13/Glytch-AutoSync.git)

# Navigate to backend and install dependencies
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

# Navigate to frontend and run
cd frontend
npm install
npm start
