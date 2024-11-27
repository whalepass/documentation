---
sidebar_position: 3
---
# Enrolling A Player To Your Game

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

This table specifies the token types used in API requests, along with the corresponding headers and formats. It also provides the relevant URLs for each token.

| Token Type   | Location         | Format                               | Where To Find                                                       |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key                              |
| Body Field   | gameId           | { "gameId": "string" }               | https://www.whalepass.gg/documentation/tutorial#finding-your-game-id|
| Body Field   | playerId         | { "playerId": "string" }             | Provided by the user                                                |

Request:
```http
POST https://api.whalepass.gg/enrollments
{
  "playerId": "string", 
  "gameId": "string" 
}
```
Expected Response:
```http
{
  "id": "string",
  "externalPlayerId": "string",
  "gameId": "string",
  "userId": "string",
  "accountConnected": true,
  "createdAt": "2023-12-26T13:05:17.428Z",
  "updatedAt": "2023-12-26T13:05:17.428Z"
}
```
