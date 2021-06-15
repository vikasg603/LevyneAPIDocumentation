# FetchByProductID

Used to fetch product by its ID.

**URL** : `/v1/Brand/Products/FetchByProductID`

**Method** : ` GET`

**Auth required** : YES

**Query constraints**

```json
{
    "ProductID": "[valid productID]",
    "isArchiveProduct": "[boolean 0|1]"
}
```

**Query example**

```json
{
    "ProductID": "4",
    "isArchiveProduct": "0"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "ProductID": 4,
    "UniqueProductID": "Hugh-Hugh-huh-1",
    "BrandID": 2,
    "Price": 900,
    "isPublic": 1,
    "createdAt": "2021-05-25T18:22:38.000Z",
    "updatedAt": "2021-05-25T18:22:38.000Z",
    "deletedAt": null,
    "ProductCustomized": {
        "Title": "Hugh Hugh huh",
        "PrimaryImage": "https://d12eccyy0fqhx.cloudfront.net/eyJidWNrZXQiOiJsZXZ5bmVwcm9kdWN0cy10ZXN0Iiwia2V5IjoiMjAyMS0wNS0yNVQxNjIxOTY2OTQzOTk4NTg5Mjc0MTIzMS5qcGciLCJlZGl0cyI6eyJyZXNpemUiOnsid2lkdGgiOjUwMH19fQ==",
        "MarketPrice": 1000,
        "ShortDescription": "Huh uyvuh jhjh jvhjh huh j",
        "ProductID": 4,
        "SubCategory": {
            "Name": "Shirt",
            "ID": 1
        },
        "MainCategory": {
            "Name": "Fashion",
            "ID": 1
        },
        "ProductCustomizedProperties": {
            "ApproxManufacturingDays": "10",
            "ProductDescription": "Jbhjh jhj hi hvhhvyu Yusuf tryst net stock ytjydtnhdjy",
            "WashType": "1",
            "Styles": [
                "3",
                "4",
                "7"
            ],
            "Fabrics": [
                "3",
                "5",
                "7"
            ],
            "ProductImage": [
                "https://picsum.photos/1200/900",
                "https://picsum.photos/1200/900",
                "https://picsum.photos/1200/900",
                "https://picsum.photos/1200/900"
            ]
        }
    },
    "ProductSKUs": [
        {
            "Title": "C",
            "SKU": "B00000001P0000004",
            "StockAvailable": 1000,
            "StockSoldOffline": 0,
            "StockSoldOnline": 0
        }
    ]
}
```

## Error Response

**Condition** : If 'ProductID' is not in database .

**Code** : `404 NOT FOUND`

**Content** :

```json
{
    "status": "Failed",
    "description": "Product Not Found"
}
```

*Or*

**Condition** : If 'isArchiveProduct' is not boolean.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"isArchiveProduct\" must be one of [1, 0]"
}
```
