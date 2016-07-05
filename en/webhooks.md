# Webhooks

## What data will I receive?
You will receive a **POST** request to the webhook you specified which will contain one POST field: "data"

The "data" POST field is a JSON object which will include the event name and data


## Events
Currently there are three events that you can receive: login, got_xp and grade_levelup

### login
The "login" event will be sent to your webhook **only the first time** when a user linked their account to your app.