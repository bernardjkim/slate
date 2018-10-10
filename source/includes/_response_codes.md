# Response Codes

Our APIs use the following response codes:

*RESPONSE CODES*

Error Code | Meaning
---------- | -------
200 | <b>Success</b>
201 | <b>Resource created</b>
204 | <b>No content</b> - The server successfully processed the request and is not returning any content.
400 | <b>Bad Request</b> -- Input validation failed.
403 | <b>Forbidden</b> -- The Session Token is invalid, or it is not authorized to access the service.
404 | <b>Not Found</b> -- The requested resource could not be found but may be available in the future.
410 | <b>Gone</b> – The session has expired. A new session must be created.
429 | <b>Too Many Requests</b> – There have been too many requests in the last minute.
500 | <b>Server Error</b> – An internal server error has occurred which has been logged.
