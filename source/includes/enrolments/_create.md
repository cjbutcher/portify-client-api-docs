## [POST] Create Enrolment

```shell 
 curl "ENV_URL/clients/api/v1/enrolments?app_id=APP_ID" \ 
   -X POST \
   -H 'Accept: application/json' \
   -H "Authorization: Token token=ACCESS_TOKEN" \
   -H 'Content-Type: application/json' \ 
   -d '{
        "enrolment": {
          "client_identifier": CLIENT_ID,
          "email": EMAIL,
          "phone": PHONE,
          "name": NAME
        }
       }'
```
> The above command returns JSON structured like this:

```json
{
    "enrolment": {
        "id": "XXXX",
        "email": "XXXX",
        "name": "XXXX",
        "phone": "XXXX",
        "client_identifier": "XXXX",
        "active": "XXXX",
        "score": "XXXX",
        "created_at": "XXXX",
    },
    "message": {
        "type": "success",
        "text": "Enrolment created successfully",
        "code": "enrolment_create_success"
    }
}
```

This endpoint creates an enrolment for a given email.


Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
email | Email for the user being enrolled  [required]
phone | Phone number of the user enrolled [required]
name | The name of user being enrolled [required]
client identifier | Unique client identifier [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
