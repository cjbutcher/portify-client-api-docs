## [POST] Create Enrolment

```shell 
curl "ENV_URL/clients/api/v1/enrolments" \
  -X POST \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Token token=ACCESS_TOKEN" \
  -d '{
    "app_id": APP_ID,
    "enrolment": {
    	"name": "Chris Fairbank",
    	"email": "example@example.com",
    	"phone": 07654776556",
    	"client_identifier": "10000",
    	"active": true,
			"score": 3333
    }
  }'
```
> The above command returns JSON structured like this:

```json
{
    "enrolment": {
      "id": "c7bf2a8f-7508-45d1-946e-b510d5130653",
      "email": "example@example.com",
      "name": "Chris Fairbank",
      "phone": "07654776556",
      "score": "3333",
      "client_identifier": "10000",
      "active": true,
      "created_at": "2019-04-12T11:05:11.317Z"
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
enrolment[:email] | Email for the user being enrolled  [required]
enrolment[:phone] | Phone number of the user enrolled [required]
enrolment[:name] | The name of user being enrolled [optional]
enrolment[:score] | The score associated with this enrolment [optional]
enrolment[:client_identifier] | Unique client identifier [optional]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
