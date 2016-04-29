# Fundamentals
GradeLink is a REST API. The base URL for your requests is ```https://socialcube.net/api```

The first parameter will be an action or sequence and the latter ones are parameters.

**!!! Every request has to include the following POST variables !!!**
- api_key (the key of your app)
- user_token (the token of the user)

All unix timestamps you send to the API are assumed to be in GMT+0

The API key has to be requested by every developer and app. The user token will be provided if the user logged in and accepted your app.

### ```https://socialcube.net/api/<ACTION>/<PARAMETERS>```