# RefreshToken

Used to Refresh Token.

**URL** : `/v1/Brand/Auth/RefreshToken`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
	"RefreshToken": "[string of length 64 (from VerifyOTP route)]",
	"UID": "[random string of length 16]"
}
```

**Data example**

```json
{
	"RefreshToken": "201ec060c809e217eabc63b793913ce9e49df6e044524323db5bf0041fdf4cb9",
	"UID": "1234567891234567"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
	"status": "Success",
	"Tokens": {
		"Token": "8rLJ+wYHmBgMXbqGZE9rQwx9pA10EQ1wEgoYxyh0SuILSTDB3RUwRBFoTSRMtFAAn3clQK5QalWRd1H1UGJwt6DRn4se8kgqabM9E1gHu6hYCBkrdkq58g8+ZYWEvu3JMKYviXDI2WynWm4Nu90+qxbraO4OTBuq/Qnx3BxqqeawFwUAXTSPP0eSFrXFBFJDBvtORQdjGuZ7zO+9aUgCu9djnGErD31SFcQKXXDcfRdvVH7GmoIKeC94HcwDqvV3GO+Dl8IKYN+/p0UCe4o2wObu8OJFbvZomQnYoYFKIRMr9oEH1MLxHE/qiVpbJHODLYllPQ5pNEtVk28GerFc9A==",
		"RefreshToken": "66d3c35655e523b1b4a48bf5611f4fe8ea26db7d6230d7f39d1983a6b07d8355"
	}
}
```

## Error Response

**Condition** : If 'RefreshToken' is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "Not a valid Refresh Token!"
}
```

**Condition** : If 'UID' is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "\"UID\" does not match any of the allowed types"
}
```

**Condition** : If 'authorization' is not provided.

**Code** : `401 Unauthorized`

**Content** :

```json
{
	"status": "Failed",
	"description": "Authorization header not found"
}
```
