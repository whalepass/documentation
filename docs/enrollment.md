---
sidebar_position: 3
---
# Enrolling A Player To Your Game

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

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
