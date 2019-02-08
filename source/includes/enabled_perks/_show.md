## [GET] Show Enabled Perk

```shell
curl "ENV_URL/clients/api/v1/enabled_perks/3de61f43-7ff3-445b-9f4f-f1e2982d37e7?app_id=APP_ID" \
  -X GET \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Token token=ACCESS_TOKEN"
```
> The above command returns JSON structured like this:

```json
{
  "enabled_perk": {
    "id": "3de61f43-7ff3-445b-9f4f-f1e2982d37e7",
    "brand": "Amazon",
    "title": "5.0% off orders at Amazon",
    "discount": 5.0,
    "custom": false,
    "created_at": "2018-11-15T16:10:24.499Z"
  }
}
```

This endpoint returns an enabled perk object.


Parameter | Description
--------- | -----------
ACCESS_TOKEN | Your application's active access token [required]
id | The id of the enabled perk to retrieve
app_id | Your application's app id [required]
