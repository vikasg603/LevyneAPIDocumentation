# FetchSearchSuggestion

Used to collect search suggestions.

**URL** : `/v1/Website/Products/SearchSuggestions`

**Method** : `GET`

**Auth required** : NO

**Data constraints**

```json
{
    "SearchKey": "[string]"
}
```

**Data example**

```json
{
    "SearchKey":"Alaina"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
[
    "Alaina",
    "A classic top with a layerd sharara",
    "Stylish top with a trumpet lehenga",
    "Peplum with umbrella skirt",
    "Mid thigh kurti with a skirt",
    "Ethnic indoswestern",
    "Rosy brown cape top",
    "Floral print lehenga",
    "Black Shimmer Gown",
    "Cami top and flared sharara",
    "Aline kurti with ankle pants",
    "An oblong blouse with a skirt",
    "V Neck Top and Sharara",
    "Peplum top and Sharara",
    "Red crop top Lehenga",
    "Heres a red",
    "Tubetopped couture",
    "Blazer of your choice",
    "A crop top with lehenga",
    "Everblue wedding Lucknowi",
    "Onesided pleated sherwani"
]
```

## Error Response

**Condition** : No error

**Code** : `No error`

**Content** :

```json
No error
```
