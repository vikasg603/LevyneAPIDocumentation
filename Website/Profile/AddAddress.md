# AddAddress

Used to Add Address of User.

**URL** : `/v1/Website/Profile/AddAddress`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
   "Name"    : "[string]",
   "Address" : "[string]",
   "PicCode" : "[number]"
}
```

**Data example**

```json
{
    "Name": "Abhi",
    "Address": "14 Ganpati Kunj",
    "PinCode": 123456
}
```

## Success Response

**Code** : `200 OK`

**Output Constraints**

```json
{
    "AddressID": number 
}
```

**Output example**

```json
{
    "AddressID": 21
}
```

## Error Response

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

**Condition** : If 'PinCode' is not provided (as UserAddress.PinCode cannot be null) .

**Code** : `500 Internal Server Error`

**Content** :

```json
{
    "status": "Failed",
    "description": "Internal Server Error"
}
```
