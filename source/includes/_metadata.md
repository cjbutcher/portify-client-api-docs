# Metadata

Every (non-authentication related) request to the Portify Client API contains a metadata object. This object is designed to assist with pagination. The API will return up to 50 records per request.

Parameter | Description
--------- | -----------
total_record_count | The number of records that would be returned in the response, were there no pagination
record_count | The number of records returned in this request
continuation_token | The token you should use on the next request to receive the next page of results

When scraping data, the continuation_token should be retrieved from your previous request, and passed as a query string parameter on your following request. It is a UNIX timestamp that repesents the datetime from which the next page of records were created after. If no continuation_token is passed, records will be returned from the beginning of the given date.
