# Top Users By Amount

Used to fetch top users by amount of orders

**URL** : `/v1/Brand/Reports/TopUsersByAmount`

**Method** : `GET`

**Auth required** : YES

**Data constraints**

```json
{
    "current": "[boolean field]",
    "type": "[W/M/Y]"
}
```

**Data example (Fetches all top users from ongoing month)**

```json
{
    "current": "true",
    "type": "M"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Tue Jun 01 2021 - Mon Jun 14 2021",
    "TopUsers": [
        {
            "Name": "Ceasar",
            "Mobile": 4471200671,
            "TotalAmount": 843
        },
        {
            "Name": "Kade",
            "Mobile": 1975477987,
            "TotalAmount": 65
        },
        {
            "Name": "vikas",
            "Mobile": 7021982047,
            "TotalAmount": 46
        }
    ]
}
```

## Error Response

**Condition** : If 'current' or 'type' is not specified or Invalid type.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "[Missing/Invalid field will be specified here]"
}
```
