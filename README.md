# 🎲 Dice Game (Real-Time Multiplayer)

A real-time multiplayer dice game built with **Node.js, Express, Socket.IO and MongoDB**.

Players can join the game, roll dice in real time, and see updates instantly thanks to **WebSockets with Socket.IO**. Game results and scores are stored in **MongoDB**.

---

# 🚀 Features

- Real-time multiplayer gameplay
- Dice rolling mechanics
- Live updates using **Socket.IO**
- Score tracking
- Game state synchronization between players
- MongoDB database for storing game results
- REST API for retrieving leaderboard data

---

# 🧱 Tech Stack

Frontend
- HTML
- CSS
- JavaScript

Backend
- Node.js
- Express
- Socket.IO
- MongoDB
- Mongoose
- dotenv

---

# 📦 Installation

Clone the repository:

```bash
git clone https://github.com/Flizzyar/socketio-dice-game.git
cd socketio-dice-game
```

Install dependencies:

```bash
npm install
```

---

# ⚙️ Environment Variables

Create a `.env` file in the project root.

Example:

```env
PORT=3000

# MongoDB Atlas
MONGO_USER=your_user
MONGO_PASS=your_password
MONGO_CLUSTER=your_cluster_url
MONGO_DB=your_db_name
```


---

# ▶️ Run the Project

Start the server:

```bash
npm run dev
```

or

```bash
npm start
```

Open the browser and play the game.

---

# ⚡ Real-Time Gameplay (Socket.IO)

The game uses **Socket.IO** to synchronize game events between players.

Examples of real-time events:

- Player joins game
- Dice rolled
- Score updates
- Player turn switch
- Game finished

This ensures both players see updates instantly without refreshing the page.

---

# 📡 API Endpoints

### Get Leaderboard

```
GET /games/leaderboard
```

Returns top scores stored in MongoDB.

Example response:

```json
[
  {
    "player": "Player1",
    "score": 120
  }
]
```

---

# 🎮 Game Rules

1. Two players take turns rolling the dice.
2. Each roll adds to the **current score**.
3. Rolling a **1 resets the current score** and switches player.
4. Players can **hold** to save their score.
5. The first player to reach the winning score wins the game.

---
