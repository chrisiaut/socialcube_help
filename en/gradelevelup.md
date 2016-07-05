# Event: grade_levelup

The "grade_levelup" event will be triggered whenever a student upgrades their grade by getting XP. This will always be triggered immediately after a got_xp event (if the student got enough XP to level up their grade)

## Webhook data

The data your webhook will receive looks like this

```json
{
  "event": "grade_levelup",
  "secret": "secret_of_your_app_for_validation",
  "user": 
  {
    "id": "5abc23af", //alphanumeric string. should be used to identify user since email can be changed
    "xp_percent": 50, //amount of max XP in percent the student has in this course
    "course": 48, //ID of course (class) where user got the XP from
    "institution": 5 //ID of the institution where the course is in
  }
}
```

## Response
Your webhook has to output "200" as string if everything was in order.

### Retries
If the Socialcube server doesn't receive a "200" it will automatically retry the webhook call 5 times with 10 minutes in between. This ensures that you don't miss any data when your server goes down for a short time.

### Timeout
If your server doesn't answer for 10 seconds the connection is handled as failed and retry will be scheduled