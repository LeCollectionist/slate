# Introduction

Welcome to the Le Collectionist API!

This API uses REST endpoints and returns JSON.

The response base keys are `data`, `meta` or `errors`.

The API is hosted on:

+ Staging: `https://staging-michelangelo.herokuapp.com`
+ Prod: `https://prod-michelangelo.herokuapp.com`

### Errors

> An example:

```json
{
  "errors": [
    "Couldn't find House with 'id'=678987"
  ]
}
```

Le Collectionist API show the errors with the `errors` base key.



### Pagination
<span class='badge badge-blue'>Paginated</span>

> All the paginated ressources comes with the meta base key:

```json
{
  "data": [{
    ...
  }],
  "meta": {
    "current_page": 1,
    "next_page": 2,
    "per_page": 25,
    "prev_page": null,
    "total_pages": 44,
    "total_count": 1081
  }
}
```

This label means the resouces below the `data` response base key is paginated.
It allows you to pass few more arguments to the endpoints.

Le Collectionist API show the pagination infos in the `meta` base key.

Parameter | Description | Example | Default
--------- | ----------- | ------- | -------
per | Split the resources by the indicated number | `per=10` | `25`
page | Choose the page of the paginated resources | `page=3` | `1`

Note: The `page` params can also have the value `all` (`page=all`).
In this case, it will respond with the entire collection.

### Localization
<span class='badge badge-green'>Localized</span>

This label means the resouces are translated on the requested locale.

The current available locales are:

+ en
+ fr
