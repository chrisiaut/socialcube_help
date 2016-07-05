# Event: login

The "login" event will be sent to your webhook **only the first time** when a user linked their account to your app/game/website.

## Webhook data

The data your webhook will receive looks like this

```json
{
  "event": "login",
  "secret": "secret_of_your_app_for_validation",
  "user": 
  {
    "id": "5abc23af", //alphanumeric string. should be used to identify user since email can be changed
    "email": "user@usersemailprovider.usr",
    "user_token":"abcdefghijklmnopqrstuvwxyz", //save this token! You need this to make REST API requests
    "lang": "en", //language
    "timezone": 2, //timezone offset from GMT
    "usertype": 3, //0->admin,1->institution admin,2->teacher,3->student
    "inst_courses": { "1":[42,48],"5":[23] } //list of institution IDs and which courses in these institutions the user is a member of
  }
}
```

## Response
Your webhook should respond with a **URL** the user will be redirected to. This is usually some success page of your app or a page. You can add GET variables to it if you want to.

### Example response by your webhook
```
http://your_app.yourdomain.dom/login/gradelink
```

### Retries
If the Socialcube server doesn't receive a valid URL it will automatically retry the webhook call 5 times with 10 minutes in between. This allows you not to miss any data when your server went down for a short time.

### Timeout
If your server doesn't answer for 10 seconds the connection is handled as failed and retry will be scheduled