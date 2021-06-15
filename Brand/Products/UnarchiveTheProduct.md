# UnarchiveTheProduct

Used to unarchive the product

**URL** : `/v1/Brand/Products/UnarchiveTheProduct`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
    "ProductID": "[valid Product ID]"
}
```

**Data example**

```json
{
    "ProductID": 239
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

**Condition** : If ProductID is not archived

**Code** : `503 SERVICE UNAVAILABLE`

**Content** :

```json
{
    "status": "Failed",
    "description": "Something went wrong"
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
