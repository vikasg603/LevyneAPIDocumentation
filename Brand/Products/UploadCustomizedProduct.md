# UploadCustomizedProduct

Used to upload a customized product from user

**URL** : /`v1/Brand/Products/UploadCustomizedProduct`

**Method** : `POST`

**Auth required** : YES

**Data constraints**

```json
{
    "Price": [Price of product],
    "MainCategoryID": [Main Category ID] ,
    "SubCategoryID": [SubCategory ID] ,
    "Title": [Valid title],
    "MarketPrice": [Price in market] ,
    "ShortDescription": [Short description],
    "Properties": {
        "Colour": "Yellow",
        "Size": 4
    },
    "ProductSKU": {
        "SKU": "",
        "Title": "",
        "StockAvailable": 
    }
}
```

**Data example**

```json
{
    "Price": 100,
    "MainCategoryID": 1,
    "SubCategoryID": 1,
    "Title": "New Products",
    "PrimaryImage": "https://unsplash.com/photos/bwMhq_itmMU",
    "ProductImages": [
		"https://unsplash.com/photos/bwMhq_itmMU"
]
    "MarketPrice": 200,
    "ShortDescription": "This is a new product",
    "Properties": {
        "Colour": "Yellow",
        "Size": 4
    },
    "ProductSKU": {
        "SKU": "UGG-BB-PUR-06",
        "Title": "New Product",
        "StockAvailable": 5
    }
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "token": "93144b288eb1fdccbe46d6fc0f241a51766ecd3d"
}
```

## Error Response

**Condition** : If 'username' and 'password' combination is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "non_field_errors": [
        "Unable to login with provided credentials."
    ]
}
```
