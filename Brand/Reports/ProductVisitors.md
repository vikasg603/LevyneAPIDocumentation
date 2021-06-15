# Product Visitors

Used to count _total_ _visitors_ of products on specific Brand wesbites or of particular Product.

**URL** : `/v1/Brand/Reports/ProductVisitors`

**Method** : `GET`

**Auth required** : YES

**Data constraints**

```json
{
    "From": "[valid start date]",
    "To": "[valid end date]",
    "ProductID": "[valid ProductID (optional) default is undefined]",
    "Gender": "[valid Gender (optional) default is undefined]"
}
```

## **Data example 1**

```json
{
    "From": "2021-05-02",
    "To": "2021-08-02"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Sun May 02 2021 - Mon Aug 02 2021",
    "ProductVisitors": 142
}
```

## **Data example 2**

```json
{
    "From": "2021-05-02",
    "To": "2021-08-02",
    "ProductID": 51
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Sun May 02 2021 - Mon Aug 02 2021",
    "ProductVisitors": 4
}
```

## **Error Response**

**Condition** : If 'From' or 'To' is not specified

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "[Missing field will be specified here]"
}
```
