---
sidebar_position: 9
---
# Getting A Battlepass with Levels, Challenges and Rewards

![Whalepass.gg](https://i.imgur.com/zwUqWaS.png)


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
          "amountInDecimal": 0
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
          "amountInDecimal": 0
        }
      ],
      "premiumTierRewards": [
        {
          "id": "string",
          "gameId": "string",
          "battlepassId": "string",
          "name": "string",
          "amount": 0,
          "amountInDecimal": 0
        }
      ]
    }
  ]
}
```
