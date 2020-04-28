# Errors

Standard HTTP error codes are used to signal success and errors:

Code | Meaning
---------- | -------
**200** | Request was successful and a representation is included in the body.
**204** | No Content: Request was successful. No body is returned.
**400** | Bad Request: There was an issue parsing your request. Check the JSON.
**422** | Unprocessable Entity: The request made an invalid state change or didn’t pass application-level validation. Check the errors returned in the body.