# Current User

All those endpoints retrieves resources of the current user.

The user is logged in by the authentication headers.

## PUT Informations

> Response:

```json
{
  "data": {
    "id": "234",
    "type": "user",
    "attributes": {
      "address": null,
      "birthdate": null,
      "city": null,
      "clientGeneralRentalConditionSigned": false,
      "country": null,
      "createdAt": "2020-04-09T11:49:37.846+02:00",
      "email": "julien@viviani.fr",
      "firstName": "Julien",
      "lastName": "pardo",
      "gender": null,
      "locale": "fr",
      "nationality": null,
      "ownerGeneralRentalConditionSigned": false,
      "phone": null,
      "postalCode": null,
      "secondaryEmail": null,
      "secondaryPhone": null,
      "updatedAt": "2020-07-06T17:53:00.072+02:00",
      "hasHouses": true,
      "hasCompanies": false
    }
  }
}
```

This endpoint updates the profile informations of the current user

### HTTP Request

`PUT (fr;en)/api/v1/user/informations`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ---- | -------
user[address] | Address of the user | String | 128 Rue de provence
user[birthdate] | Birthdate of the user | Date | 1998-07-13
user[city] | City of the user | String | Paris
user[country] | Country of the user | String (alpha2 country code) | FR
user[first_name] | First name of the user | String | Julien
user[gender] | Gender of the user | String (male/female/unknown) | male
user[last_name] | Last name of the user | String | Viviani
user[nationality] | Nationality of the user | String (alpha2 country code) | FR
user[phone] | Phone of the user | String | 0123456789
user[postal_code] | Zip code of the user | String | 75008
user[secondary_email] | Secondary email of the user | String | julien@viviani.fr
user[secondary_phone] | Secondary phone of the user | String | 0123456788

## Get Client Contracts
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "5215",
      "type": "clientContract",
      "attributes": {
        "clientProcedureYousignToken": null,
        "contract": {
          "id": "5215",
          "type": "contract",
          "attributes": {
            "checkInDate": "2020-08-17",
            "checkInTime": "11:00",
            "checkOutDate": "2020-08-24",
            "checkOutTime": "10:00",
            "houseName": "Villa Notre Dame",
            "houseOldName": "Villa Atlantide",
            "destinationName": "Marseille"
          }
        }
      }
    },
    {
      "id": "4476",
      "type": "clientContract",
      "attributes": {
        "clientProcedureYousignToken": "/members/1218b86c-bb6b-4cc3-afac-e17d88b53791",
        "contract": {
          "id": "4476",
          "type": "contract",
          "attributes": {
            "checkInDate": "2021-08-15",
            "checkInTime": "17:00",
            "checkOutDate": "2021-08-22",
            "checkOutTime": "10:00",
            "houseName": "Villa Difolia",
            "houseOldName": "Villa Amadei",
            "destinationName": "Bonifacio"
          }
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
    "total_count": 2
  }
}
```

This endpoint retrieves all the contracts as client of the current user.

### HTTP Request

`GET /fr/api/v1/user/client_contracts`


## Get one Owner Contract
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": {
    "id": "5215",
    "type": "ownerContract",
    "attributes": {
      "ownerProcedureYousignToken": "/members/1218b86c-bb6b-4cc3-afac-e17d88b53791",
      "contract": {
        "id": "5215",
        "type": "contract",
        "attributes": {
          "checkInDate": "2020-08-17",
          "checkInTime": "11:00",
          "checkOutDate": "2020-08-24",
          "checkOutTime": "10:00",
          "houseName": "Villa Notre Dame",
          "houseOldName": "Villa Atlantide",
          "destinationName": "Marseille"
        }
      }
    }
  }
}
```

This endpoint retrieves all the contracts as owner of the current user.

### HTTP Request

`GET /fr/api/v1/user/owner_contracts/:contract_id`


## Get one Client Contract
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": {
    "id": "5215",
    "type": "clientContract",
    "attributes": {
      "clientProcedureYousignToken": "/members/1218b86c-bb6b-4cc3-afac-e17d88b53791",
      "contract": {
        "id": "5215",
        "type": "contract",
        "attributes": {
          "checkInDate": "2020-08-17",
          "checkInTime": "11:00",
          "checkOutDate": "2020-08-24",
          "checkOutTime": "10:00",
          "houseName": "Villa Notre Dame",
          "houseOldName": "Villa Atlantide",
          "destinationName": "Marseille"
        }
      }
    }
  }
}
```

This endpoint retrieves all the contracts as owner of the current user.

### HTTP Request

`GET /fr/api/v1/user/owner_contracts/:contract_id`


## Get Owner Contracts
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "5215",
      "type": "ownerContract",
      "attributes": {
        "ownerProcedureYousignToken": null,
        "contract": {
          "id": "5215",
          "type": "contract",
          "attributes": {
            "checkInDate": "2020-08-17",
            "checkInTime": "11:00",
            "checkOutDate": "2020-08-24",
            "checkOutTime": "10:00",
            "houseName": "Villa Notre Dame",
            "houseOldName": "Villa Atlantide",
            "destinationName": "Marseille"
          }
        }
      }
    },
    {
      "id": "4476",
      "type": "ownerContract",
      "attributes": {
        "ownerProcedureYousignToken": "/members/1218b86c-bb6b-4cc3-afac-e17d88b53791",
        "contract": {
          "id": "4476",
          "type": "contract",
          "attributes": {
            "checkInDate": "2021-08-15",
            "checkInTime": "17:00",
            "checkOutDate": "2021-08-22",
            "checkOutTime": "10:00",
            "houseName": "Villa Difolia",
            "houseOldName": "Villa Amadei",
            "destinationName": "Bonifacio"
          }
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
    "total_count": 2
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


## Get Owner's Houses
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "3485",
      "type": "house",
      "attributes": {
        "name": "Mas des Anges",
        "bathrooms": 2,
        "bedrooms": 4,
        "capacity": 8,
        "destinationId": 436,
        "firstPhotoUrl": "production/uploads/photos/house-3485/2019-12-16-01f7de533067d924c6a4d82fd938ba47.jpeg"
      }
    }
  ]
}
```

This endpoint retrieves all the houses if the current user is an owner.

### HTTP Request

`GET /fr/api/v1/user/houses`


## Get Owner's houses bookings
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "1237135",
      "type": "booking",
      "attributes": {
        "checkInDate": "2020-07-01",
        "checkOutDate": "2020-07-31",
        "checkInTime": 17,
        "checkOutTime": 10,
        "type": "admin"
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

This endpoint retrieves all the bookings of one of the current user house

### HTTP Request
`GET (fr;en)/api/v1/user/houses/:house_id/bookings?start_date=2020-01-01`

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ---- | -------
start_date | Date of the bookings | Date | 2020-01-01

## Post Owner's ICalendar
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": {
    "id": "91",
    "type": "calendarImport",
    "attributes": {
      "name": "my calendar",
      "url": "www.jejeje.com",
      "houseId": 1799
    }
  }
}
```

This endpoint creates the booking from an ICalendar

### HTTP Request

`POST (fr;en)/api/v1/user/houses/:house_id/calendar_imports`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ---- | -------
*calendar_import[name] | Name of the calendar (20 characters max)| String | My Calendar
*calendar_import[url] | Url of the calendar | String | wwww.mycalendar.com

## Get Owner's ICalendar
<span class='badge badge-blue'>Paginated</span>

by opening a new tab with this url, the ical should download in the navigator 

### URL

`/api/v1/user/houses/:house_id/calendar_imports` (with user's access tokens)
