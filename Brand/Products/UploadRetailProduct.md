# `UploadRetailProduct`

Used to upload a retail product from user

**URL** : /`v1/Brand/Products/UploadRetailProduct`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
[{
    "Price": "[Price in number]",
    "Title": "[Title in plain text]",
    "ProductRetailDataID": "[ID in number]",
    "ProductSKU": [{
        "SKU": "[SKU string]",
        "Title": "[Title String]",
        "StockAvailable": "[Stocks in number]"
    }]
}]
```

**Data example**

```json
[{
    "Price": 100,
    "Title": "New Products",
    "ProductRetailDataID": 2,
    "ProductSKU":[
{
        "SKU": "UGG-BB-PUR-06",
        "Title": "New",
        "StockAvailable": 5
}

    ] 

}]
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "ProductIDs": [
        27681
    ]
}
```

## Error Response

**Condition** : If any of the fields are missing.

**Code** : `400 BAD REQUEST`

**Content Example** :

```json
{
    "status": "Failed",
    "description": "\"[0].ProductRetailDataID\" is required"
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
