**Project Title:** Cricket Team Management API

**Description:**

I designed and implemented a RESTful API for managing a cricket team using Node.js and Express.js. This project involved creating API endpoints to perform various operations on a SQLite database, including player management. The API provides the following functionalities:

1. **GET Players (API 1):** Retrieves a list of all players in the cricket team, displaying their details such as player ID, name, jersey number, and role.

2. **Add Player (API 2):** Allows the addition of new players to the team. The API auto-generates player IDs and stores player information, including name, jersey number, and role, in a SQLite database.

3. **Get Player by ID (API 3):** Retrieves detailed information about a specific player based on their player ID. This endpoint returns player-specific details, including their name, jersey number, and role.

4. **Update Player Details (API 4):** Provides the ability to update player details, such as their name, jersey number, or role, by specifying the player ID. This feature ensures accurate and up-to-date player information.

5. **Remove Player (API 5):** Enables the removal of players from the team based on their player ID. This feature helps in managing the team roster efficiently.

I used CommonJS modules for modularization and SQLite as the database system to store player information. The project also involved deploying the API on the Render platform to make it accessible over the internet.

This project showcased my skills in creating RESTful APIs, working with databases, and deploying applications in a real-world environment. It also demonstrated my proficiency in Node.js and Express.js, essential technologies for backend web development.

**Deployment Link**: [https://sample-node-cricketteam-deploying.onrender.com](url)

The table `cricket_team` contains the following columns,

| Columns       | Type    |
| ------------- | ------- |
| player_id     | INTEGER |
| player_name   | TEXT    |
| jersey_number | INTEGER |
| role          | TEXT    |

### API 1

#### Path: `/players/`

#### Method: `GET`

#### Description:

Returns a list of all players in the team

#### Response

```
[
  {
    playerId: 1,
    playerName: "Lakshman",
    jerseyNumber: 5,
    role: "All-rounder"
  },

  ...
]
```

### API 2

#### Path: `/players/`

#### Method: `POST`

#### Description:

Creates a new player in the team (database). `player_id` is auto-incremented

#### Request

```
{
  "playerName": "Vishal",
  "jerseyNumber": 17,
  "role": "Bowler"
}
```

#### Response

```
Player Added to Team
```

### API 3

#### Path: `/players/:playerId/`

#### Method: `GET`

#### Description:

Returns a player based on a player ID

#### Response

```
{
  playerId: 1,
  playerName: "Lakshman",
  jerseyNumber: 5,
  role: "All-rounder"
}
```

### API 4

#### Path: `/players/:playerId/`

#### Method: `PUT`

#### Description:

Updates the details of a player in the team (database) based on the player ID

#### Request

```
{
  "playerName": "Maneesh",
  "jerseyNumber": 54,
  "role": "All-rounder"
}
```

#### Response

```
Player Details Updated

```

### API 5

#### Path: `/players/:playerId/`

#### Method: `DELETE`

#### Description:

Deletes a player from the team (database) based on the player ID

#### Response

```
Player Removed
```

<br/>

Use `npm install` to install the packages.
