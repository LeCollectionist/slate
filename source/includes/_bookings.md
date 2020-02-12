# Bookings

## Create a booking
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "228136",
    "type": "bookingExternal",
    "attributes": {
      "checkInDate": "2020-01-01",
      "checkOutDate": "2020-01-20",
      "checkInTime": 17,
      "checkOutTime": 10,
      "houseId": 3504,
      "booker": "Bonder"
    }
  }
}
```

This endpoint creates a booking for a given house

### HTTP Request

`POST /en/api/v1/houses/:id/booking_externals`

The `:id` parameter must be the house id.

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
booking_external[check_in_date] | Check-in date of the booking | String | '2020-01-01'
booking_external[check_out_date] | Check-out date of the booking | String | '2020-01-20'
bonder | Token to authenticate Bonder | String | 'c74e5890-18ed-4651-92d6-240b986cd767'

## Update a booking
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "228136",
    "type": "bookingExternal",
    "attributes": {
      "checkInDate": "2020-01-01",
      "checkOutDate": "2020-01-20",
      "checkInTime": 17,
      "checkOutTime": 10,
      "houseId": 3504,
      "booker": "Bonder"
    }
  }
}
```

This endpoint updates a booking for a given house

### HTTP Request

`PUT /en/api/v1/houses/:house_id/booking_externals/:id`

The `:house_id` parameter must be the house id.

The `:id` parameter must be the booking id.

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
booking_external[check_in_date] | Check-in date of the booking | String | '2020-01-01'
booking_external[check_out_date] | Check-out date of the booking | String | '2020-01-20'
bonder | Token to authenticate Bonder | String | 'c74e5890-18ed-4651-92d6-240b986cd767'

## Delete a booking
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "status": "ok"
}
```

This endpoint deletes a booking for a given house

### HTTP Request

`DELETE /en/api/v1/houses/:house_id/booking_externals/:id`

The `:house_id` parameter must be the house id.

The `:id` parameter must be the booking id.

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
bonder | Token to authenticate Bonder | String | 'c74e5890-18ed-4651-92d6-240b986cd767'

## Get All Bookings of a house
<span class='badge badge-blue'>Paginated</span>
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
    {
      "id": "4567",
      "type": "booking",
      "attributes": {
        "checkInDate": "2020-02-08",
        "checkOutDate": "2020-02-22",
        "checkInTime": 17,
        "checkOutTime": 10
      }
    },
    {
      "id": "4569",
      "type": "booking",
      "attributes": {
        "checkInDate": "2019-12-28",
        "checkOutDate": "2020-01-04",
        "checkInTime": 17,
        "checkOutTime": 10
      }
    },
    {
      "id": "6789",
      "type": "booking",
      "attributes": {
        "checkInDate": "2019-12-21",
        "checkOutDate": "2019-12-28",
        "checkInTime": 17,
        "checkOutTime": 10
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

This endpoint retrieves all the bookings of a house.

### HTTP Request

`GET /fr/api/v1/houses/:identifier/bookings`

The `:identifier` parameter must be the house id or localized slug.
