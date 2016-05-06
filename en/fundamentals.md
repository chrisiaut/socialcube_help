# Fundamentals

## About the API
GradeLink is a REST API. The base URL for your requests is:

### ```https://socialcube.net/api/<ACTION>/<PARAMETERS>```

The first parameter will be an action or sequence and the latter ones are parameters.

**!!! Every request has to include the following variables (POST or GET) !!!**
- api_key (the key of your app)
- user_token (the token of the user)

All unix timestamps you send to the API are assumed to be in GMT+0

The API key has to be requested by every developer and app. The user token will be provided if the user logged in and accepted your app.

[Check out what the API can do](/actions.html)

## How Socialcube works

Socialcube is a platform where institutions (schools, universities, etc.) can be registered. Every Teacher in an institution can create courses

## The goal

The goal of this API is to create an interface between the students performance and external sites. If you are a game developer you can reward your students in your game when they get XP in school.