# RequestEditProfile

Used to request edit profile

**URL** : `/v1/Brand/Profile/RequestEditProfile`

**Method** : POST

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
    "status": "Success"
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
