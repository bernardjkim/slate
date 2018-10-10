# Users

## Create A User

*API endpoint*

`POST https://ptrade-api-staging.herokuapp.com/v1/users`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` | 

*REQUEST PARAMETERS (FORM)*

| Parameter | Description |
| --------- | ------- |
| ```first``` <br><span class="required">REQUIRED</span> | First name of new user. |
| ```last``` <br><span class="required">REQUIRED</span> | Last name of new user. |
| ```email``` <br><span class="required">REQUIRED</span> | Email of new user. |
| ```password``` <br><span class="required">REQUIRED</span> | Password of new user. |

### Response

A successful response will return the new users data.

> Example JSON response  

```json
{
    "id": 11,
    "first": "Allen",
    "last": "Iverson",
    "email": "alleniverson@gmail.com",
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `id` | User assigned id. |
| `first` | User's first name. |
| `last` | User's last name. |
| `email` | User's email address. |

## Get A User

*API endpoint*

`GET https://ptrade-api-staging.herokuapp.com/v1/users/{user_id}`

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
    "id": 11,
    "first": "Allen",
    "last": "Iverson",
    "email": "alleniverson@gmail.com",
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `id` | User assigned id. |
| `first` | User's first name. |
| `last` | User's last name. |
| `email` | User's email address. |