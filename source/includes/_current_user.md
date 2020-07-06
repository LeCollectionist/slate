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

> Response:

```json
{
  "data": {
    "id": "90",
    "type": "calendarImport",
    "attributes": {
      "name": "my calendar",
      "url": "www.jejeje.com",
      "houseId": 3485
    }
  }
}
```

This endpoint get url from an ICalendar

### HTTP Request

`GET (fr;en)/api/v1/user/houses/:house_id/calendar_imports`
