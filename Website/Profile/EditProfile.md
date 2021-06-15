# Edit Profile

Used to Edit Profile.

**URL** : `/v1/Website/Profile/EditProfile`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "Name" : "[string]",
    "Email": "[valid email address]",
    "Gender": "[0 | 1]"
}
```

**Data example**

```json
{
    "Name": "prachi",
    "Email":"prachi31@gmail.com",
    "Gender": 0
}
```

## Success Response

**Code** : `200 OK`

**Output Constraints**

```json
{
    "status": "Success"
}
```

**Output example**

```json
{
    "status": "Success"
}
```

## Error Response

**Condition** : If 'UserID' (primary key) is repeated.

**Code** : `500 Internal Server Error`

**Content** :

```json
{
    "status": "Failed",
    "description": "Internal Server Error"
}
```
