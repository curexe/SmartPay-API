# API v2.0

The 2.0 API is built as a series of endpoints (urls) that are built in a <a href="https://en.wikipedia.org/wiki/Representational_state_transfer">RESTful structure</a>.

- All timestamps are formatted as UTC (Coordinated Universal Time).
- All returned responses will be JSON (application/json).
- POST, PATCH and PUT requests must submit body data as either JSON (application/json) or x-www-form-urlencoded.
- GET requests may use url params to filter the data.
- /Authenticate issues a bearer token that must be sent with each request (good for up to 1 hour)

# How-To

If you are unfamilar how to query APIs our [How-To Guide](how-to.md) shows the basics demonstrated with a free tool called PostMan to help you get started.

# API Overview

See the [Overview Document](overview.md) for details about the endpoint structure of the 2.0 API

# Getting Started

## Authentication & Tokens

<i>Getting an api_key: after registering with SmartPay your api key is available in the <b>Integrate</b> section of the dashboard.</i>

The endpoint /authenticate receives a <b>basic auth token</b> and issues a <b>bearer token</b> in response.  First you must generate an auth_token, and then you must include it in the Authorization HTTP header with the request sent to /authenticate.

The auth_token is a base64 encoded copy of your public iframe_key, a colon, and and your secret api_key.

PHP Example:
```
$auth_token = base64_encode("$iframe_key:$api_key");
```

GET /2-0/authenticate

Headers:
```
Authorization: Basic AUTH_TOKEN
```

The returned data is either the result (in this case a bearer token), or any errors:

```
{
  "result": {
    "access_token": "xoqBMvdeG9vqs2AeYLsxLnsuzmtgpsab",
    "expires_in": 3600,
    "token_type": "bearer"
  }
}
```

```
{
  "errors": {
      "1001": "Invalid key",
  }
}
```

* Tokens will expire within one hour of issue

## Using Token Example

The token received from /authenticate is used to query all other endpoints for data.  This token is sent as a bearer token within the <b>Authorization</b> HTTP header.

GET /2-0/get_consumers?created_after=2019-08-22%2001:02:03

Headers:
```
Authorization: Bearer ACCESS_TOKEN
```

Result
```
{
  page: 1,
  total_pages: 3,
  result: [
    ...
  ]
}
```
