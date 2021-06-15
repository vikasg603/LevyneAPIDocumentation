# Orders Count

Used to count total orders to particular Brand.

**URL** : `/v1/Brand/Reports/FetchOrdersCount `

**Method** : `GET`

**Auth required** : YES

**Data constraints**

```json
{
    "From": "[valid start date]",
    "To": "[valid end date]",
    "difference": "[days difference (optional) default is 1]"
}
```

**Data example 1**

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
[
    {
        "label": "Mon May 31 2021 - Mon May 31 2021",
        "totalOrders": 7
    },
    {
        "label": "Tue Jun 01 2021 - Tue Jun 01 2021",
        "totalOrders": 4
    },
    {
        "label": "Wed Jun 02 2021 - Wed Jun 02 2021",
        "totalOrders": 0
    }
]
```

**Data example 2**

```json
{
    "From": "2021-05-31",
    "To": "2021-06-02",
    "difference": 2
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "label": "Mon May 31 2021 - Tue Jun 01 2021",
        "totalOrders": 11
    },
    {
        "label": "Wed Jun 02 2021 - Wed Jun 02 2021",
        "totalOrders": 0
    }
]
```

## Error Response

**Condition** : If 'From' or 'To' is not specified.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "[Missing field will be specified here]"
}
```
