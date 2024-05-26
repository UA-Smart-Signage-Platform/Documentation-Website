#### Messages Sent by the Media Player

```json
Register Message (sent once to register the monitor)

topic: "register"
payload: 
{
    "method":"REGISTER",
    "name":"",   // name defined when configuring the monitor
    "width":"",  // screen width
    "height":"", // screen height
    "uuid":""    // unique identifier of the monitor
}
```

```json
Keep-Alive Message (sent periodically to tell the backend it's still alive)

topic: "keepalive"
payload: 
{
    "method":"KEEP_ALIVE",
    "uuid":""  // unique identifier of the monitor
}
```

#### Messages Sent by the Server

```json
Confirm Register Message (sent as a response to the register message)

topic: uuid // sent in a topic with the monitor's uuid
payload: 
{
    "method":"CONFIRM_REGISTER"
}
```
```json
Rules Message (sent when the rules applied to a group are changed)

topic: "uuid" // uuid of the monitor we want so send the message to
{
  "method": "RULES",
  "rules": [  // list with all the rules applied to the group
    {
      "html": "",        // html of the template to be displayed
      "files": [],       // list with download links to all the media
      "schedule": {      
        "startTime": "", // time of the day to start. formated as "12:00"
        "endTime": "",   // time of the day to end. formated as "12:00"
        "weekdays": [],  // days of the week to display the rule 0-Monday 6-Sunday
        "startDate": "", // rule applies from this date on out. formatted as "2024-05-11"
        "endDate": "",   // rule applies up to this date. formatted as "2024-05-11"
        "priority": 0    // used to decide what template plays when overlap happens. smaller number means higher priority.
      }
    }
  ]
}
```