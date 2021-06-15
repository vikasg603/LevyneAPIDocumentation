# FetchChatBuckets

Used to Fetch Chat Buckets.

**URL** : `/v1/Brand/Chat/FetchChatBuckets`

**Method** : `GET`

**Auth required** : YES

**URL constraints**

```json
/v1/Brand/Chat/FetchChatBuckets/?Page=1
Page is optional number with default value 1

```

## Success Response

**Code** : `200 OK`

**Content example**

```json
[
	{
		"BucketID": 1,
		"UserID": 1,
		"OrderID": null,
		"isUnread": 0,
		"User": {
			"UserID": 1,
			"Mobile": 7021982047,
			"UserProfile": {
				"Name": "vikas"
			}
		},
		"BucketMessages": [
			{
				"Text": null,
				"Type": 4,
				"updatedAt": "2021-05-26T16:04:05.000Z"
			}
		]
	}
]
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
