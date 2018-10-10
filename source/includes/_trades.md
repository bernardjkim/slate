# Trades

## Create A New Trade Order

*API endpoint*

`POST https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}/trades`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` | 
| `Session-Token` <br><span class="required">REQUIRED</span> | Token required to authenticate order. |

*REQUSET PARAMETERS*

| Element | Detail |
| --- | --- |
| `user_id` <br><span class="required">REQUIRED</span> | The id of user create order for. |

*REQUEST PARAMETERS (FORM)*

| Parameter | Description |
| --------- | ------- |
| ```symbol``` <br><span class="required">REQUIRED</span> | The symbol for the stock to be traded. |
| ```shares``` <br><span class="required">REQUIRED</span> | The number of shares to be traded. Positive value indicates a `buy` order. Negative value indicates a `sell` order. |

### Response

A successful response contains no content.

## Get All Trade Orders

*API endpoint*

`GET https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}/trades`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` | 
| `Session-Token` <br><span class="required">REQUIRED</span> | Token required to authenticate data request. |

*REQUSET PARAMETERS*

| Element | Detail |
| --- | --- |
| `user_id` <br><span class="required">REQUIRED</span> | The id of user to retrieve data for. |

### Response

A successful response contains a list of trade orders made by the specefied user.

> Example JSON response  

```json
{
    "user_id": 11,
    "trades": [
        {
            "id": 123,
            "date_start": "2018-10-09 02:14:47",
            "date_end": "2018-10-09 02:15:47",
            "status": "FULFILLED",
            "stock_id": 13,
            "shares": 5,
        },
        {
            "id": 124,
            "date_start": "2018-10-09 02:14:47",
            "date_end": "2018-10-09 02:15:47",
            "status": "CANCELED",
            "stock_id": 13,
            "shares": -5,
        },
        ...
    ]
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `user_id` | The user's id. |
| `trades` | Array of trade orders. |
| `id` | The order id. |
| `date_start` | The date the order was create. |
| `date_end` | The date the order was completed. |
| `status` | The order's status `PENDING`, `CANCELED`, `FULFILLED`. |
| `stock_id` | The id of the stock traded. |
| `shares` | The number of shares traded. Positive value indicates a `buy` order. Negative value indicates a `sell` order. |
