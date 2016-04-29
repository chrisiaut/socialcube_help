# XP

## Get all XP of user

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_sum |
| Answer |  {"STATUS":"OK","ANSWER":"1271"} |

### Get detailed XP log

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_details |
| Answer |  {"STATUS":"OK","ANSWER":[{"ID":"1","section":"2","xp":"10","timestamp":"1418516185"},{"ID":"2","section":"3","xp":"400","timestamp":"1418516201"},{"ID":"3","section":"3","xp":"10","timestamp":"1418516208"},{"ID":"4","section":"3","xp":"10","timestamp":"1418516226"},{"ID":"21","section":"10","xp":"100","timestamp":"1418595369"},{"ID":"22","section":"10","xp":"100","timestamp":"1418595411"},{"ID":"23","section":"10","xp":"100","timestamp":"1418595469"},{"ID":"24","section":"10","xp":"100","timestamp":"1418595561"},{"ID":"25","section":"10","xp":"100","timestamp":"1418595603"},{"ID":"26","section":"10","xp":"100","timestamp":"1418595928"}]} |

### Get XP **since** a specific time (unix timestamp)

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp/since/1461790126 |
| Answer |  {"STATUS":"OK","ANSWER":"0"} |

### Get XP **until** a specific time (unix timestamp)

| Attribute | Value |
| -- | -- |
| URL | https://socialcube.net/api/xp/get_xp/until/1461790126 |
| Answer |  {"STATUS":"OK","ANSWER":"1271"} |