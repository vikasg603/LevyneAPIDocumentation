# Product Upload Count

Total products uploaded by Brand in all its websites

**URL** : `/v1/Brand/Reports/ProductUploadedCount`

**Method** : `GET`

**Auth required** : YES

**Data constraints**

```json
{
    "From": "[valid start date]",
    "To": "[valid end date]"
}
```

**Data example**

```json
{
    "From": "2021-03-02",
    "To": "2021-08-02"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Tue Mar 02 2021 - Mon Aug 02 2021",
    "TotalProductsUploaded": 38
}
```

## Error Response

**Condition** : If 'From' or 'To' is not specified

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "[Missing field will be specified here]"
}
```
