# Edit Address

Used to Edit Address .

**URL** : `/v1/Website/Profile/EditAddress`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "Address" : "[string]",
    "PicCode" : "[number]",
    "Name"    : "[string]",
    "AddressID": "[number]"
}
```

**Data example**

```json
{
    "Address":"74978 Thompson Camp,Romaguera Roads",
    "PinCode":"123456",
    "Name": "prachi",
    "AddressID":7
}
```

## Success Response

**Code** : `200 OK`

**Output Constraints**

```json
{
    "status": "Success"
}
```

**Output example**

```json
{
    "status": "Success"
}
```

## Error Response

**Condition** : If 'AddressID' is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"AddressID\" is required"
}

```
**Condition** : If 'Name' is not provided.

**Code** : `400 Bad Request`

**Content** :

```json

{
    "status": "Failed",
    "description": "\"Name\" is required"
}
```
**Condition** : If 'Address' is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"Address\" is required"
}

```

