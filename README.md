# TripSaathi 🧭

**TripSaathi** is a smart trip-planning website that helps users turn a travel idea into a practical, day-by-day itinerary. Users will be able to enter a destination, trip duration, starting point, budget, and interests, then discover relevant places and organize them into a route.

> **Project status:** Planning / initial development  
> This README describes the planned project. Features and integrations will be marked complete only after they are implemented and tested.

## ✨ Planned Features

- Enter a destination, starting point, trip duration, budget, and travel interests.
- Discover attractions relevant to the trip.
- Generate a day-by-day itinerary.
- Group nearby attractions to reduce unnecessary travel.
- Display places and routes on an interactive map.
- Consider available ratings, review counts, opening hours, weather, and route information.
- Save, edit, and revisit itineraries.
- Provide estimated travel times and costs with clear caveats.

## 🧰 Planned Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| Frontend | React, JavaScript, HTML, CSS | User interface and itinerary display |
| Frontend tooling | Vite, npm | Local development and package management |
| Backend | Java, Spring Boot | REST APIs and trip-planning logic |
| Database | PostgreSQL | Users, saved trips, places, and itinerary data |
| Database integration | Spring Data JPA | Accessing database records from Java |
| API testing | Postman | Testing backend endpoints |
| Version control | Git and GitHub | Tracking and sharing source code |
| External data | Maps, places, routing, and weather APIs | Place discovery and trip information |

The exact external providers will be selected after reviewing availability, API limits, licensing, and pricing.

## 🏗️ How It Will Work

1. The user submits trip preferences through the React frontend.
2. The frontend sends a request to the Spring Boot backend.
3. The backend validates the input and retrieves relevant place and route data from configured providers.
4. The itinerary planner filters and orders places based on interests, distance, time, and other available information.
5. The backend returns a structured itinerary as JSON.
6. The frontend displays the plan, map, and estimates.
7. When saving is implemented, the backend stores the trip in PostgreSQL.

```text
User
  |
  v
React Frontend
  |
  | HTTP / JSON
  v
Java + Spring Boot REST API
  |                    |
  v                    v
PostgreSQL       External APIs
                 Places / Routes /
                 Maps / Weather
  |
  v
Saved Trips and Itinerary Data
```

## 🗺️ Itinerary Quality and Data Accuracy

TripSaathi aims to make useful recommendations, not simply list popular attractions.

The planned itinerary logic may consider:

- User interests and budget
- Place ratings and review counts, where legally and technically available
- Distance between attractions
- Estimated travel time and visit duration
- Opening hours and closures, when current data is available
- Weather forecasts and disruption information, when available

**Important:** Travel times, costs, opening hours, reviews, and weather can change. Estimates will be labelled as estimates, and the app will communicate when information is unavailable or could not be verified. External data will be accessed according to each provider's terms; the project will not assume that review data is freely available from every provider.

## 🚀 Getting Started

The project is under initial development. Setup instructions will be expanded as each application component is added.

### Prerequisites

Install these tools as the relevant components are introduced:

- [Node.js (LTS)](https://nodejs.org/)
- [Java JDK](https://adoptium.net/)
- [Git](https://git-scm.com/)
- [PostgreSQL](https://www.postgresql.org/)
- [Postman](https://www.postman.com/) (optional, for API testing)

### Frontend (planned)

After the React/Vite frontend has been created in this repository, run:

```bash
npm install
npm run dev
```

Use the local URL printed by Vite in your terminal.

### Backend (planned)

The Spring Boot backend will be added in a separate directory. Its build and run instructions will be documented once the backend structure and configuration are in place.

### Environment variables and API keys

External API credentials should be stored in environment variables or an appropriate local configuration file that is excluded from version control. **Never commit API keys, passwords, database credentials, or other secrets to GitHub.**

An `.env.example` file will be added when the required configuration is known.

## 🛣️ Development Roadmap

- [ ] Plan the MVP and project structure
- [ ] Build the responsive React home page and trip form
- [ ] Create itinerary cards using sample data
- [ ] Build Spring Boot REST endpoints
- [ ] Connect the React frontend to the backend
- [ ] Design the PostgreSQL schema and persist trips
- [ ] Integrate a place-discovery provider
- [ ] Add interactive maps and route estimates
- [ ] Implement itinerary generation and daily scheduling
- [ ] Add available weather and disruption checks
- [ ] Add authentication and user-specific saved trips
- [ ] Test error cases and data quality
- [ ] Deploy the application
- [ ] Add screenshots, demo details, and final setup instructions

## 📁 Planned Repository Structure

The structure may evolve as development progresses.

```text
trip-saathi/
├── frontend/          # React + Vite application
├── backend/           # Java + Spring Boot application
├── docs/              # Architecture notes and project documentation
├── .gitignore
└── README.md
```

## 🧪 Testing Plan

Testing will be added as features are implemented. Planned checks include:

- Invalid or incomplete trip inputs
- Trips with no matching attractions
- External API timeouts or unavailable data
- Itineraries that exceed the available time
- Database save and retrieval failures
- Authentication and access to saved trips
- Responsive layout on desktop and mobile

## 🔐 Privacy and Security

- Keep API keys and credentials out of source control.
- Validate user input on the backend.
- Protect saved trips so users can access only the data they are authorized to view.
- Request only the personal information required for the product.
- Follow the privacy, licensing, and usage terms of external data providers.

## 🤝 Contributing

This is currently a learning project. Suggestions, issues, and constructive feedback are welcome. As the codebase develops, contribution and local-development guidelines will be added here.

## 📄 License

A license has not been selected yet. Until one is added to the repository, reuse and redistribution permissions should not be assumed.

---

**Built as a learning project to explore full-stack development with React, Java, Spring Boot, PostgreSQL, and travel-related APIs.**
