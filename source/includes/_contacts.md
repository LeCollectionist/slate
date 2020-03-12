# Contacts

## Create a contact
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": {
    "id": "178",
    "type": "contact",
    "attributes": {
      "firstName": "Julien",
      "lastName": "Viviani",
      "phone": "0134567890",
      "email": "j.viviani@gmail.com",
      "locale": "en",
      "message": "A message"
    }
  }
}
```

This endpoint creates a contact

### HTTP Request

`POST (fr;en)/api/v1/contacts`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ---- | -------
*contact[first_name] | First name of the contact sender | String | Julien
*contact[last_name] | Last name of the contact sender | String | Viviani
*contact[email] | Email of the contact sender | String | j.viviani@gmail.com
*contact[phone] | Phone of the contact sender | String | 0123456789
*contact[message] | Message | String | A message
