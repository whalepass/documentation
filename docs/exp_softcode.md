---
sidebar_position: 5
---
# Incrementing A Player's Experience Points (SOFTCODE)

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)


Called when player completes a specific game action to update experience point
To test specific DRAFT Battlepass, add X-Battlepass-Id header to request

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
