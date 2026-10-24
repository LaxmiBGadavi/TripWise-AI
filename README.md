# ✈️ TripWise AI — Smart Travel Planning & Trip Management Platform

TripWise AI is a full-stack, AI-powered travel planning platform designed to help users plan personalized trips, estimate travel expenses, organize itineraries, and manage their travel plans in one place.

The goal is to simplify travel planning by combining intelligent recommendations, budget management, and a user-friendly web interface.

## 🚀 Project Overview

Planning a trip often requires switching between multiple websites to research destinations, organize activities, estimate expenses, and manage travel details.

TripWise AI aims to bring these tasks together in one platform. Users can enter their destination, travel duration, budget, and interests to generate a personalized sample itinerary.

## ✨ Key Features

- **Smart Trip Planning:** Generate day-by-day itineraries based on destination, duration, budget, and interests.
- **Budget Estimation:** Calculate a daily budget and organize estimated travel expenses.
- **Interest-Based Recommendations:** Customize plans for sightseeing, food, beaches, adventure, nature, culture, and shopping.
- **Trip Management:** Save and retrieve travel plans using a database.
- **REST API Integration:** Connect the frontend and backend through structured API endpoints.
- **AI-Ready Architecture:** Designed for integration with large language models to provide contextual travel recommendations.
- **Responsive Interface:** Access the travel planner through a modern web interface.

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js, HTML, CSS, JavaScript |
| Backend | Python, FastAPI |
| Database | SQLite |
| API | REST APIs |
| AI Integration | LLM API integration — planned enhancement |
| Development Tools | VS Code, Git, GitHub |
| API Testing | FastAPI Swagger UI, Postman |

## 🏗️ System Architecture

```text
                 User
                  |
                  v
          React.js Frontend
                  |
                  v
           FastAPI Backend
                  |
          +-------+-------+
          |               |
          v               v
   Trip Generation    SQLite Database
   and Budget Logic   Saved Trip Details
          |
          v
    Personalized
    Sample Itinerary
```

## 📂 Project Structure

```text
TripWise-AI/
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   └── .env.example
├── frontend/
│   ├── index.html
│   ├── package.json
│   └── src/
│       ├── App.jsx
│       ├── main.jsx
│       └── styles.css
├── .gitignore
└── README.md
```

## ⚙️ Installation and Setup

### Prerequisites

Install the following before running the project:

- Python 3.10 or later
- Node.js and npm
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/TripWise-AI.git
cd TripWise-AI
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Set Up the Backend

Open a terminal in the project root and run:

```bash
cd backend
py -m venv .venv
```

Activate the virtual environment on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI server:

```bash
uvicorn main:app --reload
```

The backend will run at:

`http://127.0.0.1:8000`

Interactive API documentation:

`http://127.0.0.1:8000/docs`

### 3. Set Up the Frontend

Open a second terminal in the project root:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed in the terminal, usually:

`http://127.0.0.1:5173`

Keep both terminals running while using the application.

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | API welcome message |
| GET | `/health` | Check backend status |
| POST | `/api/trips/generate` | Generate a sample itinerary |
| POST | `/api/trips` | Save a trip |
| GET | `/api/trips` | Retrieve saved trips |
| GET | `/api/trips/{trip_id}` | Retrieve a specific trip |

### Example Request

Send a POST request to `/api/trips/generate`:

```json
{
  "destination": "Goa",
  "days": 3,
  "budget": 10000,
  "interests": [
    "beaches",
    "food",
    "sightseeing"
  ]
}
```

The API returns a structured itinerary containing activities for each day and the requested budget information.

## 🗄️ Database

SQLite is used to store saved trip details, including:

- Destination
- Trip duration
- Budget
- Travel interests
- Generated itinerary
- Estimated cost
- Creation timestamp

The database is created automatically when the backend starts.

## 🧠 AI Integration

The platform is designed to support LLM-based itinerary generation and conversational travel assistance.

The current MVP uses a template-based itinerary generator. A real LLM API and live travel data integrations are future enhancements, not features of the current implementation.

## 🔮 Future Enhancements

- Integrate an LLM API for contextual itinerary generation.
- Add live flight and hotel search through supported travel APIs.
- Integrate maps and location-based recommendations.
- Add user authentication and personalized profiles.
- Introduce collaborative trip planning.
- Add detailed expense tracking and budget alerts.
- Support itinerary export to PDF.
- Deploy the frontend and backend to cloud hosting.

## 💼 Business Value

TripWise AI aims to reduce the effort involved in organizing travel by combining itinerary planning, budget estimation, and trip management in a single interface.

Potential users include solo travelers, families, students, and groups looking for an organized way to plan trips.

## 👩‍💻 Learning Outcomes

This project demonstrates practical experience with:

- Full-stack application architecture
- Python backend development
- REST API design and integration
- React-based user interfaces
- Relational data persistence
- Input validation and error handling
- Git and GitHub version control
- Planning future AI and external API integrations

## 👤 Author
**Laxmi Gadavi**
**AI & Data Science Engineering Graduate**


---

*TripWise AI — Plan smarter. Travel better.*
