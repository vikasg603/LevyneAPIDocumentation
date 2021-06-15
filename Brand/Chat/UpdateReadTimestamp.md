# UpdateReadTimestamp

Used to Update Read Timestamp

**URL** : `/v1/Brand/Chat/UpdateReadTimestamp`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
	"BucketID": ["Positive integer required"]
}
```

**Data example**

```json
{
	"BucketID": 1
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

**Condition** : If 'BucketID' is not provided.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
	"status": "Failed",
	"description": "\"BucketID\" is required"
}
```
