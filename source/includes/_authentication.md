# Authentication

As a client organisation that has requested access to this API, you will have received an APP_ID and SECRET.

1) Use these credentials on the access_tokens#create endpoint to create an access token. Store this token as it is used to authenticate future requests. It is recommended to store the corresponding refresh token as well.

2) Your access token will expire 24 hours after creation. When the token expires, use the access_token#update endpoint to revive the same access token for another 24 hours.

You can create a new access token instead, though this is not advised. Creating a new access token will invalidate any other active access tokens belonging to your application.

# Security

In addition to the aforementioned SECRET tokens and access token authentication, the Portify Client API will reject any requests from IP addresses that you have not whitelisted. Please contact the Portify development team to manage your whitelisted IPs.

This feature can be disabled on request for the staging environment.