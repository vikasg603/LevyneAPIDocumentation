# SendOTP

Used to Send OTP.

**URL** : `/v1/Brand/Auth/SendOTP`

**Method** : `POST`

**Auth required** : NO

**Data constraints **

```json
{
	"Mobile": "[10 digit number]",
	"Hash": "[14 character string]"
}
```

**Data example**

```json
{
	"Mobile": 7021982047,
	"Hash": "771115c8465ce2"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
	"status": "Success",
	"OTP": "296855",
	"OTPToken": "6217d69b1ed362a4abb460c99a0ccece52fb28ed7a16749a4e362c03fe108e64"
}
```

## Error Response

**Condition** : If 'Mobile' is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "Not a valid Mobile!"
}
```

**Condition** : If 'Hash' is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "Not a valid Hash!"
}
```
