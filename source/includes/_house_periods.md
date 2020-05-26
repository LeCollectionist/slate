# Houses Periods

For all this endpoints, the `:identifier` can be the `id` or the localized `slug`.

## Get House Periods
<span class='badge badge-blue'>Paginated</span>

> Response:

```json
{
  "data": [
    {
      "id": "937",
      "type": "house",
      "attributes": {
        "startAt": "2020-05-23",
        "endAt": "2020-05-30",
        "price": 542.0,
        "currency": "USD",
        "minimumPrice": 542.0,
        "valid": true,
        "periods": [
          {
            "id": 4,
            "periodType": "weekly_by_saturday",
            "minimumDuration": 1,
            "startAt": "2020-05-23",
            "endAt": "2020-05-30",
            "price": 542.0,
            "houseId": 937,
            "unitPrice": 542.0,
            "nightCount": 7,
            "validMinimumDuration": true,
            "minimumPrice": 542.0
          }
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
    "total_count": 1
  }
}
```

This endpoint retrieves all the house with periods for the given date range.

### HTTP Request

`GET /fr/api/v1/house_periods`

### Query Parameters

*: Mandatory

Parameter | Description | Example
--------- | ----------- | -------
*start_at | Start date of the period | 2020-01-01
*end_at | End date of the period | 2020-01-20
house_ids[] | ID of the wanted houses | 17
currency | Currency of the periods | USD
min_budget | Budget minimum | 100
max_budget | Budget maximum | 15000

## Get House Period

> Response:

```json
{
  "data": {
    "id": "937",
    "type": "house",
    "attributes": {
      "startAt": "2020-05-23",
      "endAt": "2020-05-30",
      "price": 542.0,
      "currency": "USD",
      "minimumPrice": 542.0,
      "valid": true,
      "periods": [
        {
          "id": 4,
          "periodType": "weekly_by_saturday",
          "minimumDuration": 1,
          "startAt": "2020-05-23",
          "endAt": "2020-05-30",
          "price": 542.0,
          "houseId": 937,
          "unitPrice": 542.0,
          "nightCount": 7,
          "validMinimumDuration": true,
          "minimumPrice": 542.0
        }
      ]
    }
  }
}
```

This endpoint retrieves all the house with periods for the given date range.

### HTTP Request

`GET /fr/api/v1/house_periods/937`

### Query Parameters

*: Mandatory

Parameter | Description | Example
--------- | ----------- | -------
*start_at | Start date of the period | 2020-01-01
*end_at | End date of the period | 2020-01-20
currency | Currency of the periods | USD
