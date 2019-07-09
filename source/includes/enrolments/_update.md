## [PATCH] Update Enrolment

```shell
curl 'ENV_URL/clients/api/v1/enrolments?app_id=APP_ID&email=EMAIL' \
-X PATCH \
-H 'Accept: application/json' \
-H "Authorization: Token token=ACCESS_TOKEN" \
-H 'Content-Type: application/json' \
```
> The above command returns JSON structured like this:

```json
{
    "email": "EMAIL",
    "message": {
        "type": "success",
        "text": "Enrolment updated successfully",
        "code": "updated"
    }
}
```

This update endpoint is used to remove an enrolment.


Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
email | The email required to identify the enrolment to remove [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
