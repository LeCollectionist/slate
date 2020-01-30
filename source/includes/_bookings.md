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

`POST /api/v1/houses/:id/booking_external`

The `:id` parameter must be the house id.

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
booking_external[check_in_date] | Check-in date of the booking | string | '2020-01-01'
booking_external[check_out_date] | Check-out date of the booking | string | '2020-01-20'
bonder | Token to authenticate Bonder | string | 'c74e5890-18ed-4651-92d6-240b986cd767'

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

`PUT /api/v1/houses/:house_id/booking_external/:id`

The `:house_id` parameter must be the house id.
The `:id` parameter must be the booking id.

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
booking_external[check_in_date] | Check-in date of the booking | string | '2020-01-01'
booking_external[check_out_date] | Check-out date of the booking | string | '2020-01-20'
bonder | Token to authenticate Bonder | string | 'c74e5890-18ed-4651-92d6-240b986cd767'

## Delete a booking
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  status: 'ok'
}
```

This endpoint deletes a booking for a given house

### HTTP Request

`DELETE /api/v1/houses/:house_id/booking_external/:id`

The `:house_id` parameter must be the house id.
The `:id` parameter must be the booking id.
