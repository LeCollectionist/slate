# Houses

## Get All
<span class='badge badge-bleu'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "24",
      "type": "house",
      "attributes": {
        "name": "Appartement 1",
        "slug": {
          "en": "appartement-1",
          "fr": "appartement-1"
        },
        "firstPhotoUrl": "url-of-the-img-appartement"
      }
    },
    {
      "id": "878",
      "type": "house",
      "attributes": {
        "name": "Villa 878",
        "slug": {
          "en": "villa-878",
          "fr": "villa-878"
        },
        "firstPhotoUrl": null
      }
    }
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

`GET http://example.com/api/v1/houses`

`GET http://example.com/api/v1/houses?ids=24,878`

`GET http://example.com/api/v1/houses?ids[]=24&ids[]=878`

### Query Parameters

Parameter | Description | Example
--------- | ----------- | -------
ids | List of specific house id | `ids=24,878`

## Get One

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
      "description": {
        "en": "This peaceful getaway ...",
        "fr": "Îlot de tranquillité, il est loin du tumulte .."
      },
      "domainSurface": 90000,
      "leadText": {
        "en": "Chalet LC is an authentic ...",
        "fr": "Le chalet LC est un alpage ... "
      },
      "gpslatitude": "47.45678",
      "gpslongitude": "4.456789",
      "name": "Chalet LC",
      "slug": {
        "en": "chalet-lc",
        "fr": "chalet-lc"
      },
      "state": "published",
      "surface": 450,
      "surrounding": {
        "en": "Located just a few kilometres ...",
        "fr": "À juste quelques kilomètres de la station mythique de Megève,.."
      },
      "firstPhotoUrl": "first-photo-url"
    }
  }
}
```

This endpoint retrieves an available house.

### HTTP Request

`GET http://example.com/api/v1/houses/1`

## Get Starred tags
<span class='badge badge-bleu'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "328",
      "type": "tag",
      "attributes": {
        "isVisible": true,
        "name": {
          "en": "Ski closet and shoe heaters",
          "fr": "Local à ski et chauffe chaussures"
        },
        "photo": "url-of-the-tag"
      }
    },
    ...
    {
      "id": "309",
      "type": "tag",
      "attributes": {
        "isVisible": true,
        "name": {
          "en": "Wine cellar",
          "fr": "Cave à vin"
        },
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

`GET http://example.com/api/v1/houses/1/starrings`

## Get Experiences
<span class='badge badge-bleu'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "191",
      "type": "activity",
      "attributes": {
        "address": {
          "en": null,
          "fr": null
        },
        "description": {
          "en": "Cross the vast territory ...",
          "fr": "Arpentez le large territoire du Mont ..."
        },
        "leadText": {
          "en": "",
          "fr": ""
        },
        "name": {
          "en": "Play the musher apprentice",
          "fr": "Jouer les apprentis musher"
        }
      }
    },
    ...
    {
      "id": "197",
      "type": "activity",
      "attributes": {
        "address": {
          "en": null,
          "fr": null
        },
        "description": {
          "en": "Become a night owl and ski the slopes...",
          "fr": "Devenez un oiseau de nuit en parcourant..."
        },
        "leadText": {
          "en": "",
          "fr": ""
        },
        "name": {
          "en": "Explore the ski resorts at night",
          "fr": "Explorer les stations de ski la nuit"
        }
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

`GET http://example.com/api/v1/houses/1/experiences`

## Get Tag's Group by Section
<span class='badge badge-bleu'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "79",
      "type": "group",
      "attributes": {
        "name": {
          "en": "Office",
          "fr": "Bureau"
        },
        "position": 18,
        "tags": [
          {
            "id": "272",
            "type": "tag",
            "attributes": {
              "isVisible": false,
              "name": {
                "en": "Table",
                "fr": "Table"
              },
              "photo": null
            }
          },
          ...
          {
            "id": "271",
            "type": "tag",
            "attributes": {
              "isVisible": false,
              "name": {
                "en": "Landline phone",
                "fr": "Téléphone"
              },
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
        "name": {
          "en": "Dining room",
          "fr": "Salle à manger"
        },
        "position": 3,
        "tags": [
          {
            "id": "182",
            "type": "tag",
            "attributes": {
              "isVisible": false,
              "name": {
                "en": "Seats",
                "fr": "Nombre de personnes assises"
              },
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

`GET http://example.com/api/v1/houses/1/sections/rooms`

`GET http://example.com/api/v1/houses/1/sections/location`

`GET http://example.com/api/v1/houses/1/sections/essentials`

`GET http://example.com/api/v1/houses/1/sections/amenities`

`GET http://example.com/api/v1/houses/1/sections/outdoor_and_recreation`

## Get Prices
<span class='badge badge-bleu'>Paginated</span>

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

`GET http://example.com/api/v1/houses/7/prices`

