# Login

Used to book an Appointment

**URL** : ` `/v1/Brand/Appointment/BookAppointment ` `

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
    "UserID": "Number  (optional)",
    "Title": "plain text",
    "Summary" : "plain text (optional)",
    "StartTime" : "valid date and time & Format : yyyy-mm-dd hh:mm:ss",
    "Duration" : "Number"
}
```

**Data example**

```json
{
    "Title" : "Testing",
    "StartTime" : "2021-06-15 19:45:00",
    "Duration" : 35,
    "Summary" : "Personal meet"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

Returns an ID of the inserted record

```json
[
    37,
    1
]
```

## Error Response

**Condition** : if we miss out 'Duration'

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "Please enter the duration time"
}
```


**Condition** : if we miss out 'Title'

**Code** : `400 BAD REQUEST`

**Content** : 

```json
{
    "status": "Failed",
    "description": "title is missing"
}
```


**Condition** : if we put StartTime - "2021-06-12 19:45:00"

**Code** : `400 BAD REQUEST`

**Content** : 

```json
{
    "status": "Failed",
    "description": "Please Select a proper Date"
}
```
