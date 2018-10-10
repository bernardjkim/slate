# Transfers

## Create A New Transfer Order

*API endpoint*

`POST https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}/transfers`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` | 
| `Session-Token` <br><span class="required">REQUIRED</span> | Token required to authenticate order. |

*REQUSET PARAMETERS*

| Element | Detail |
| --- | --- |
| `user_id` <br><span class="required">REQUIRED</span> | The id of user to create order for. |

*REQUEST PARAMETERS (FORM)*

| Parameter | Description |
| --------- | ------- |
| ```balance``` <br><span class="required">REQUIRED</span> | The balance to be transfered in `USD`. Positive value for a `deposit`. Negative value for a `withdrawl`. |

### Response

A successful response contains no content.

## Get All Transfer Orders

*API endpoint*

`GET https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}/transfers`

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

A successful response contains a list of transfer orders made by the specefied user.

> Example JSON response  

```json
{
    "user_id": 11,
    "transfers":
    [
        {
            "id": 123,
            "date_start": "2018-10-09 02:14:47",
            "date_end": "2018-10-09 02:15:47",
            "status": "FULFILLED",
            "balance": 100.00,
        },
        {
            "id": 124,
            "date_start": "2018-10-09 02:14:47",
            "date_end": "2018-10-09 02:15:47",
            "status": "CANCELED",
            "balance": 1000.00,
        },
        ...
    ]
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `user_id` | The user's id. |
| `transfers` | Array of transfer orders. |
| `id` | The order id. |
| `date_start` | The date the order was create. |
| `date_end` | The date the order was completed. |
| `status` | The order's status `PENDING`, `CANCELED`, `FULFILLED`. |
| `balance` | The balance transfered in `USD`. Positive value indicates a `deposit`. Negative value indicates a `withdrawl`.|
