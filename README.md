# Web-Technology-work
# Word Antakshari Game

## Overview
The **Word Antakshari Game** is a web-based word game where players take turns providing words that start with the last letter of the previously given word. The game involves real-time validation using a MongoDB dictionary and a scoring system to track player performance.

## Features
- **User Authentication**: Players enter their names to start the game.
- **Random Word Generator**: The game starts with a randomly selected word from a MongoDB database.
- **Word Validation**: The entered word must start with the last letter of the previous word and exist in the dictionary.
- **Scoring System**: Points are awarded based on word length and streak.
- **Timer**: Players have limited time to enter a valid word.
- **Leaderboard**: Tracks top players based on their scores.

## Tech Stack
- **Frontend**: HTML, CSS, JavaScript, jQuery
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Additional Libraries**: Axios, Mongoose, CORS

## Installation
### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/try/download/community)

### Steps
1. **Clone the repository**
   ```sh
   git clone https://github.com/your-username/word-antakshari.git
   cd word-antakshari
   ```
2. **Install dependencies**
   ```sh
   npm install
   ```
3. **Start MongoDB** (Ensure MongoDB is running locally or provide a remote URI in `server.js`)
4. **Run the server**
   ```sh
   node server.js
   ```
5. **Access the game**
   Open `http://localhost:3000` in your browser.

## API Endpoints
### 1. Start Game
**Endpoint:** `GET /start`
- Returns a randomly selected starting word.

### 2. Submit Word
**Endpoint:** `POST /play`
- **Request Body:**
  ```json
  {
    "playerName": "Riya",
    "word": "apple"
  }
  ```
- **Response:** Validates the word and provides the next word if valid.

### 3. Leaderboard
**Endpoint:** `GET /leaderboard`
- Returns the top 10 players with their scores.

## File Structure
```
word-antakshari/
│── public/
│   ├── index.html
│   ├── style.css
│   ├── script.js
│── server.js
│── package.json
│── README.md
```



