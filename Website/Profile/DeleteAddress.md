# Delete Address

Used to Delete Address.

**URL** : `/v1/Website/Profile/DeleteAddress`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "AddressID": "[number]"
}
```

**Data example**

```json
{
    "AddressID":16
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

**Condition** : If 'AddressID' is not provided.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"AddressID\" is required"
}
```
