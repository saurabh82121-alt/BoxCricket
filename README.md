Build an Android application (Kotlin + Jetpack Compose, MVVM architecture, Repository pattern) for managing Box Cricket matches.

Functional Requirements

Match Setup

Screen to create a new match with:

Match Name, Date, Place

Number of overs (configurable)

Rules: max overs per bowler, wide/no-ball extra run value

Team & Player Management

Create teams

Add players to teams (fields: name, photo, mobile number, role [batsman/bowler/all-rounder])

Edit/update player profile anytime

Match Flow

Start the match → live score tracking screen

Track and update:

Runs, 4s, 6s per player

Run-outs, catches, wickets per bowler/fielder

After each over → automatically change bowler/batsman (with manual override option)

Mark a player as out and record bowler against dismissal

Allow mid-match player edits

Scoring & Leaderboard

Display overall team score (runs, wickets, overs)

Display individual player stats

Generate leaderboard with MVP points (performance-based)

Role-based access → associate players can only see leaderboard

Data Storage & Sync

Use MongoDB (Remote DB) for storing matches, teams, players, scores, leaderboards

Provide REST APIs (Node.js/Express or Java Spring Boot) for:

POST /match (create match)

PUT /match/:id (update match)

DELETE /match/:id (delete match)

GET /match/:id (fetch match details)

Offline mode: store data locally (Room/SQLite) if no internet → sync to MongoDB when online → remove local copy once synced

UI/UX

Use Jetpack Compose UI with Material3 design

Beautiful icons for batsman, bowler, fielder, and app logo

Easy navigation: Match Setup → Team Creation → Live Match → Leaderboard

Technical Requirements

Android Client: Kotlin, Jetpack Compose, MVVM, Room DB (for offline), Retrofit for API calls

Backend: Node.js + Express (or Spring Boot if Java) with MongoDB Atlas

Sync Logic: Background worker (WorkManager) to sync local DB with remote MongoDB when network available

Code Style: Clean architecture, modular, well-commented, production-ready
