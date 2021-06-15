# About Us Page

Used for About Us Page.

**URL** : `/v1/Website/Brand/AboutUsPage`

**Method** : `GET`

**Auth required** : NO

**Data constraints**

```json
No data required
```

**Data example**

```json
No data required
```

## Success Response

**Code** : `200 OK`

**Output Constraints**

```json
{
    "IndustryID": number,
    "Mobile": number,
    "isMobilePublic": number,
    "BrandProfile.Gender": 0 | 1,
    "BrandProfile.Name": string,
    "BrandProfile.ProfileImage": string,
    "BrandProfile.About": string,
    "BrandAddress.Address": string,
    "BrandAddress.PinCode": number,
    "BrandAddress.Latitude": float,
    "BrandAddress.Longitude": float,
    "BrandStoreTimings.Day": null,
    "BrandStoreTimings.StartTiming": null,
    "BrandStoreTimings.CloseTiming": null
}
```

**Output example**

```json
{
    "IndustryID": 1,
    "Mobile": 9347423906,
    "isMobilePublic": 2,
    "BrandProfile.Gender": 1,
    "BrandProfile.Name": "Kristopher",
    "BrandProfile.ProfileImage": "https://placeimg.com/400/400?random=1",
    "BrandProfile.About": "laboriosam veniam dolores",
    "BrandAddress.Address": "311 Quitzon Coves",
    "BrandAddress.PinCode": 52681,
    "BrandAddress.Latitude": 38.83580017,
    "BrandAddress.Longitude": -87.33550262,
    "BrandStoreTimings.Day": null,
    "BrandStoreTimings.StartTiming": null,
    "BrandStoreTimings.CloseTiming": null
}
```

## Error Response

**Condition** : No error

**Code** : `No Error`

**Content** :

```json
No error
```
