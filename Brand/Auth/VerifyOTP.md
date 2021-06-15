# VerifyOTP

Used to Verify OTP.

**URL** : `/v1/Brand/Auth/VerifyOTP`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
	"Mobile": "[10 digit number]",
	"OTP": "[String of length 6 (from SendOTP route)]",
	"OTPTokenHash": "[String of length 64 (from SendOTP route)]",
	"UID": "[random string of length 16]",
	"FirebaseToken": "[empty string]"
}
```

```

```

**Data example**

```json
{
	"Mobile": 7021982047,
	"OTP": "296855",
	"OTPTokenHash": "6217d69b1ed362a4abb460c99a0ccece52fb28ed7a16749a4e362c03fe108e64",
	"UID": "1234567891234567",
	"FirebaseToken": ""
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
	"status": "Success",
	"Tokens": {
		"Token": "GBqEwLfo3Xr+ph+/FlebVGDrUDC7/oVkqTivvs7u3+j/y/Ml73N8KfiP8GMe5uSoib/5DcHwgaZbwV3zqbydddxoSjChd2bUbkjOAMccaEUko9SgfOhFsY/hH5J+GVWZ5GL5OAhaTxO4Phn2DUPPnwuZfGAIppzLEtu+tNMEjOeT4DKMu4DOW/iccjeQwHv+IXvmbUOct6D6FHaNKNalxj1zxH/CfhhJya/VP7/EvB1DuJiHob/BabCZ/8NW12Z0qI2fvE3ZtrHSS+ra6AkeTqcDvLoWn+RRx5/oe7c7EySonZjSqkRJd4rClAo9uaJ5l2Q1dBAMGN8UUZMcWjrzdg==",
		"RefreshToken": "201ec060c809e217eabc63b793913ce9e49df6e044524323db5bf0041fdf4cb9"
	},
	"BrandProfileInfo": {
		"Status": 1,
		"BrandID": 1,
		"BrandProfile": {
			"Gender": 1,
			"Name": "vikas",
			"Email": "vikas.rg@somaiya.edu",
			"ProfileImage": "https://www.directive.com/images/easyblog_shared/July_2018/7-4-18/b2ap3_large_totw_network_profile_400.jpg",
			"About": "Levyne Vikas"
		},
		"BrandAddress": {
			"Address": "Virar",
			"PinCode": 401303,
			"Latitude": 26.44992256,
			"Longitude": 80.33187103
		},
		"Industry": {
			"Name": "FashionDesign",
			"IndustryID": 1
		},
		"BrandStoreTimings": [
			{
				"ID": 1,
				"Day": null,
				"StartTiming": "240",
				"CloseTiming": "1021"
			},
			{
				"ID": 2,
				"Day": null,
				"StartTiming": "202",
				"CloseTiming": "769"
			},
			{
				"ID": 3,
				"Day": null,
				"StartTiming": "292",
				"CloseTiming": "1199"
			},
			{
				"ID": 4,
				"Day": null,
				"StartTiming": "148",
				"CloseTiming": "1056"
			},
			{
				"ID": 5,
				"Day": null,
				"StartTiming": "403",
				"CloseTiming": "419"
			}
		],
		"BrandWebsites": [
			{
				"URL": "apitesting603.levyne.com"
			}
		]
	}
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

**Condition** : If 'OTP' is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "Not a valid OTP!"
}
```

**Condition** : If 'OTPTokenHash' is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "Not a valid OTP Token Hash!"
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

**Condition** : If 'FirebaseToken' is wrong.

**Code** : `401 Unauthorized`

**Content** :

```json
{
	"status": "Failed",
	"description": "OTP Verification Failed"
}
```
