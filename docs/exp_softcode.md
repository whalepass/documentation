---
sidebar_position: 5
---
# Incrementing A Player's Experience Points (SOFTCODE)

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)


Called when player completes a specific game action to update experience point
To test specific DRAFT Battlepass, add X-Battlepass-Id header to request

| Token Type   | Location         | Format                               | Where To Find                                                       |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key                              |
| Header Token | X-Battlepass-Id  | X-Battlepass-Id: YOURTOKEN           | https://dashboard.whalepass.gg/campaigns                            |
| Path Field   | playerId         | { "playerId": "string" }             | You can find in response                                            |
| Body Field   | gameId           | { "gameId": "string" }               | https://www.whalepass.gg/documentation/tutorial#finding-your-game-id|
| Body Field   | actionId         | { "actionId": "string" }             | https://dashboard.whalepass.gg/game-actions                         |


Request:
```http
POST https://api.whalepass.gg/players/{playerId}/progress/action
{
  "gameId": "string",
  "actionId": "string"
}
```

Expected Response:
```http
{
  "playerBattlepassProgress": {
    "id": "string",
    "playerId": "string",
    "battlepassId": "string",
    "currentExp": 0,
    "lastCompletedLevel": 0,
    "completedLevels": [
      0
    ],
    "completedChallenges": [
      "string"
    ],
    "createdAt": "2023-12-27T09:53:34.155Z",
    "updatedAt": "2023-12-27T09:53:34.155Z"
  },
  "completedLevels": [
    {
      "id": "string",
      "battlepassId": "string",
      "level": 0,
      "expRequired": 0,
      "status": true,
      "freeTierRewards": [
        {
          "id": "string",
          "gameId": "string",
          "battlepassId": "string",
          "tokenId": "string",
          "amount": 0,
          "amountInDecimal": 0,
          "mediaUrl": "string"
        }
      ],
      "premiumTierRewards": [
        {
          "id": "string",
          "gameId": "string",
          "battlepassId": "string",
          "tokenId": "string",
          "amount": 0,
          "amountInDecimal": 0,
          "mediaUrl": "string"
        }
      ]
    }
  ]
}
```
