# Inquiries

## Create an Inquiry
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "35440",
    "type": "request",
    "attributes": {
      "clientAccountId": 27752,
      "createdAt": "2020-01-30T13:35:43.037+01:00",
      "endDate": "2020-01-20",
      "houseId": 237,
      "notes": null,
      "people": 12,
      "startDate": "2020-01-01",
      "updatedAt": "2020-01-30T13:35:43.037+01:00"
    }
  }
}
```

This endpoint creates an inquiry

### HTTP Request

`POST (fr;en)/api/v1/requests`

Either the house_id or the destination_id is required, not both of them at the same time.

*: Mandatory

### Query Parameters

Parameter | Description | Example
--------- | ----------- | -------
*request[house_id] | ID of the house | 237
*request[destination_id] | ID of the destination | 17
*request[end_date] | End date of the request | '2020-01-01'
*request[start_date] | Start date of the request | '2020-01-20'
*request[favorite_contact] | Favorite contact of the client | email / phone / whatsapp
*request[phone] | Phone of the client | '0611234581'
*request[budget] | Budget of the client | 12000
*request[people] | Number of people for the request | 12
request[notes] | Extra information about the request | ''
*person[email] | Email of the client | j.l@gmail.com
*person[firstname] | First name of the client | Julien
*person[lastname] | Last name of the client | Mpa
*person[newsletter] | Client accepted newsletter | true / false
person[wishlist_token] | Token of the client wishlist | 'c74e5890-18ed-4651-92d6-240b986cd767'
