## [PATCH] Update Enrolment

```shell
curl "ENV_URL/clients/api/v1/enrolments" \
  -X PATCH \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Token token=ACCESS_TOKEN" \
  -d '{
    "app_id": APP_ID,
    "enrolment": {
      "active": true,
      "email": "user_0@fake-company.com",
      "score": 3333
    }
  }'
```
> The above command returns JSON structured like this:

```json
{
    "enrolment": {
      "id": "c7bf2a8f-7508-45d1-946e-b510d5130653",
      "email": "user_0@fake-company.com",
      "name": "user 0",
      "phone": "01234 567891",
      "score": "2345",
      "client_identifier": "10000",
      "active": true,
      "created_at": "2019-04-12T11:05:11.317Z"
    },
    "message": {
      "type": "success",
      "text": "Enrolment updated successfully",
      "code": "enrolment_update_success"
    }
}
```

This update endpoint is used to remove an enrolment.


Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
enrolment[:active] | Whether the enrolment is active or not [optional]
enrolment[:email] | The email required to identify the enrolment to remove [required]
enrolment[:score] | The score associated with this enrolment [optional]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
