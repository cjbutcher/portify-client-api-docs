## [GET] List Bank Connections

```shell
curl "ENV_URL/clients/api/v1/bank_connections?app_id=APP_ID&date=2018-11-15" \
  -X GET \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "bank_connections": [
    {
      "id": "9ffb5c2c-5e65-4a03-bfaa-d06426222b2a",
      "client_identifier": "123412",
      "created_at": "2018-11-15T16:10:24.499Z",
    },
    {
      "id": "9ffb5c2c-5e65-4a03-bfaa-d06426222b2a",
      "client_identifier": "876543",
      "created_at": "2018-11-15T16:10:23.511Z",
    },
    ...
  ],
  "metadata": {
    "total_record_count": 123,
    "record_count": 50,
    "continuation_token": "1544458255327"
  }
}
```

This endpoint returns up to 50 bank connections per request for a given date. Subsequent pages of results can be retrieved by repeating the request and passing in a continuation token, received in the previous response.

Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
date | The date for which you would like to retrieve records (YYYY-MM-DD) [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
