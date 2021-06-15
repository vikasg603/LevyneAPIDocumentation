# AddCoupon

Used to Add Coupon.

**URL** : `/v1/Brand/Coupon/AddCoupon`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
        CouponCode: Required Uppercase string of length between 5 to 15 characters,

        isPublic: Boolean value, 0 or 1 (0 by default),

        IsMultiUser: Boolean value, 0 or 1 (1 by default),

        UsesLimitPerUser: Integer number (1 by default),

        MinimumOrderAmount: Integer number (null by default),

        PercentageDiscount: Integer number (range 1 to 100),

        MaxDiscount: Integer number, minimum value 1 (null by default),

        ValidTill: Date (null by default),

        ValidFrom: Date, default value is new date,

    }
```

**Data example**

```json
{
	"CouponCode": "ABCDEFGH",
	"isPublic": 1,
	"IsMultiUser": 1,
	"UsesLimitPerUser": 5,
	"MinimumOrderAmount": 0,
	"PercentageDiscount": 10,
	"MaxDiscount": 10,
	"ValidTill": "2021-06-05 04:56:46",
	"ValidFrom": "2021-06-05 04:56:46"
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

**Condition** : If 'ValidTill' Date is wrong

**Code** : `500 Internal Server Error`

**Content** :

```json
{
	"status": "Failed",
	"description": "Internal Server Error"
}
```

**Condition** : If 'MaxDiscount', 'PercentageDiscount', is missing

**Code** : `404 Not Found `

**Content** :

```json
{
	"status": "Failed",
	"description": "Error while inserting Coupon"
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
