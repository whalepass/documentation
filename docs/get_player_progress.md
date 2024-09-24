---
sidebar_position: 7
---
# Getting Player's Progress

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)


To test a specific DRAFT Battlepass, add X-Battlepass-Id header to request

Request:
```http
GET https://api.whalepass.gg/players/{playerId}/progress?gameId={gameId}
```

Expected Response:
```http
{
  "player": {
    "id": "string",
    "externalPlayerId": "string",
    "gameId": "string",
    "userId": "string",
    "accountConnected": true,
    "createdAt": "2023-12-27T10:58:40.064Z",
    "updatedAt": "2023-12-27T10:58:40.064Z"
  },
  "battlepassProgress": {
    "battlepassId": "string",
    "currentExp": 0,
    "lastCompletedLevel": 0,
    "levels": [
      {
        "id": "string",
        "battlepassId": "string",
        "level": 0,
        "expRequired": 0,
        "active": true,
        "freeTierRewards": [
          {
            "id": "string",
            "gameId": "string",
            "battlepassId": "string",
            "name": "string",
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
            "name": "string",
            "amount": 0,
            "amountInDecimal": 0,
            "mediaUrl": "string"
          }
        ],
        "completed": true
      }
    ],
    "challenges": [
      {
        "id": "string",
        "battlepassId": "string",
        "name": "string",
        "startDate": "2023-12-27T10:58:40.064Z",
        "endDate": "2023-12-27T10:58:40.064Z",
        "active": true,
        "premium": true,
        "rewards": [
          {
            "id": "string",
            "gameId": "string",
            "battlepassId": "string",
            "name": "string",
            "amount": 0,
            "amountInDecimal": 0,
            "mediaUrl": "string"
          }
        ],
        "completed": true
      }
    ]
  }
}
```
