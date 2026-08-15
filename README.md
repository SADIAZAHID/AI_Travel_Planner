# 🌍 AI Travel Planner

An AI-powered travel planning web application that helps users decide **where to travel based on their budget, number of people, travel duration, interests, weather, accommodation, and other real-world travel information**.

The application combines **React.js, FastAPI, real-time APIs, and AI** to generate personalised travel recommendations.

---

## ✨ Features

### 👤 User Input

Users provide a few simple details:

* Starting location
* Destination *(optional)*
* Travel budget
* Number of people
* Number of days
* Travel interests
* Preferred travel type

The destination can either be entered by the user or recommended by the AI based on their requirements.

### 🤖 AI Travel Recommendations

The AI analyses the collected information and provides:

* Recommended destinations
* Destination suitability score
* Budget compatibility
* Personalised recommendations
* Reasons to visit
* Reasons to reconsider
* Alternative destinations

### 💰 Smart Budget Planning

The application estimates the overall trip cost, including:

* Transportation
* Hotel/accommodation
* Food
* Activities
* Miscellaneous expenses

Example:

```text
Total Budget:       PKR 40,000
Estimated Cost:     PKR 34,500
Remaining Budget:   PKR 5,500
```

### 🌦️ Real-Time Weather

The application retrieves real weather information and helps users determine whether the destination is suitable for their planned trip.

### 🏨 Accommodation

Users can see recommended accommodation options and estimated prices where available through the selected travel APIs.

### 📍 Places to Visit

The application provides:

* Tourist attractions
* Popular places
* Restaurants
* Activities
* Nearby locations

### 🗺️ Travel Information

The application can provide:

* Distance
* Estimated travel time
* Transportation information
* Nearby attractions
* Location information

### 🗓️ AI-Generated Itinerary

The AI can create a day-by-day travel plan based on:

* Number of days
* Budget
* Interests
* Destination
* Available attractions

Example:

```text
Day 1
• Arrival
• Hotel check-in
• Local sightseeing

Day 2
• Main attractions
• Lunch
• Outdoor activities

Day 3
• Nature/Adventure activities
• Local food

Day 4
• Shopping
• Departure
```

---

# 🏗️ Tech Stack

## Frontend

* React.js
* JavaScript
* HTML5
* CSS3
* React Router
* Fetch API / Axios

## Backend

* Python
* FastAPI
* REST APIs

## AI

The project will use a free/low-cost AI API with a suitable free tier.

The AI will be responsible for:

* Travel recommendations
* Destination comparison
* Itinerary generation
* Budget analysis
* Personalised travel advice

## External APIs

The application will use real APIs for information such as:

* Weather
* Places
* Maps/distance
* Accommodation
* Currency conversion

The exact APIs will be selected based on their **current free-tier availability and project requirements**.

---

# 🧠 Application Architecture

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     React.js        │
                    │      Frontend       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      FastAPI        │
                    │       Backend       │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
      ┌─────────────┐   ┌─────────────┐   ┌─────────────┐
      │ Weather API │   │ Places API  │   │  Maps API   │
      └─────────────┘   └─────────────┘   └─────────────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       AI API        │
                    │ Recommendation      │
                    │ & Itinerary Engine  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  Travel Dashboard   │
                    │       React.js      │
                    └─────────────────────┘
```

---

# 📁 Project Structure

```text
AI-Travel-Planner/
│
├── frontend/
│   ├── public/
│   │
│   └── src/
│       ├── components/
│       │   ├── Navbar.jsx
│       │   ├── TravelForm.jsx
│       │   ├── BudgetCard.jsx
│       │   ├── WeatherCard.jsx
│       │   ├── HotelCard.jsx
│       │   ├── PlaceCard.jsx
│       │   ├── Itinerary.jsx
│       │   └── Recommendation.jsx
│       │
│       ├── pages/
│       │   ├── Home.jsx
│       │   ├── Results.jsx
│       │   └── About.jsx
│       │
│       ├── services/
│       │   └── api.js
│       │
│       ├── App.jsx
│       ├── main.jsx
│       └── index.css
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   │
│   │   ├── routes/
│   │   │   ├── travel.py
│   │   │   ├── weather.py
│   │   │   └── places.py
│   │   │
│   │   ├── services/
│   │   │   ├── ai_service.py
│   │   │   ├── weather_service.py
│   │   │   ├── places_service.py
│   │   │   └── travel_service.py
│   │   │
│   │   └── models/
│   │       └── travel.py
│   │
│   ├── requirements.txt
│   └── .env
│
├── .gitignore
└── README.md
```

---

# 🔄 How It Works

### Step 1 — User enters requirements

Example:

```text
Starting Location: Islamabad
Destination: Optional
Budget: PKR 40,000
People: 2
Duration: 4 days
Interests: Mountains, Nature, Food
```

### Step 2 — Backend receives the request

React sends the information to the FastAPI backend.

### Step 3 — Backend collects real-world information

FastAPI communicates with the required APIs to retrieve:

* Weather
* Places
* Distance
* Accommodation information
* Currency information

### Step 4 — AI analyses the information

The AI receives the user's requirements together with the collected travel information.

It determines:

* Which destinations fit the budget
* Whether the weather is suitable
* Which places should be visited
* Estimated expenses
* Whether the trip is worthwhile
* Alternative options

### Step 5 — React displays the result

The frontend presents everything in a clean travel dashboard.

---

# 🔐 Environment Variables

API keys must **never be placed directly inside React frontend code**.

The backend will use environment variables.

Example:

```env
AI_API_KEY=your_api_key
WEATHER_API_KEY=your_api_key
PLACES_API_KEY=your_api_key
MAPS_API_KEY=your_api_key
```

The `.env` file should never be committed to GitHub.

---

# 🚀 Installation

## 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Travel-Planner.git

cd AI-Travel-Planner
```

---

## 2. Setup React frontend

```bash
cd frontend
npm install
npm run dev
```

---

## 3. Setup FastAPI backend

Open another terminal:

```bash
cd backend
python -m venv .venv
```

### Windows

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the backend:

```bash
uvicorn app.main:app --reload
```

The FastAPI API will be available locally through the configured development port.

---

# 🧪 Development Roadmap

## Phase 1 — Project Setup

* [ ] Create GitHub repository
* [ ] Create React application
* [ ] Create FastAPI backend
* [ ] Connect frontend and backend
* [ ] Configure environment variables

## Phase 2 — Frontend

* [ ] Build landing page
* [ ] Build travel form
* [ ] Add destination search
* [ ] Add budget input
* [ ] Add people selector
* [ ] Add duration selector
* [ ] Add interests

## Phase 3 — Real APIs

* [ ] Integrate weather API
* [ ] Integrate places API
* [ ] Integrate maps/distance API
* [ ] Integrate accommodation data
* [ ] Integrate currency conversion

## Phase 4 — AI

* [ ] Connect AI API
* [ ] Create travel recommendation prompt
* [ ] Generate destination recommendations
* [ ] Generate budget analysis
* [ ] Generate itinerary
* [ ] Generate alternative destinations

## Phase 5 — Results Dashboard

* [ ] Destination overview
* [ ] Weather card
* [ ] Budget breakdown
* [ ] Hotel recommendations
* [ ] Places to visit
* [ ] Restaurant recommendations
* [ ] AI recommendation
* [ ] Day-by-day itinerary

## Phase 6 — Quality

* [ ] Loading states
* [ ] Error handling
* [ ] API failure handling
* [ ] Responsive design
* [ ] Mobile-friendly UI
* [ ] Input validation

## Phase 7 — Deployment

* [ ] Push frontend to GitHub
* [ ] Deploy React frontend
* [ ] Deploy FastAPI backend
* [ ] Configure environment variables
* [ ] Test production APIs
* [ ] Connect frontend to production backend
* [ ] Add live demo to GitHub README

---

# 🌐 Deployment Goal

The project is designed to be deployed using **free hosting/free tiers wherever practical**.

Target architecture:

```text
GitHub
   │
   ├── React Frontend
   │       ↓
   │   Free Web Hosting
   │
   └── FastAPI Backend
           ↓
       Free Backend Hosting
           ↓
       External APIs
```

The final project should have:

* ✅ Public GitHub repository
* ✅ Live website
* ✅ Working backend API
* ✅ Real travel information
* ✅ AI recommendations
* ✅ Responsive UI
* ✅ Secure API keys

---

# 🎯 Future Improvements

Possible future features include:

* User authentication
* Save trips
* Favourite destinations
* Trip history
* Google Maps integration
* Interactive maps
* Travel expense tracker
* Group trip planning
* Flight information
* Real-time hotel availability
* Currency conversion
* Multi-language support
* Dark mode
* PWA/mobile version
* AI travel chatbot

---

# 👩‍💻 Author

**Sadia Zahid**

Computer Science | React.js | Python | FastAPI | AI

---

## ⭐ Project Goal

The goal of AI Travel Planner is to transform travel planning from:

> **"Where should I go?"**

into:

> **"Based on my budget, time, interests, weather, and available options — where should I go, what should I do, and is it actually worth going?"**

This project demonstrates practical experience with **React.js, REST APIs, Python/FastAPI, AI integration, API orchestration, data processing, and deployment.**
