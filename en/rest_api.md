# GradeLink API
Motto: ~~Pay2Win~~ Learn2Win

This document will be describing how to use the GradeLink API. It's meant for developers who want to reward students for their achievements in school.



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

### Courses and sections

##### Get courses of user

The ```get_courses``` URL will return an array with the IDs of the courses.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/courses/get_courses |
| Answer | {"STATUS":"OK","ANSWER":["10"]} |

##### Get sections of course

This API call will return an array of all sections of the specified course. This includes the ID, name and maximum XP of this section.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/courses/get_sections_of_course/-course ID- |
| Answer | {"STATUS":"OK","ANSWER":[{"ID":"453","name":"Test","points":"122","course":"10"},{"ID":"454","name":"test2","points":"100","course":"10"}]} |


#### Get XP of user in section

This is mostly like the "get all XP of user" requests but in addition you have to provide the ID of a section. Section IDs can be aquired with the get_course_sections and courses with get_courses

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp_in_section/-section ID- |
| Answer |  {"STATUS":"OK","ANSWER":"51"} |

##### Get XP **since** a specific time (unix timestamp)

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp_in_section/-section ID-/since/1461790126 |
| Answer |  {"STATUS":"OK","ANSWER":"0"} |

##### Get XP **until** a specific time (unix timestamp)

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp_in_section/-section ID-/until/1461790126 |
| Answer |  {"STATUS":"OK","ANSWER":"1271"} |

### Cubes

Cubes are a virtual currency on Socialcube. For every XP a user earns, 5 Cubes are created and given to this user. There are also a few small games on Socialcube that can be used to lose or earn cubes.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/cubes/get_cubes |
| Answer | {"STATUS":"OK","ANSWER":"1090"} |