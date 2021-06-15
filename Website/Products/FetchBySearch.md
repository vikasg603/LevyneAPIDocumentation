# FetchBySearch

Used to collect users's and search details.

**URL** : `/v1/Website/Products/FetchBySearch`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "City": keyword,
    "Handset":keyword ,
    "Operator":keyword ,
    "isSaveDataEnabled":boolean ,
    "NetworkType":keyword ,
    "DeviceMemory":byte,
    "UserAgent":keyword,
    "vendor": keyword,
    "browser":keyword,
    "isMobile":boolean ,
    "OS": keyword,
    "utm_source":keyword,
    "utm_medium": keyword,
    "utm_campaign": keyword,
    "batteryPercentage":byte,
    "SearchKey": keyword,
    "Filters": keyword
}
```

**Data example**

```json
{
    "City": "pune",
    "Handset":"Samsung" ,
    "Operator":"android" ,
    "isSaveDataEnabled":"true" ,
    "NetworkType":"jio" ,
    "DeviceMemory": "8",
    "UserAgent":"xyz",
    "vendor": "abc",
    "browser":"chrome",
    "isMobile":"true" ,
    "OS": "1",
    "utm_source":"hij",
    "utm_medium": "pol",
    "utm_campaign": "nots",
    "batteryPercentage":"30",
    "SearchKey": "Langosh, Balistreri and Murray",
    "Filters": "Pants"
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

**Condition** : No error

**Code** : `No error`

**Content** :

```json
No error
```
