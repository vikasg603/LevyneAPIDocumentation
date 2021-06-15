# Logout

Used to Logout.

**URL** : `/v1/Brand/Auth/Logout`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
	"DeviceID": "[random string of length 16]"
}
```

**Data example**

```json
{
	"DeviceID": "1234567891234567"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
	"status": "Success"
}
```

## Error Response

**Condition** : If 'authorization' is not provided.

**Code** : `401 Unauthorized`

**Content** :

```json
{
	"status": "Failed",
	"description": "Authorization header not found"
}
```
