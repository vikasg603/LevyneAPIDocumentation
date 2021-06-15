# TopSearchedKeywords

Used to check the top searched keywords

**URL** : `/v1/Brand/Reports/TopSearchedKeywords`

**Method** : `GET`

**Auth required** : YES

**URL constraints**

```json
http://localhost:8080/v1/Brand/Reports/TopSearchedKeywords/?From="<Date>"&To="<Date>""&type=<SearchKey | Category>
```

**URL example**

```json
http://localhost:8080/v1/Brand/Reports/TopSearchedKeywords/?From="2021-06-05"&To="2021-06-05"&type=Category
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "label": "Sat Jun 05 2021 - Sat Jun 05 2021",
    "TopSearchedKeywords": [
        []
    ]
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
