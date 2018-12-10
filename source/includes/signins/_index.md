## [GET] List Sign-ins

```shell
curl "ENV_URL/api/v1/clients/signins?app_id=APP_ID"
  -X GET
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -H "Authorization": "Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "signins": [
    {
      "client_identifier": "123412",
      "last_seen": "2018-11-15T16:10:24.499Z",
      "total_visits": 12
    },
    {
      "client_identifier": "876543",
      "last_seen": "2018-11-15T16:10:24.506Z",
      "total_visits": 5
    }
  ],
  "metadata": {
    "total_records": 2,
    "continuation_token": null
  }
}
```

This endpoint returns user sign-ins, ordered by timestamp (most recent first). Subsequent pages of results can be retrieved by repeating the request and passing in the continuation token returned by the previous response.

Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
