## [GET] List Bank Connections

```shell
curl "ENV_URL/api/v1/clients/bank_connections?app_id=APP_ID"
  -X GET
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -H "Authorization": "Token token=ACCESS_TOKEN"
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
      "created_at": "2018-11-15T16:10:24.506Z",
    }
  ],
  "metadata": {
    "total_records": 2,
    "continuation_token": null
  }
}
```

This endpoint returns bank connections, ordered by timestamp (most recent first). Subsequent pages of results can be retrieved by repeating the request and passing in the continuation token returned by the previous response.

Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
