# Wishlists

## Get One Wishlist
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "7",
    "type": "wishlist",
    "attributes": {
      "token": "Hr82kZh9zCrGmfBC4b8eYTm2",
      "houses": [
        {
          "id": "235",
          "type": "house",
          "attributes": {
            "bathrooms": 0,
            "bedrooms": 4,
            "capacity": 8,
            "description": "When you first stroll down Rue J...",
            "destinationId": 85,
            "domainSurface": 0,
            "gpslatitude": "42.269895",
            "gpslongitude": "6.638203",
            "hiddenPrice": false,
            "housekeeping": "2_days",
            "housekeepingHours": "3_hours",
            "leadText": "Appartement LC is a dive into the heart of...",
            "licenceNumber": "",
            "minimumStayHighSeason": 7,
            "minimumStayLowSeason": 3,
            "name": "Appartement LC",
            "slug": {
              "en": "appartement-lc",
              "fr": "appartement-lc"
            },
            "state": "published",
            "surface": 240,
            "surrounding": "Dawn has barely broken but the port of...",
            "firstPhotoUrl": "photo-url.jpg",
            "maxPrice": {
              "CHF": 1422,
              "EUR": 1250,
              "GBP": 1078,
              "USD": 1404
            },
            "minPrice": {
              "CHF": 996,
              "EUR": 875,
              "GBP": 755,
              "USD": 983
            }
          }
        }
      ]
    }
  }
}
```

This endpoint retrieves a wishlist

### HTTP Request

`GET /fr/api/v1/wishlists/:token`

## Creates A Wishlist
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "7",
    "type": "wishlist",
    "attributes": {
      "token": "Hr82kZh9zCrGmfBC4b8eYTm2",
      "houses": [
        {
          "id": "235",
          "type": "house",
          "attributes": {
            "bathrooms": 0,
            "bedrooms": 4,
            "capacity": 8,
            "description": "When you first stroll down Rue J...",
            "destinationId": 85,
            "domainSurface": 0,
            "gpslatitude": "42.269895",
            "gpslongitude": "6.638203",
            "hiddenPrice": false,
            "housekeeping": "2_days",
            "housekeepingHours": "3_hours",
            "leadText": "Appartement LC is a dive into the heart of...",
            "licenceNumber": "",
            "minimumStayHighSeason": 7,
            "minimumStayLowSeason": 3,
            "name": "Appartement LC",
            "slug": {
              "en": "appartement-lc",
              "fr": "appartement-lc"
            },
            "state": "published",
            "surface": 240,
            "surrounding": "Dawn has barely broken but the port of...",
            "firstPhotoUrl": "photo-url.jpg",
            "maxPrice": {
              "CHF": 1422,
              "EUR": 1250,
              "GBP": 1078,
              "USD": 1404
            },
            "minPrice": {
              "CHF": 996,
              "EUR": 875,
              "GBP": 755,
              "USD": 983
            }
          }
        }
      ]
    }
  }
}
```

This endpoint creates a wishlist

### HTTP Request

`POST /fr/api/v1/wishlists`
with parameter
`wishlist[house_ids][]=235`

You can send many times the `wishlist[house_ids][]` parameter with different house id.

## Updates A Wishlist
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "7",
    "type": "wishlist",
    "attributes": {
      "token": "Hr82kZh9zCrGmfBC4b8eYTm2",
      "houses": []
    }
  }
}
```

This endpoint updates a wishlist.


You must send all the ids of the wishlist.

Not including a house id related to the wishlist will unlink them.

### HTTP Request

`PUT /fr/api/v1/wishlists/Hr82kZh9zCrGmfBC4b8eYTm2`

You can send many times the `wishlist[house_ids][]` parameter with different house id.
