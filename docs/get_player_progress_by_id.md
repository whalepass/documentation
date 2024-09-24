---
sidebar_position: 8
---
# Getting Player(s) Progress by Player Id Search


![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)


To test specific DRAFT Battlepass, add X-Battlepass-Id header to request

Request:
```http
GET https://api.whalepass.gg/players/progress
{
  "playerIds": ["string"],
  "gameId": "string"
}
```

Expected Response:
```http
{
  "progressList": [
    {
      "player": {
        "id": "string",
        "externalPlayerId": "string",
        "gameId": "string",
        "userId": "string",
        "accountConnected": true,
        "createdAt": "2023-12-27T10:59:15.390Z",
        "updatedAt": "2023-12-27T10:59:15.390Z"
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
            "startDate": "2023-12-27T10:59:15.390Z",
            "endDate": "2023-12-27T10:59:15.390Z",
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
  ]
}
```
