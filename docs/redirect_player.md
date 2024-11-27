---
sidebar_position: 12
---
# Redirect Player to Player's Dashboard

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

For getting a redirection link so player can connect or create a Whalepass account

| Token Type   | Location         | Format                               | Where To Find                                                       |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key                              |
| Header Token | X-Battlepass-Id  | X-Battlepass-Id: YOURTOKEN           | https://dashboard.whalepass.gg/campaigns                            |
| Request Param   | playerId         | \{ "playerId": "string" \}             | You can find in response                                            |
| Request Param   | gameId           | \{ "gameId": "string" \}               | https://www.whalepass.gg/documentation/tutorial#finding-your-game-id|

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
