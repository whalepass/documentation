---
sidebar_position: 3
---
# Enrolling A Player To Your Game

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

Method	Token Type	Location	Format
GET	Bearer Token	Authorization Header	Authorization: Bearer YOURTOKEN
POST	Header Token	X-API-KEY Header	X-API-KEY: YOURTOKEN
GET	Query Token	Request Parameter	/endpoint?api_key=YOURTOKEN
DELETE	Bearer Token	Authorization Header	Authorization: Bearer YOURTOKEN
PUT	Header Token	X-API-KEY Header	X-API-KEY: YOURTOKEN

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
