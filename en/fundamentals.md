# Fundamentals

## Setting up an developer account
The first thing you need to do if you didn't already do it is to create an account as a developer on Socialcube.

You can do it here: https://www.socialcube.net/developers

After verification you can create an unlimited amount of apps and each one will give you a secret and a key.

## About the API
The Socialcube GradeLink API can be used in two ways. Via Webhooks and via a REST API.

The Webhook method is the preferred method although you can get more details with the REST API.

### [Webhooks](/webhooks.html) (easy start)

#### What is a webhook?
To put it simple: A webhook is a web-accessible script that you own and host, which will receive data from the Socialcube server whenever an event happens like "user got XP".

So let's say you own the domain ```http://socialcube.testapp.app``` and a user links their Socialcube account with your app.

The user receives XP in their class so the Socialcube server sends a POST request to the webhook you defined (eg ```http://socialcube.testapp.app/webhook.php```) which contains the info which student got how many XP.

### [REST API](/actions.html)
GradeLink is a REST API. The base URL for your requests is:

### ```https://socialcube.net/api/<ACTION>/<PARAMETERS>```

The first parameter will be an action or sequence and the latter ones are parameters.

**!!! Every request has to include the following variables (POST or GET) !!!**
- api_key (the key of your app)
- user_token (the token of the user. Obtained by the [login webhook event](/login.html))

All unix timestamps you send to the API are assumed to be in GMT+0

The API key has to be requested by every developer and app. The user token will be provided if the user logged in and accepted your app.

### [Check out what the API can do](/actions.html)

