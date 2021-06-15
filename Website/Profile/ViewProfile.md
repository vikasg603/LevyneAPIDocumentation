# View Profile

Used to View Profile.

**URL** : `/v1/Website/Profile/ViewProfile`

**Method** : `GET`

**Auth required** : NO

**Data constraints**

```json
{
    "UserID": "[number]",
}
```

**Data example**

```json
{
 "UserID" = 1
}
```

## Success Response

**Code** : `200 OK`

**Output Constraints**

```json
{
    "UserID": number,
    "Status": number,
    "Mobile": number,
    "createdAt": "DateTime",
    "updatedAt": "DateTime",
    "UserProfile": {
        "Name": "string",
        "Email": "string",
        "Gender": 0 | 1
    },
    "UserAddresses": [
        {
            "Name": "string",
            "Address": "string",
            "PinCode": number,
            "ID": number
        },
    ]
}
```

**Output example**

```json
{
    "UserID": 1,
    "Status": 1,
    "Mobile": 7021982047,
    "createdAt": "2021-05-26T16:01:02.000Z",
    "updatedAt": "2021-05-26T16:01:02.000Z",
    "UserProfile": {
        "Name": "vikas",
        "Email": "vikas.rg@somaiya.edu",
        "Gender": 1
    },
    "UserAddresses": [
        {
            "Name": "Obie",
            "Address": "284 Romaguera Roads",
            "PinCode": 90119,
            "ID": 7
        },
        {
            "Name": "Bernard",
            "Address": "4193 Fay Ports",
            "PinCode": 69360,
            "ID": 9
        },
        {
            "Name": "Raymundo",
            "Address": "87185 Krista Gardens",
            "PinCode": 34302,
            "ID": 10
        },
        {
            "Name": "Krystel",
            "Address": "5965 Stroman Motorway",
            "PinCode": 39281,
            "ID": 16
        },
        {
            "Name": "Vesta",
            "Address": "17498 Emmerich Crest",
            "PinCode": 38901,
            "ID": 18
        }
    ]
}
```

## Error Response

**Condition** : If 'UserID' is not a number.

**Code** : `503 Service Unavailable`

**Content** :

```json
{
    "status": "Failed",
    "description": "Something went wrong"
}
```
