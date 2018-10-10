# Portfolios

## Get A User's Portfolio History

*API endpoint*

`GET https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}/charts`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` | 

*REQUSET PARAMETERS*

| Element | Detail |
| --- | --- |
| `user_id` <br><span class="required">REQUIRED</span> | The id of user to retrieve data for. |

### Response

A successful response contains a user's portfolio value history.

> Example JSON response  

```json
{
    "user_id": 11,
    "portfolio_history": [
        {
            "id": 1,
            "date": "2018-10-01 15:00:00",
            "value": 1000.00
        },
        {
            "id": 2,
            "date": "2018-10-02 15:00:00",
            "value": 1100.00
        },
        {
            "id": 3,
            "date": "2018-10-03 15:00:00",
            "value": 1050.00
        },
        ...
    ]
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `user_id` | User's id. |
| `portfolio_history` | Array of portfolio values. |
| `id` | Portfolio value id. |
| `date` | The date the value was recorded. |
| `value` | The portfolio value recorded in `USD`. |