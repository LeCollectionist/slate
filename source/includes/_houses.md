# Houses

For all this endpoints, the `:identifier` can be the `id` or the localized `slug`.

For example:

`GET /fr/api/v1/houses/1`

`GET /fr/api/v1/houses/chalet-megeve`

## Get All Houses
<span class='badge badge-blue'>Paginated</span>
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
    {
      "id": "94",
      "type": "house",
      "attributes": {
        "bathrooms": 5,
        "bedrooms": 6,
        "capacity": 12,
        "minimumStayHighSeason": 7,
        "minimumStayLowSeason": 3,
        "description": null,
        "destinationId": 17,
        "domainSurface": 800,
        "leadText": null,
        "gpslatitude": "43.4897779",
        "gpslongitude": "-1.552215599999954",
        "name": "Villa Trinidad",
        "slug": {
          "en": "villa-trinidad-biarritz",
          "fr": "villa-trinidad-biarritz"
        },
        "state": "published",
        "surface": 320,
        "surrounding": null,
        "firstPhotoUrl": null
        }
      }
    },
    ...
  ],
  "meta": {
    "current_page": 1,
    "next_page": 2,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 44,
    "total_count": 1081
  }
```

This endpoint retrieves all the available houses.

### HTTP Request

`GET /fr/api/v1/houses`

`GET /fr/api/v1/houses?ids=24,878`

`GET /fr/api/v1/houses?ids[]=24&ids[]=878`

### Query Parameters

Parameter | Description | Example
--------- | ----------- | -------
ids | List of specific house id | `ids=24,878`

## Get One House
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "1",
    "type": "house",
    "attributes": {
      "bathrooms": 5,
      "bedrooms": 7,
      "capacity": 14,
      "description": "Îlot de tranquillité, il est loin du tumulte ..",
      "destinationId": 71,
      "domainSurface": 90000,
      "leadText": "Le chalet LC est un alpage ... ",
      "gpslatitude": "47.45678",
      "gpslongitude": "4.456789",
      "name": "Chalet LC",
      "slug": {
        "fr": "chalet-lc",
        "en": "chalet-en"
      },
      "state": "published",
      "surface": 450,
      "surrounding": "À juste quelques kilomètres de la station mythique de Megève,..",
      "firstPhotoUrl": "//first-photo-url"
    }
  }
}
```

This endpoint retrieves an available house.

### HTTP Request

`GET /fr/api/v1/houses/:identifier`

## Get Starred tags
<span class='badge badge-blue'>Paginated</span>
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
    {
      "id": "328",
      "type": "tag",
      "attributes": {
        "isVisible": true,
        "name": "Local à ski et chauffe chaussures",
        "photo": "url-of-the-tag"
      }
    },
    ...
    {
      "id": "309",
      "type": "tag",
      "attributes": {
        "isVisible": true,
        "name": "Cave à vin",
        "photo": null
      }
    }
  ],
  "meta": {
    "current_page": 1,
    "next_page": null,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 1,
    "total_count": 10
  }
}
```

This endpoint retrieves all the starred tags of a house.

### HTTP Request

`GET /fr/api/v1/houses/:identifier/starrings`

## Get Experiences
<span class='badge badge-blue'>Paginated</span>
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
    {
      "id": "191",
      "type": "activity",
      "attributes": {
        "address": null,
        "description": "Arpentez le large territoire du Mont ...",
        "leadText": "",
        "name": "Jouer les apprentis musher"
      }
    },
    ...
    {
      "id": "197",
      "type": "activity",
      "attributes": {
        "address": null,
        "description": "Devenez un oiseau de nuit en parcourant...",
        "leadText": "",
        "name": "Explorer les stations de ski la nuit"
      }
    }
  ],
  "meta": {
    "current_page": 1,
    "next_page": null,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 1,
    "total_count": 3
  }
}
```

This endpoint retrieves all the experiences of the destination's house.

### HTTP Request

`GET /fr/api/v1/houses/:identifier/experiences`

## Get Tag's Group by Section
<span class='badge badge-blue'>Paginated</span>
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
    {
      "id": "79",
      "type": "group",
      "attributes": {
        "name": "Bureau",
        "position": 18,
        "tags": [
          {
            "id": "272",
            "type": "tag",
            "attributes": {
              "isVisible": false,
              "name": "Table",
              "photo": null
            }
          },
          ...
          {
            "id": "271",
            "type": "tag",
            "attributes": {
              "isVisible": false,
              "name": "Téléphone",
              "photo": null
            }
          }
        ]
      }
    },
    {
      "id": "16",
      "type": "group",
      "attributes": {
        "name": "Salle à manger",
        "position": 3,
        "tags": [
          {
            "id": "182",
            "type": "tag",
            "attributes": {
              "isVisible": false,
              "name": "Nombre de personnes assises",
              "photo": null
            }
          },
          ...
        ]
      }
    }
  ],
  "meta": {
    "current_page": 1,
    "next_page": null,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 1,
    "total_count": 20
  }
    
```

This endpoint retrieves all the tags of a section's house.

The possible the sections are:

+ rooms
+ location
+ essentials
+ amenities
+ outdoor_and_recreation

### HTTP Request

`GET /fr/api/v1/houses/:identifier/sections/rooms`

`GET /fr/api/v1/houses/:identifier/sections/location`

`GET /fr/api/v1/houses/:identifier/sections/essentials`

`GET /fr/api/v1/houses/:identifier/sections/amenities`

`GET /fr/api/v1/houses/:identifier/sections/outdoor_and_recreation`

## Get Photos
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "4822",
      "type": "photo",
      "attributes": {
        "position": 14,
        "url": "first-photo-url"
      }
    },
    ...
    {
      "id": "40961",
      "type": "photo",
      "attributes": {
        "position": 37,
        "url": "second-photo-url"
      }
    },
  ],
  "meta": {
    "current_page": 1,
    "next_page": 2,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 2,
    "total_count": 27
  }
}
```

This endpoint retrieves all the photos of the house.

### HTTP Request

`GET /fr/api/v1/houses/:identifier/photos`

## Get Prices
<span class='badge badge-blue'>Paginated</span>
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
    {
      "id": "4567",
      "type": "price",
      "attributes": {
        "houseId": 7,
        "contractPrice": 5700,
        "currency": "EUR",
        "day": "2018-01-01",
        "fee": "0.25",
        "ownerPrice": 4560,
        "publicPrice": 5700,
        "season": "high",
        "taxesAndCharges": "0.0"
      }
    },
    ...
    {
      "id": "5678",
      "type": "price",
      "attributes": {
        "houseId": 7,
        "contractPrice": 3286,
        "currency": "EUR",
        "day": "2018-01-25",
        "fee": "0.25",
        "ownerPrice": 2629,
        "publicPrice": 3286,
        "season": "low",
        "taxesAndCharges": "0.0"
      }
    }
  ],
  "meta": {
    "current_page": 1,
    "next_page": 2,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 46,
    "total_count": 1128
  }
}
```

This endpoint retrieves all the prices of the house.

### HTTP Request

`GET /fr/api/v1/houses/:identifier/prices`

## Get Booking Flights
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "6975",
      "type": "bookingFlight",
      "attributes": {
        "startOn": "2020-03-22",
        "endOn": "2020-03-29",
        "price": null,
        "kind": "external",
        "currency": null,
        "checkInTime": null,
        "checkOutTime": null,
        "bookingInfo": "External",
        "houseId": 780
      }
    },
    ...
    {
      "id": "6981",
      "type": "bookingFlight",
      "attributes": {
        "startOn": "2020-03-29",
        "endOn": "2020-04-05",
        "price": null,
        "kind": "external",
        "currency": null,
        "checkInTime": null,
        "checkOutTime": null,
        "bookingInfo": "External",
        "houseId": 780
      }
    }
  ],
  "meta": {
    "current_page": 1,
    "next_page": 2,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 4,
    "total_count": 89
  }
}
```

This endpoint retrieves all the booking flights of the house.

### HTTP Request

`GET /fr/api/v1/houses/:identifier/booking_flights`
