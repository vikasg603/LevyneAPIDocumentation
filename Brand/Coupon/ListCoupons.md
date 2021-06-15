# ListCoupons

Used to List Coupons.

**URL** : `/v1/Brand/Coupon/ListCoupons`

**Method** : `GET`

**Auth required** : YES

**Query constraints**

```json
Page can be passed in query.
Default value is 1 for page
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
	"CouponID": 2,
	"CouponCode": "qui",
	"BrandID": 1,
	"isPublic": 1,
	"isActive": 1,
	"IsMultiUser": 1,
	"UsesLimitPerUser": 1,
	"Message": "fuga molestiae accusantium",
	"MinimumOrderAmount": 0,
	"PercentageDiscount": 0,
	"MaxDiscount": 10,
	"AssignedUserID": null,
	"ValidTill": "2021-06-04T15:39:08.000Z",
	"ValidFrom": "2021-06-04T15:39:08.000Z",
	"createdAt": "2021-06-04T15:39:08.000Z",
	"updatedAt": "2021-06-11T05:26:27.000Z"
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
