# Brand Website Unique Visitors

Used to fetch unique visitors of all websites of particular Brand.

**URL** : `/v1/Brand/Reports/BrandWebsiteUniqueVisitors`

**Method** : `GET`

**Auth required** : YES

**Data constraints**

```json
{
    "WebsiteID": "[valid WebsiteID]",
    "From": "[Valid start date]",
    "To": "[Valid end date]"
}
```

**Data example**

```json
{
    "WebsiteID": 1,
    "From": "2020-06-08",
    "To": "2022-09-29"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Tue Jun 01 2021 -  Thu Jul 01 2021",
    "UniqueVisitorCount": 87
}
```

## Error Response

**Condition** : If 'WebsiteID' is not valid

**Code** : `503 Service Unavailable `

**Content** :

```json
{
    "status": "Failed",
    "description": "Something went wrong"
}
```

**Or**

**Condition** : If 'From', 'To' or 'WebsiteID' is not specified.

**Code** : `400 Bad Request `

**Content** :

```json
{
    "status": "Failed",
    "description": "[Missing field will be specified here]"
}
```
