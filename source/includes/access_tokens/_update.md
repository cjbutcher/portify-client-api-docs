## [POST] Refresh Access Token

```shell
curl "ENV_URL/clients/access_tokens/refresh"
  -X POST
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
    "app_id": APP_ID,
    "access_token": ACCESS_TOKEN,
    "refresh_token": REFRESH_TOKEN
  }'
```
> The above command returns JSON structured like this:

```json
{
  "access_token": {
    "access_token": "W801u8F66xSb_qNRJLXwxczorZVhUku3MM5vSP95arY",
    "expires_at": "2018-11-17T16:08:35.519Z",
    "refresh_token": "FXbXovzza53FyiJMnEyEobDd",
    "refreshed_at": "2018-11-16T16:08:35.519Z"
  }
}
```

This endpoint returns your access token with an updated expires_at timestamp and regenerated refresh_token.

Parameter | Description
--------- | -----------
app_id | Your application's app id [required]
access_token | The access token you wish to refresh [required]
refresh_token | The correct corresponding refresh token for the access token [required]
