## [GET] List Sign Ins

```shell
curl "ENV_URL/clients/api/v1/signins?date=2018-12-10&app_id=APP_ID"
  -X GET
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -H "Authorization": "Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "sign_ins": [
    {
      "id": "39c01faf-94f9-44e5-98d9-d498b90b369a",
      "client_identifier": "123412",
      "created_at": "2018-11-15T16:10:24.499Z"
    },
    {
      "id": "139ddec3-3bf0-4795-be21-37ad9fa1eedf",
      "client_identifier": "136789",
      "created_at": "2018-11-15T16:10:21.543Z"
    },
    ...
  ],
  "metadata": {
    "total_record_count": 2345,
    "record_count": 50,
    "continuation_token": "1544458255327"
  }
}
```

This endpoint returns user sign-ins on a given date, ordered by created_at (oldest first). Subsequent pages of results can be retrieved by repeating the request and passing in the continuation token returned by the previous response.

Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
date | The date for which you would like to retrieve records (YYYY-MM-DD) [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
