# Sessions

A session token is required for certain API endpoints. Create a new session by signing into a user account.

ptrade expects for the Session-Token to be included in API requests to the server in a header that looks like the following:

`Session-Token: token123`

## Create A New Session

### Request

*API endpoint*

`POST https://ptrade-api-staging.herokuapp.com/v1/sessions`

<!-- [![Run in Postman](https://run.pstmn.io/button.svg)]() -->

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` |

*REQUEST PARAMETERS (FORM)*

| Parameter | Description |
| --------- | ------- |
| ```email``` <br><span class="required">REQUIRED</span> | The user email. |
| ```password``` <br><span class="required">REQUIRED</span> | The user password. |

### Response

A successful response contains a Session-Token created for the requested user. 

> Example JSON response  

```json
{
  "Session-Token": "eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCJ9..." 
}
```

*RESPONSE PARAMETERS*

| Element | Detail |
| ------- | ------ |
| `Session-Token` | Session-Token for user authentication. |

## Delete A Session 

*API endpoint*

`DELETE https://ptrade-api-staging.herokuapp.com/v1/sessions`

*HEADER VALUES*

| Header | Value |
| --- | --- |
| `Content-Type` <br><span class="required">REQUIRED</span> | `application/x-www-form-urlencoded` |
| `Session-Token` <br><span class="required">REQUIRED</span> | The session token to be deleted. |

### Response

A successful response contains no content.