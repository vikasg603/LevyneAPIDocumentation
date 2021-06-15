# VerifyOTP

Used to verify the OTP.

**URL** : `/v1/Website/Auth/VerifyOTP`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "Mobile": "[valid Mobile Number]",
    "OTP": "[valid OTP]"
}
```

**Data example**

```json
{
    "Mobile": "9987877001",
    "OTP": "626632"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "UserID": 20,
    "Mobile": 9987877001,
    "UserProfile.Name": null,
    "UserProfile.Email": null,
    "UserProfile.Gender": null
}
```

## Error Response

**Condition** : If 'Mobile' and 'OTP' combination is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "Not a valid OTP!"
}
or
{
    "status": "Failed",
    "description": "Not a valid Mobile!"
}
```
