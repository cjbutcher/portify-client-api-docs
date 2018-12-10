## [GET] List Enabled Perk Views

```shell
curl "ENV_URL/api/v1/clients/enabled_perk_views?app_id=APP_ID&date=2018-11-15"
  -X GET
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -H "Authorization": "Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "enabled_perk_views": [
    {
      "id": "9ffb5c2c-5e65-4a03-bfaa-d06426222b2a",
      "client_identifier": "135622",
      "enabled_perk_id": "0fad8ba8-52fb-48a0-ad40-21146e4b62e1",
      "created_at": "2018-11-15T16:10:24.499Z"
    },
    {
      "id": "ff7df128-74f9-4a5b-a154-e574f823f705",
      "client_identifier": "123412",
      "enabled_perk_id": "3de61f43-7ff3-445b-9f4f-f1e2982d37e7",
      "created_at": "2018-11-15T16:09:24.506Z"
    },
    ...
  ],
  "metadata": {
    "total_record_count": 3488,
    "record_count": 50,
    "continuation_token": 1544458255
  }
}
```

This endpoint returns up to 50 perk views per request for a given date. Subsequent pages of results can be retrieved by repeating the request and passing in the continuation token returned by the previous response.

Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
date | The date for which you would like to retrieve records (YYYY-MM-DD) [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
