## [GET] List Enrolments

```shell
curl "ENV_URL/clients/api/v1/enrolments?app_id=APP_ID" \
  -X GET \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Token token=ACCESS_TOKEN" \
```
> The above command returns JSON structured like this:

```json
{
  "enrolments": [
    {
        "id": "c7bf2a8f-7508-45d1-946e-b510d5130653",
        "email": "user_0@fake-Company.com",
        "name": "user 0",
        "phone": "01234 567891",
        "score": "2345",
        "client_identifier": "10000",
        "active": true,
        "created_at": "2019-04-12T11:05:11.317Z"
    },
    {
        "id": "8ebac528-9ace-4465-bc43-5a9e35a4a08e",
        "email": "user_1@fake-company.com",
        "name": "user 1",
        "phone": "01234 567891",
        "score": "3456",
        "client_identifier": "10001",
        "active": true,
        "created_at": "2019-04-12T11:05:11.432Z"
    },
    ...
  ],
     "metadata": {
       "total_record_count": 111,
       "record_count": 50,
       "continuation_token": "1555067114697"
     }
}
```

This endpoint returns up to 50 enrolments per request. Subsequent pages of results can be retrieved by repeating the request and passing in a continuation token, received in the previous response.
Subsequent pages of results can be retrieved by repeating the request and passing in a continuation token, received in the previous response.


Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
app_id | Your application's app id [required]
continuation_token | The token returned by the previous request, if retrieving a subsequent page of results [optional]
