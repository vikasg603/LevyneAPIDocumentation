# Login

Used to list all the Booked Appointments

**URL** : `/v1/Brand/Appointment/AllBookedAppointments`

**Method** : GET

**Auth required** : YES

**Query constraints**

```json

    StartDate: "valid date and format : yyyy-mm-dd",
    EndDate: "valid date and format : yyyy-mm-dd",

```

```json

```

## Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "UserID": 1,
        "Title": "hello",
        "Summary": "",
        "BrandID": 1,
        "StartTime": "2021-06-14T11:45:00.000Z",
        "EndTime": "2021-06-14T12:30:00.000Z",
        "Duration": 45
    },
    {
        "UserID": 1,
        "Title": "urgent",
        "Summary": "",
        "BrandID": 1,
        "StartTime": "2021-06-15T10:45:00.000Z",
        "EndTime": "2021-06-15T11:30:00.000Z",
        "Duration": 45
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
