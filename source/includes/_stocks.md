# Stocks

## Get List Of Available Stocks

*API endpoint*

`GET https://ptrade-api-staging.herokuapp.com/v1/stocks`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` | 

### Response

A successful response contains a list of stock info.

> Example JSON response  

```json
[
    {
        "id": 1,
        "symbol": "A",
        "name": "Agilent Technologies Inc.",
        "price_per_share": 69.41
    },
    {
        "id": 2,
        "symbol": "AA",
        "name": "Alcoa Corporation",
        "price_per_share": 37.64
    },
    {
        "id": 3,
        "symbol": "AAAU",
        "name": "Perth Mint Physical Gold",
        "price_per_share": 11.895
    },
    ...
]
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `id` | The stock id. |
| `symbol` | The stock's symbol. |
| `name` | The stock's company name. |
| `price_per_share` | The stocks price per share in `USD`. |