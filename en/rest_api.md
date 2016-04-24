# GradeLink API
Motto: ~~Pay2Win~~ Learn2WIn

This document will be describing how to use the GradeLink API. It's meant for developers who want to reward students for their achievements in school.

## Fundamentals
GradeLink is a REST API. The base URL for your requests is ```https://socialcube.net/api```

The first parameter will be an action or sequence and the latter ones are parameters.

Every request has to include the following POST variables:
- api_key
- user_token

The API key has to be requested by every developer and app. The user token will be provided if the user logged in and accepted your app.

### ```https://socialcube.net/api/<ACTION>/<PARAMETERS>```

## Actions

### Courses

#### Get courses of user
For privacy reasons you won't see the name of the course as entered by the teacher, just a distinct GUID.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/courses/get |
| Answer |  {} |


### Logout
