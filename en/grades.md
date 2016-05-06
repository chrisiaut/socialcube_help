# Grades

For privacy reasons you can only get the grades in form of percentages of whole courses. You won't see the exact grade for every section but the percentage of the course should be sufficient for most applications.

## Get grades of student

The ```get_grades``` URL will return a percent value (0-100+) and requires you to specify a course ID. You can obtain a course ID by [requesting all courses of a user](/courses.html).

If the value is **greater than 100** that means the student earned more XP than the maximum set by the teacher. This usually happens with highly motivated students who do more than the teacher asked for and the teacher is nice enough to give the student XP for his bonus work.

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/grades/get_grades/-courseID- |
| Answer | {"STATUS":"OK","ANSWER":["10"]} |