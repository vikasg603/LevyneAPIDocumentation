# ArchiveTheProduct

Used to archive the product

**URL** : `/v1/Brand/Products/ArchiveTheProduct`

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

**Condition** : If ProductID assocaited with BrandID is not available in database

**Code** : `404 NOT FOUND`

**Content** :

```json
{
    "status": "Failed",
    "description": "Product Not Found"
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
