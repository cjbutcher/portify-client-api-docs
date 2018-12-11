## [POST] Create Access Token

```shell
curl "ENV_URL/clients/api/v1/access_tokens"
  -X POST
  -H "Authorization": "Token token=SECRET"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
    "app_id": APP_ID
  }'
```
> The above command returns JSON structured like this:

```json
{
  "access_token": {
    "access_token": "W801u8F66xSb_qNRJLXwxczorZVhUku3MM5vSP95arY",
    "expires_at": "2018-11-17T15:35:30.182Z",
    "refresh_token": "qaKgQejogCPUyNfs8WNF5qEx",
    "refreshed_at": null
  }
}
```

This endpoint returns an access token valid for up to 24 hours, before it needs to be refreshed.

Parameter | Description
--------- | -----------
SECRET | Your application's secret token [required]
app_id | You application's app id [required]
