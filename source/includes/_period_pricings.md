# Period pricings

## Get Period pricings

> Response:

```json
{
  "data": [
    {
      "id": "39",
      "type": "periodPricing",
      "attributes": {
        "periodType": "weekly_by_saturday",
        "minimumDuration": 1,
        "price": 200.0,
        "houseId": 937,
        "startAt": "2020-03-14",
        "endAt": "2020-03-21",
        "currency": "USD",
        "nightCount": 7
      }
    },
    {
      "id": "40",
      "type": "periodPricing",
      "attributes": {
        "periodType": "weekly_by_sunday",
        "minimumDuration": 1,
        "price": 300.0,
        "houseId": 937,
        "startAt": "2020-03-22",
        "endAt": "2020-03-29",
        "currency": "USD",
        "nightCount": 7
      }
    }
  ]
}
```

This endpoint retrieves the pricings of the given period.

`start_at` and `end_at` parameters must be valid date as `YYYY-MM-DD`.

`start_at` parameter must be inferior to `end_at` parameter.

`currency` parameter must be a valid currency in `EUR/USD/GBP/CHF`.

If the given period is not fully covered by the house periods, it will ends as 'Bad request' response (400).


### HTTP Request

`GET /api/v1/houses/:id/period_pricings?start_at=2020-03-14&end_at=2020-03-29`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
start_at | Start of the period | Date as a string | 2020-01-01
end_at | End of the period | Date as a string | 2020-01-10
currency | Currency of the price | String | USD
