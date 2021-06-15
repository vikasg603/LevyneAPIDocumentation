# FetchBucketMessages

Used to Fetch Bucket Messages.

**URL** : `/v1/Brand/Chat/FetchBucketMessages`

**Method** : `GET`

**Auth required** : YES

**URL constraints**

```json
/v1/Brand/Chat/FetchBucketMessages/?BucketID=1&Page=1

Page is optional number with default value 1
BucketID is required positive number

```

## Success Response

**Code** : `200 OK`

**Content example**

```json
[
	{
		"ID": 1,
		"BucketID": 1,
		"Type": 3,
		"isSentByCustomer": 1,
		"Text": null,
		"ImageURL": null,
		"createdAt": "2021-05-26T16:02:58.000Z",
		"updatedAt": "2021-05-26T16:02:58.000Z"
	},
	{
		"ID": 2,
		"BucketID": 1,
		"Type": 4,
		"isSentByCustomer": 1,
		"Text": null,
		"ImageURL": null,
		"createdAt": "2021-05-26T16:02:59.000Z",
		"updatedAt": "2021-05-26T16:04:05.000Z"
	},
	{
		"ID": 3,
		"BucketID": 1,
		"Type": 4,
		"isSentByCustomer": 1,
		"Text": null,
		"ImageURL": null,
		"createdAt": "2021-05-26T16:02:59.000Z",
		"updatedAt": "2021-05-26T16:04:05.000Z"
	}
]
```

## Error Response

**Condition** : If 'BucketID' is not provided.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "\"BucketID\" is required"
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
