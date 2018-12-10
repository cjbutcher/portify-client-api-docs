## [GET] List Bank Disconnections

```shell
curl "ENV_URL/api/v1/clients/bank_disconnections?app_id=APP_ID"
  -X GET
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -H "Authorization": "Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "bank_disconnections": [
    {
      "id": "9ffb5c2c-5e65-4a03-bfaa-d06426222b2a",
      "client_identifier": "123412",
      "created_at": "2018-11-15T16:10:24.499Z",
    },
    {
      "id": "9ffb5c2c-5e65-4a03-bfaa-d06426222b2a",
      "client_identifier": "876543",
      "created_at": "2018-11-15T16:10:24.506Z",
    },
    ...
  ],
  "metadata": {
    "total_record_count": 12,
    "record_count": 12,
    "continuation_token": 1544458255
  }
}
```

This endpoint returns bank disconnections, ordered by created_at (most recent first). Subsequent pages of results can be retrieved by repeating the request and passing in the continuation token returned by the previous response.

Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
