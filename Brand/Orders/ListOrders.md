# ListOrders

Used to List the orders

**URL** : `/v1/Brand/Orders/ListOrders`

**Method** : `GET`

**Auth required** : YES

**URL constraints**

```json
http://localhost:8080/v1/Brand/Orders/FetchBucketItems/?BucketID = [integer]
```

**Data example**

```json
http://localhost:8080/v1/Brand/Orders/FetchBucketItems/?BucketID=1
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
[]
```

## Error Response


**Condition** : If 'BucketID' is not provided.

**Code** : `400 Bad Request`

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
