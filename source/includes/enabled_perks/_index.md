## [GET] List Enabled Perks

```shell
curl "ENV_URL/clients/api/v1/enabled_perks?app_id=APP_ID" \
  -X GET \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "enabled_perks": [
    {
      "id": "9ffb5c2c-5e65-4a03-bfaa-d06426222b2a",
      "brand": "Amazon",
      "title": "5.0% off orders at Amazon",
      "discount": 5.0,
      "custom": false,
      "created_at": "2018-11-15T16:10:24.499Z"
    },
    {
      "id": "ff7df128-74f9-4a5b-a154-e574f823f705",
      "brand": "Tesco",
      "title": "5.0% off at Tesco",
      "discount": 5.0,
      "custom": false,
      "created_at": "2018-11-15T16:10:24.506Z"
    },
    ...
  ],
  "metadata": {
    "total_record_count": 76,
    "record_count": 50,
    "continuation_token": "1544458255327"
  }
}
```

This endpoint returns up to 50 enabled perks per request. Subsequent pages of results can be retrieved by repeating the request and passing in a continuation token, received in the previous response.


Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
