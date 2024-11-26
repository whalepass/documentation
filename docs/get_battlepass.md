---
sidebar_position: 10
---
# Getting A Battlepass with Levels, Challenges and Rewards

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)

| Token Type   | Location         | Format                               | Where To Find                              |
|:------------:|:----------------:|--------------------------------------:|-------------------------------------------:|
| Header Token | X-API-KEY        | X-API-KEY: YOURTOKEN                 | https://dashboard.whalepass.gg/api-key     |
| Path Field   | {battlepassId}   | battlepass/{battlepassId}            | https://dashboard.whalepass.gg/campaigns   |

Request:
```http
GET https://api.whalepass.gg/battlepass/{battlepassId}?includeLevels=true&includeChallenges=true
```

Request Parameters:
```http
includeLevels: default false
includeChallenges: default false
```

Expected Response:
```http
{
  "id": "string",
  "gameId": "string",
  "organizationId": "string",
  "name": "string",
  "noTimeLimit": true,
  "premiumPrice": 0,
  "startDate": "2023-10-26T09:33:23.970Z",
  "endDate": "2023-10-26T09:33:23.970Z",
  "challenges": [
    {
      "id": "string",
      "battlepassId": "string",
      "name": "string",
      "startDate": "2023-10-26T09:33:23.970Z",
      "endDate": "2023-10-26T09:33:23.970Z",
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
      ]
    }
  ],
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
      ]
    }
  ]
}
```
