# Contracts

## Client : Update contract as a person

> Response:

```json
{
  "data": {
    "id": "4004",
    "type": "contract"
  }
}
```

This endpoint updates the contract as a client.

The user must be logged in while doing this request.

the `persist_user_profile` parameter allows the client to save this informations into his LC account.

### HTTP Request

`PUT /api/v1/client_contracts/:id`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
*contract[client_firstname] | First name of the client | string | Julien
*contract[client_lastname] | Last name of the client | string | Viviani
*contract[client_address] | Address of the client | string | 126 Rue de Provence
*contract[client_postal_code] | Postal code of the client | string | 75008
*contract[client_city] | City of the client | string | Paris
*contract[client_country] | Country of the client | string (alpha2 country code) | FR
*contract[client_phone] | Phone of the client | string | 01 73 03 02 02
*contract[client_nationality] | Nationality of the client | string (alpha2 country code) | FR
contract[client_phone2] | Secondary phone of the client | string | 01 73 03 02 03
*contract[client_email] | Email of the client | string | julien@viviani.fr
contract[client_email2] | Secondary email of the client | string | adrien@lerpscher.fr
*contract[client_birthdate] | Birthdate of the client | date (YYYY-MM-DD) | 1988-11-08
persist_user_profile | Updates the client account with the given informations | presence | true/1

## Client : Update contract as a company

> Response:

```json
{
  "data": {
    "id": "4004",
    "type": "contract"
  }
}
```

This endpoint updates the contract as a client company.

The user must be logged in while doing this request.

The client must choose between 2 ways of update :

  - With an existing company by filling the `*contract[client_company_id]` parameter.

  OR

  - Without an existing company and by filling all the others mandatory parameters.

the `persist_company` parameter allows the client to save this informations about his company.

### HTTP Request

`PUT /api/v1/client_contracts/:id?context=company`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
*contract[client_company_name] | Name of the client company | string | Le Collectionist
*contract[client_company_siret] | SIRET of the client company | string (14) | 01234567891234
*contract[client_company_address] | Address of the client | string | 126 Rue de Provence
*contract[client_company_postal_code] | Postal code of the client | string | 75008
*contract[client_company_city] | City of the client | string | Paris
*contract[client_company_country] | Country of the client | string (alpha2 country code) | FR
*contract[client_company_phone] | Phone of the client | string | 01 73 03 02 02
*contract[client_company_representative_gender] | Gender of the representative client | string (male/female/unknown) | female
*contract[client_company_representative_firstname] | First name of the representative client | Julien
*contract[client_company_representative_lastname] | Last name of the representative client | Viviani
*contract[client_company_id] | Last name of the representative client | Viviani
persist_company | Creates a related company to the client | presence | true/1

## Owner : Update contract as a person

> Response:

```json
{
  "data": {
    "id": "4004",
    "type": "contract"
  }
}
```

This endpoint updates the contract as a owner.

The user must be logged in while doing this request.

the `persist_user_profile` parameter allows the owner to save this informations into his LC account.

### HTTP Request

`PUT /api/v1/owner_contracts/:id`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
*contract[owner_firstname] | First name of the owner | string | Julien
*contract[owner_lastname] | Last name of the owner | string | Viviani
*contract[owner_address] | Address of the owner | string | 126 Rue de Provence
*contract[owner_postal_code] | Postal code of the owner | string | 75008
*contract[owner_city] | City of the owner | string | Paris
*contract[owner_country] | Country of the owner | string (alpha2 country code) | FR
*contract[owner_phone] | Phone of the owner | string | 01 73 03 02 02
*contract[owner_email] | Email of the owner | string | julien@viviani.fr
persist_user_profile | Updates the owner account with the given informations | presence | true/1

## Owner : Update contract as a company

> Response:

```json
{
  "data": {
    "id": "4004",
    "type": "contract"
  }
}
```

This endpoint updates the contract as a client company.

The user must be logged in while doing this request.

The client must choose between 2 ways of update :

  - With an existing company by filling the `*contract[owner_company_id]` parameter.

  OR

  - Without an existing company and by filling all the others mandatory parameters.

the `persist_company` parameter allows the owner to save this informations about his company.

### HTTP Request

`PUT /api/v1/owner_contracts/:id?context=company`

*: Mandatory

### Query Parameters

Parameter | Description | Type | Example
--------- | ----------- | ------- | -------
*contract[owner_company_name] | Name of the owner company | string | Le Collectionist
*contract[owner_company_siret] | SIRET of the owner company | string (14) | 01234567891234
*contract[owner_company_address] | Address of the owner | string | 126 Rue de Provence
*contract[owner_company_postal_code] | Postal code of the owner | string | 75008
*contract[owner_company_city] | City of the owner | string | Paris
*contract[owner_company_country] | Country of the owner | string (alpha2 country code) | FR
*contract[owner_company_phone] | Phone of the owner | string | 01 73 03 02 02
*contract[owner_company_representative_gender] | Gender of the representative owner | string (male/female/unknown) | female
*contract[owner_company_representative_firstname] | First name of the representative owner | Julien
*contract[owner_company_representative_lastname] | Last name of the representative owner | Viviani
*contract[owner_company_id] | Last name of the representative owner | Viviani
*contract[owner_company_bic] | Bank BIC of the owner company | string (8..11) | 12345678
*contract[owner_company_iban] | Bank IBAN of the owner company | string (27) | 123456789012345678901234567
*contract[owner_company_account_owner] | Name of the owner account company | string | Adrien Lerpscher
*contract[owner_company_email] | Email of the owner company | string | viviani@jlerp.fr
persist_company | Creates a related company to the owner | presence | true/1
