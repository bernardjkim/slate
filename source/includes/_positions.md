# Positions

## Get A User's Stock Positions

*API endpoint*

`GET https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}/position`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` | 

*REQUSET PARAMETERS*

| Element | Detail |
| --- | --- |
| `user_id` <br><span class="required">REQUIRED</span> | The id of user to retrieve data for. |

### Response

A successful response contains user data.

> Example JSON response  

```json
{
    "user_id": 11,
    "positions": [
        {
            "id": 1,
            "date": "2018-10-08 02:13:38",
            "shares": 20
        },
        {
            "id": 2,
            "date": "2018-10-09 02:13:38",
            "shares": 10
        },
        ...
    ]
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `user_id` | The user's id. |
| `id` | The stock id. |
| `date` | The date when the position was last updated. |
| `shares` | The current number of shares held. |