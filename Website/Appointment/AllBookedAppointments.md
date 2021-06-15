# Login

Used to list all the Booked Appointments

**URL** : `/v1/Website/Appointment//AllBookedAppointments/:StartDate/:EndDate`

**Method** : GET

**Auth required** : NO

**Params :** 

```json
    StartDate: "valid date and format : yyyy-mm-dd",
    EndDate: "valid date and format : yyyy-mm-dd",
```

## Success Response

**Code** : `200 OK`

**Content example** 

StartDate : 2021-06-15 , EndDate : 2021-06-16

```json
[
    {
        "StartTime": "2021-06-15T10:45:00.000Z",
        "EndTime": "2021-06-15T11:30:00.000Z"
    },
    {
        "StartTime": "2021-06-15T19:45:00.000Z",
        "EndTime": "2021-06-15T20:20:00.000Z"
    }
]
```

## Error Response

**Condition** : if you insert wrong StartDate

**Code** : `400 BAD REQUEST`

**Content** : 

```json

{
    "status": "Failed",
    "description": "Please select a proper date"
}
```


**Condition** : if you insert wrong EndDate

**Code** : `400 BAD REQUEST`

**Content** : 

```json
{
    "status": "Failed",
    "description": "Sorry, incorrect end date"
}

```
