# Wishlists

## Get One Wishlist
<span class='badge badge-green'>Localized</span>

> Response:

```json
{
  "data": [
    {
      "id": "7",
      "type": "house",
      "attributes": {
        "bathrooms": 5,
        "bedrooms": 7,
        "capacity": 14,
        ...
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

This endpoint retrieves a wishlist's houses

### HTTP Request

`GET /fr/api/v1/wishlists/:token/houses`

## Link a house to a wishlist

> Response:

```json
{
  "data": {
    "id": "4",
    "type": "wishlist",
    "attributes": {
      "token": "c74e5890-18ed-4651-92d6-240b986cd767",
      "housesCount": 1
    }
  }
}
```

This endpoint links a house to a wishlist

### HTTP Request

`POST /api/v1/wishlists/:token/houses` with parameter `wishlist[house_id]`

The `wishlist[house_id]` parameter must be the house id.

### Query Parameters

Parameter | Description | Example
--------- | ----------- | -------
wishlist[house_id] | house id | 878

## Unlink a house from a Wishlist

> Response:

```json
{
  "data": {
    "id": "4",
    "type": "wishlist",
    "attributes": {
      "token": "c74e5890-18ed-4651-92d6-240b986cd767",
      "housesCount": 0
    }
  }
}
```

This endpoint unlink a house from the wishlist.

### HTTP Request

`DELETE /api/v1/wishlists/:token/houses/:house_id`
