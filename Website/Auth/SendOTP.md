# SendOTP

Used to send OTP for a valid mobile number.

**URL** : `/v1/Website/Auth/SendOTP`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "Mobile": "[valid phone number]",
}
```

**Data example**

```json
{
    "Mobile": "9987877001"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "OTP": "626632"
}
```

## Error Response

**Condition** : If 'Mobile' is invalid.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "Not a valid Mobile Number!"
}
```
