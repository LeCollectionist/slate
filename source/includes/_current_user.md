# Current User

All those endpoints retrieves resources of the current user.

The user is logged in by the authentication headers.

## Get Client Contracts
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "3970",
      "type": "contract",
      "attributes": {
        "checkInDate": "2020-05-20",
        "checkInTime": "17:00",
        "checkOutDate": "2020-05-28",
        "checkOutTime": "10:00",
        "houseName": "Villa Lumière",
        "houseOldName": "the two sisters",
        "destinationName": "Gordes & alentours"
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
    "total_count": 1
  }
}
```

This endpoint retrieves all the contracts as client of the current user.

### HTTP Request

`GET /fr/api/v1/user/client_contracts`

## Get Owner Contracts
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "3970",
      "type": "contract",
      "attributes": {
        "checkInDate": "2020-05-20",
        "checkInTime": "17:00",
        "checkOutDate": "2020-05-28",
        "checkOutTime": "10:00",
        "houseName": "Villa Lumière",
        "houseOldName": "the two sisters",
        "destinationName": "Gordes & alentours"
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
    "total_count": 1
  }
}
```

This endpoint retrieves all the contracts as owner of the current user.

### HTTP Request

`GET /fr/api/v1/user/owner_contracts`


## Get Companies
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "1",
      "type": "company",
      "attributes": {
        "accountOwner": null,
        "address": "126 Rue de Provence",
        "bic": null,
        "city": "Paris",
        "country": "FR",
        "createdAt": "2020-06-15T19:42:47.820+02:00",
        "email": "contact@lecollectionist.com",
        "iban": null,
        "name": "LeCollectionist",
        "phone": "0123456789",
        "postalCode": "75008",
        "representativeFirstName": "Julien",
        "representativeGender": "male",
        "representativeLastName": "Viviani",
        "siret": "01234567891231",
        "updatedAt": "2020-06-15T19:42:47.820+02:00"
      }
    }
  ],
  "meta": {
    "current_page": 1,
    "next_page": null,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 1,
    "total_count": 1
  }
}
```

This endpoint retrieves all the companies of the current user

### HTTP Request

`GET /fr/api/v1/user/companies`

## Get Client Houses
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "3485",
      "type": "house",
      "attributes": {
        "bathrooms": 2,
        "bedrooms": 4,
        "capacity": 8,
        "description": null,
        "destinationId": 436,
        "displayAvailabilities": true,
        "displayPrices": true,
        "exclusivity": false,
        "flexibleCancelation": false,
        "domainSurface": 600,
        "gpslatitude": "43.925534",
        "gpslongitude": "5.251559",
        "housekeeping": "mid_stay",
        "housekeepingHours": "3_hours",
        "leadText": null,
        "licenceNumber": null,
        "minimumStayHighSeason": 7,
        "minimumStayLowSeason": 3,
        "name": "Mas des Anges",
        "onlineReservation": false,
        "slug": {
          "en": "mas-des-anges-gordes-surroundings",
          "fr": "mas-des-anges-gordes-alentours"
        },
        "state": "offboarded",
        "surface": 170,
        "surrounding": null,
        "firstPhotoUrl": "production/uploads/photos/house-3485/2019-12-16-01f7de533067d924c6a4d82fd938ba47.jpeg",
        "featuredPhotoUrl": null,
        "maxPrice": {
          "CHF": 779.0,
          "EUR": 728.0,
          "GBP": 653.0,
          "USD": 823.0
        },
        "minPrice": {
          "CHF": 492.0,
          "EUR": 460.0,
          "GBP": 412.0,
          "USD": 520.0
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
    "total_count": 1
  }
}
```

This endpoint retrieves all the houses if the current user is an owner.

### HTTP Request

`GET /fr/api/v1/user/houses`