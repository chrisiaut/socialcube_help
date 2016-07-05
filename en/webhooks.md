# Webhooks

## What kind of data will I receive?
You will receive a **POST** request to the webhook you specified which will contain one POST field: "data"

The "data" POST field is a JSON object which will include the event name and data


## Events
Currently there are three events that you can receive:
* [login](/login.html)
* [got_xp](/gotxp.html)
* [grade_levelup](/gradelevelup.html)