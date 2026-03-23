# Map_Chat_Nexus
 Geospatial Real-Time Communication PlatformMap-Chat Nexus is a location-aware full-stack web application designed to bridge the gap between physical proximity and digital interaction. Unlike traditional social media, this platform allows users to instantly connect in "Digital Town Squares" based on their real-time GPS coordinates without needing pre-existing contact information.
 
 📌 Project Overview: 
 
 In high-density environments like university campuses or large-scale conclaves (e.g., VCC-2026), information silos often prevent efficient coordination. Map-Chat Nexus solves this by using geospatial indexing to create transient, location-based chat zones.Problem Statement: Modern social platforms are identity-based, requiring "follows" or "invites," which creates friction for spontaneous local coordination and real-time event management.Solution: A "Location-as-an-Identity" model that uses Spring Boot, PostGIS, and WebSockets to enable secure, proximity-triggered messaging.
 
 🏗 System Architecture: 
 
 The project follows a decoupled Client-Server Architecture optimized for high-concurrency geospatial updates:Frontend (Presentation Layer): A React-based SPA that renders an interactive map using Leaflet.js, handling real-time user marker updates via WebSockets.Backend (Service Layer): A Spring Boot application managing RESTful APIs for authentication and a WebSocket broker for low-latency message routing.Database (Persistence Layer): PostgreSQL with the PostGIS extension for spatial queries (ST_DWithin) and Redis for ephemeral location caching.Security Layer: Implements JWT (JSON Web Tokens) and server-side Coordinate Fuzzing to ensure user privacy.
 
🛠 Tech Stack: 

Frontend: React.js, Next.js, Leaflet.js, Tailwind CSS; Backend: Java, Spring Boot, Spring Security (JWT), WebSockets; Database: PostgreSQL + PostGIS, RedisDevOpsDocker, Docker Compose; Testing: Postman, JMeter (Performance Testing)

🧩 Modules
  1. User Management
   Handles secure registration, JWT-based login, and profile management. It includes privacy toggles like "Ghost Mode" to control location visibility.
  2. Core Processing
   (Geospatial Engine)The "brain" of the app. It calculates user proximity using PostGIS and dynamically assigns users to active "Nexus Zones" (Geofences) based on their latitude and longitude.
  3. Database Management
    Manages the lifecycle of spatial data. It ensures data integrity for thousands of concurrent coordinate updates while providing fast retrieval for nearby "Pin Drops."
  4. Reporting & Analytics
     A dashboard for administrators (like Event Coordinators) to view Heatmaps of user density and communication metrics to optimize crowd flow.

🚀 Key Features
Dynamic Geofencing: Automatically join chats for specific campus zones (Library, IDEA Lab, Canteen).
Privacy Fuzzing: Protects user identity by adding a mathematical offset to precise GPS data before broadcasting.
Real-Time Pins: Users can drop "Global Pins" on the map to mark events, issues, or meetups.
Cross-Platform Responsiveness: Mobile-first design for students on the move.
