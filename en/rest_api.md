# GradeLink API
Motto: ~~Pay2Win~~ Learn2WIn

This document will be describing how to use the GradeLink API. It's meant for developers who want to reward students for their achievements in school.

## Fundamentals
GradeLink is a REST API. The base URL for your requests is ```https://socialcube.net/api```

The first parameter will be an action or sequence and the latter ones are parameters.

**!!! Every request has to include the following POST variables !!!**
- api_key (the key of your app)
- user_token (the token of the user)

The API key has to be requested by every developer and app. The user token will be provided if the user logged in and accepted your app.

### ```https://socialcube.net/api/<ACTION>/<PARAMETERS>```

## Actions

### User info
#### Get type of user
On Socialcube there are 4 types of users and their IDs:
- Admins
- Institution Admin
- Teachers
- Students

| User Type | ID |
| -- | -- |
| Socialcube Admin | 0 |
| Institution Admin | 1 |
| Teacher | 2 |
| Student | 3 |

The only one that needs explanation is the institution admin. This person is usually a teacher but also the one, who first requested access to Socialcube for their institution (school, university, etc..).

You can handle them as teachers but might also give them more permissions since they are sort of the school-admins.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/user/get_type |
| Answer: Admin | {"STATUS":"OK","ANSWER":"0"} |
| Answer: Student |  {"STATUS":"OK","ANSWER":"3"} |
| Answer: Teacher |  {"STATUS":"OK","ANSWER":"2"} |

#### Get email of user

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/user/get_email |
| Answer | {"STATUS":"OK","ANSWER":"users@mail.addr"} |


### XP

#### Get all XP of user

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp |
| Answer |  {"STATUS":"OK","ANSWER":"1271"} |

##### Get XP **since** a specific time (unix timestamp)

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp/since/1461790126 |
| Answer |  {"STATUS":"OK","ANSWER":"0"} |

##### Get XP **until** a specific time (unix timestamp)

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp/until/1461790126 |
| Answer |  {"STATUS":"OK","ANSWER":"1271"} |
