---
sidebar_position: 3
---
# Enrolling A Player To Your Game

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

| Left |  Center  | Right |
|:-----|:--------:|------:|
| L0   | **bold** | $1600 |
| L1   |  `code`  |   $12 |
| L2   | _italic_ |    $1 |

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
