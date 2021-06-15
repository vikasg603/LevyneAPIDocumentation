# Contact Form

Used for Contact Form.

**URL** : `/v1/Website/Brand/ContactForm`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "Name": "[valid name]",
    "Email": "[valid email address]",
    "Subject": "[Text]",
    "Message": "[Text]"
}
```

**Data example**

```json
{
    "Name": "name",
    "Email": "name1234@gmail.com",
    "Subject": "Subject Subject",
    "Message": "Messagemessagemessage"
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

**Condition** : If "Name" is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"Name\" is required"
}

```
**Condition** : If "Email" is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"Email\" is required"
}

```
**Condition** : If "Subject" is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"Subject\" is required"
}

```
**Condition** : If "Message" is not provided.

**Code** : `400 Bad Request`

**Content** :

```json
{
    "status": "Failed",
    "description": "\"Message\" is required"
}

```
