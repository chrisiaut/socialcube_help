# User info
## Get type of user
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

## Get email of user

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/user/get_email |
| Answer | {"STATUS":"OK","ANSWER":"users@mail.addr"} |