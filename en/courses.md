# Courses and sections

## Get courses of user

The ```get_courses``` URL will return an array with the IDs of the courses.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/courses/get_courses |
| Answer | {"STATUS":"OK","ANSWER":["10"]} |

## Get sections of course

This API call will return an array of all sections of the specified course. This includes the ID, name and maximum XP of this section.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/courses/get_sections_of_course/-course ID- |
| Answer | {"STATUS":"OK","ANSWER":[{"ID":"453","name":"Test","points":"122","course":"10"},{"ID":"454","name":"test2","points":"100","course":"10"}]} |
