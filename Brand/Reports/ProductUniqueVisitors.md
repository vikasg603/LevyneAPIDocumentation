# Product Unique Visitors

Used to count _unique_ _visitors_ of products on specific Brand wesbites or of particular Product.

**URL** : `/v1/Brand/Reports/ProductUniqueVisitors`

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
    "From": "2021-05-31",
    "To": "2021-06-02"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Mon May 31 2021 - Wed Jun 02 2021",
    "UniqueVisitorCount": 18
}
```

## **Data example 2**

```json
{
    "From": "2021-05-31",
    "To": "2021-06-02",
    "ProductID": 51
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Mon May 31 2021 - Wed Jun 02 2021",
    "UniqueVisitorCount": 3
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
