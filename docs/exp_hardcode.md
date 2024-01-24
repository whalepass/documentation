---
sidebar_position: 4
---
# Incrementing A Player's Experience Points (HARDCODE)

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)


Request:
```http
POST https://api.whalepass.gg/players/{playerId}/progress/exp
{
  "gameId": "string",
  "additionalExp": 0
}
```

> Expected response: 200 OK



| ⚠️ Warning                                                         |
|--------------------------------------------------------------------|
|This endpoint doesn't accept **battlepassId** in the request body anymore. It will work for the ACTIVE battlepass of the game in the request body. To test specific DRAFT Battlepass, add X-Battlepass-Id header to request|

