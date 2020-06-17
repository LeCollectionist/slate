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
