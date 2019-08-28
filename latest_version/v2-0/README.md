# API v2.0

The 2.0 API is built as a series of endpoints (urls) that are built in a <a href="https://en.wikipedia.org/wiki/Representational_state_transfer">RESTful structure</a>.

- All timestamps are formatted as UTC (Coordinated Universal Time).
- All returned responses will be JSON (application/json).
- POST, PATCH and PUT requests must submit body data as either JSON (application/json) or x-www-form-urlencoded.
- GET requests may use url params to filter the data.
- /Authenticate issues a bearer token that must be sent with each request (good for up to 1 hour)

# How-To

If you are unfamilar how to query APIs our [How-To Guide](how-to.md) shows the basics demonstraited with a free tool called PostMan to help you get started.

# API Overview

See the [Overview Document](overview.md) for details about the endpoint structure of the 2.0 API

# Getting Started

## Authentication & Tokens

The SmartPay API accepts queries using a two-phase approach: the authentication handshake and then the actual query itself. In either scenario, the system is queried with a version number, an endpoint (which defines the type of information requested) and a payload containing input parameters (sent by POST), and then returns a resultset.

The URL structure for querying the API is as follows:

```
https://api.smartpay.curexe.com/2-0/authenticate
```

* <b>2-0</b> represents the version number, and <b>authenticate</b> represents the endpoint.

## Authentication Example

The endpoint /authenticate is queried to received a bearer token.  You must generate an auth_token and include it in the Authentication HTTP header with this request.  This token is a base64 encoded copy of your public iframe_key, and your secret api_key.  

PHP Example:
```
$auth_token = base64_encode("$iframe_key:$api_key");
```

See further instructions on the <a href="authenticate\authenticate.md">authenticate page</a>.

<i>Getting an api_key: after registering with SmartPay your api key is available in the <b>Integrate</b> section of the dashboard.</i>

GET /2-0/authenticate

Headers:
```
Authentication: Basic AUTH_TOKEN
```

The returned data is either the result (in this case a token), or any errors:

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

The token received from /authenticate is used to query all other endpoints for data.  This token is sent as a bearer token within the <b>Authentication</b> HTTP header.

GET /2-0/get_consumers?created_after=2019-08-22%2001:02:03

Headers:
```
Authentication: Bearer ACCESS_TOKEN
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