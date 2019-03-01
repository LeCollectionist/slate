# Destinations

For all this endpoints, the `:identifier` can be the `id` or the localized `slug`.

For example:

`GET /fr/api/v1/destinations/17`

`GET /fr/api/v1/destinations/ibiza`

## Get All Destinations
<span class='badge badge-blue'>Paginated</span>
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
     {
      "id": "387",
      "type": "destination",
      "attributes": {
        "authorName": "Patmos",
        "cluster": {
          "id": "216",
          "type": "destination",
          "attributes": {
            "name": "Iles du Dodécanèse",
            "slug": {
              "en": "dodecanese-islands",
              "fr": "iles-du-dodecanese"
            },
            "description": "Rhodes & les Iles du Dodécanèse"
          }
        },
        "country": {
          "id": "18",
          "type": "destination",
          "attributes": {
            "name": "Grèce",
            "slug": {
              "en": "greece",
              "fr": "grece"
            },
            "description": "Grèce"
          }
        },
        "description": "Patmos",
        "isCluster": false,
        "isCountry": false,
        "isVisible": false,
        "metaDescription": "Patmos",
        "metaTitle": "Patmos",
        "name": "Patmos",
        "searchMetaDescription": "",
        "searchMetaTitle": "Location villas luxe Patmos",
        "searchText": "",
        "searchTextTitle": "Location villas luxe Patmos",
        "searchUrl": "location-villas-luxe/patmos",
        "slug": {
          "en": "patmos",
          "fr": "patmos"
        },
        "title": "Patmos",
        "whenToLeaveText": "TBC"
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
    "total_count": 567
  }
```

This endpoint retrieves all the destinations.

### HTTP Request

`GET /fr/api/v1/destinations`

`GET /fr/api/v1/destinations?ids=24,878`

`GET /fr/api/v1/destinations?ids[]=24&ids[]=878`

### Query Parameters

Parameter | Description | Example
--------- | ----------- | -------
ids | List of specific destination id | `ids=24,878`

## Get One Destination
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
"data": {
    "id": "71",
    "type": "destination",
    "attributes": {
      "authorName": "Antoine Lorgnier",
      "cluster": {
        "id": "70",
        "type": "destination",
        "attributes": {
          "name": "Corse",
          "slug": {
            "en": "corsica",
            "fr": "corse"
          },
          "description": "Corse"
        }
      },
      "country": {
        "id": "1",
        "type": "destination",
        "attributes": {
          "name": "France",
          "slug": {
            "en": "france",
            "fr": "france"
          },
          "description": "France"
        }
      },
      "description": "Bonifacio - Tout en haut de la montée Saint-Roch...",
      "isCluster": false,
      "isCountry": false,
      "isVisible": true,
      "metaDescription": "En Corse du Sud, la nature est...",
      "name": "Corse du Sud",
      "searchMetaDescription": "Nos locations de villas en Corse du Sud sont...",
      "searchMetaTitle": "Villa Corse du sud - Location villas luxe Corse du Sud",
      "searchText": "Découvrez nos villas en Corse du Sud\r\n\r\nNos locations...",
      "searchUrl": "location-villas-luxe/corse-du-sud",
      "slug": {
        "en": "south-corsica",
        "fr": "corse-du-sud"
      },
      "title": "La Corse du Sud, entre mer et montagne",
      "whenToLeaveText": "C’est en automne, de la mi-septembre à la..."
    }
  }
}
```

This endpoint retrieves a destination.

### HTTP Request

`GET /fr/api/v1/destinations/:identifier`
