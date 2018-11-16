## [GET] List Enabled Perk Redemptions

```shell
curl "ENV_URL/clients/enabled_perk_redemptions?app_id=APP_ID&created_since=2018-11-15%2016:10:24.487877"
  -X GET
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -H "Authorization": "Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "enabled_perk_redemptions": [
    {
      "id": "9ffb5c2c-5e65-4a03-bfaa-d06426222b2a",
      "enrolment_id": "be8172a5-a51b-462d-816b-1ebc63ca0b95",
      "brand": "Amazon",
      "value": 5000,
      "discount": 5.0,
      "money_saved": 250,
      "created_at": "2018-11-15T16:10:24.499Z"
    },
    {
      "id": "ff7df128-74f9-4a5b-a154-e574f823f705",
      "enrolment_id": "be8172a5-a51b-462d-816b-1ebc63ca0b95",
      "brand": "Tesco",
      "value": 10000,
      "discount": 5.0,
      "money_saved": 500,
      "created_at": "2018-11-15T16:10:24.506Z"
    },
    {
      "id": "e6b76648-fef8-4df8-9093-47633f5cd67d",
      "enrolment_id": "be8172a5-a51b-462d-816b-1ebc63ca0b95",
      "brand": "Spotify",
      "value": 10000,
      "discount": 10.0,
      "money_saved": 1000,
      "created_at": "2018-11-15T16:10:24.513Z"
    }
  ]
}
```

This endpoint returns up to 50 perk redemptions created since the specified time.

Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required] 
created_since | Datetime from which you'd like to receive the next page of perk redemptions [required]
