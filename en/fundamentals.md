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

### [Check out what the API can do](/actions.html)

## How Socialcube works

Socialcube is designed for grading with Christian Haschek's [XP based grading system](https://blog.haschek.at/xp-based-grading-system).

![Socialcube explanation](https://www.pictshare.net/9f69c35ef2.png)

### Institutions
On the site **institutions** (schools, universities, etc.) can be reigstered and teachers and students can join on a email- or code based invite system.

### Courses
Every Teacher in an institution can create **courses**. These courses represent classes

### Sections
Every course can have multiple **sections**. Sections are usually the topics the teacher is teaching in this class.

In these sections **XP** can be given to all students attending this course.

### Example
A professor of MIT (**Institution**) teaches "Advanced computer science" (**Course**) and divides the course in the topics "cryptography", "bash scripting" and "game theory" (**Sections**).

They give out an assignment in cryptography that will be graded in XP. Students who hand in the assignment receive a value of XP determined by the professor in the section cryptography.

## The goal

The goal of this API is to create an interface between the students performance and external sites. If you are a game developer you can reward your students in your game when they get XP in school/university.