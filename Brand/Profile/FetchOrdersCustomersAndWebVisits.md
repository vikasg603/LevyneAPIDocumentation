# FetchOrdersCustomersAndWebVisits

Used to Fetch Orders Customers And Web Visits

**URL** : `/v1/Brand/Profile/FetchOrdersCustomersAndWebVisits`

**Method** : `GET`

**Auth required** : YES

**Data constraints**

```json
{
}
```

**Data example**

```json
{
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "TotalOrders": 0,
    "TotalCustomers": 1,
    "TotalWebVisits": 10,
    "AvgBrandRating": 0
}
```

## Error Response

**Condition** : If 'authorization' is not provided.

**Code** : `401 Unauthorized`

**Content** :

```json
{
	"status": "Failed",
	"description": "Authorization header not found"
}
```
