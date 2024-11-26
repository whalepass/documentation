---
sidebar_position: 3
---
# Enrolling A Player To Your Game

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

| Token Type   | Location         | Format                               | URLs                                      |
|:------------:|:---------------:|-------------------------------------:|------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                | https://dashboard.whalepass.gg/api-key   |
| Header Token | X-Battlepass-Id  | X-Battlepass-Id: YOURTOKEN          | https://dashboard.whalepass.gg/campaigns |



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
