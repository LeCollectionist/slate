# Waiting Seaches

## Create a waiting search
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "7",
    "type": "waitingSearch",
    "attributes": {
      "bathrooms": 10,
      "bedrooms": 5,
      "minBudget": 10000,
      "maxBudget": 20000,
      "currency": 'EUR',
      "createdAt": "2020-03-18T17:02:39.252+01:00",
      "destinationId": 17,
      "email": "test@test.fr",
      "endAt": "2020-01-10T00:00:00.000+01:00",
      "firstName": "Julien",
      "lastName": "Viviani",
      "locale": "fr",
      "people": 5,
      "phone": null,
      "startAt": "2020-01-01T00:00:00.000+01:00",
      "userId": 199,
      "updatedAt": "2020-03-18T17:02:39.252+01:00"
    }
  }
}
```

This endpoint creates a waiting search.

### HTTP Request

`POST (fr;en)/api/v1/waiting_searches`

You either need to be logged or to fill the first_name/last_name/email/phone fields.

&ast;: Mandatory

(&ast;): Mandatory if user is not logged in

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ---- | -------
waiting_search[bathrooms] | Bathroom filter | integer | 5
waiting_search[bedrooms] | Bedroom filter | integer | 7
waiting_search[min_budget] | Min. Budget filter | integer | 2000
waiting_search[max_budget] | Max. Budget filter | integer | 5000
waiting_search[currency] | Currency filter | string | 5000 (default: EUR)
waiting_search[people] | People filter | integer | 10
*waiting_search[destination_id] | Destination filter | integer | 17
*waiting_search[start_at] | Start of the searched booking | string | '2020-01-10'
*waiting_search[end_at] | End of the searched booking | string | '2020-01-20'
(*)waiting_search[email] | Email of the customer | string | j.viviani@gmail.com
(*)waiting_search[first_name] | First name of the customer | string | Julien
(*)waiting_search[last_name] | Last name of the customer | string | Viviani
(*)waiting_search[phone] | Phone of the customer | string | 0123456789

