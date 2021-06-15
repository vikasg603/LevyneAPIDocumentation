# AddToWishList

Used to add product to wishlist.

**URL** : `/v1/Website/Products/AddToWishList`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
    "ProductID": "[valid ProductID]"
}
```

**Data example**

```json
{
    "ProductID":4
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

**Condition** : If 'ProductID' is invalid.

**Code** : `503 Service Unavailable`

**Content** :

```json
{
    "status": "Failed",
    "description": "Something went wrong"
}
```
