# Balances

## Get A User's Account Balance

*API endpoint*

`GET https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}/balance`

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
    "id": 1,
    "user_id": 11,
    "date": "2018-10-09 02:13:38",
    "balance": 1000.00
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `id` | Balance entry id. |
| `user_id` | The user's id. |
| `date` | The date when the balance was last updated. |
| `balance` | The current user's account balance in `USD`. |