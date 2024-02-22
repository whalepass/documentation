---
sidebar_position: 11
---
# Redirect Player to Player's Dashboard

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

For getting a redirection link so player can connect or create a Whalepass account

Request:
```http
GET https://api.whalepass.gg/players/{playerId}/redirect?gameId={gameId}
```

Expected Response:
```http
{
  "redirectionLink": "string"
}
```
