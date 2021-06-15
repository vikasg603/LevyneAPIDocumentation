# UpdateCouponStatus

Used to Update Coupon Status.

**URL** : `/v1/Brand/Coupon/UpdateCouponStatus`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
    "CouponID": Positive integer number,
    "isActive": Required value- 0 or 1
}
```

**Data example**

```json
{
	"CouponID": 2,
	"isActive": 1
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

**Condition** : If 'CouponID' is not present.

**Code** : `400 Bad Request`

**Content** :

```json
{
	"status": "Failed",
	"description": "\"CouponID\" is required"
}
```

**Condition** : If 'isActive' is not present.

**Code** : `500 Internal Server Error`

**Content** :

```json
{
	"status": "Failed",
	"description": "Internal Server Error"
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
