# API v1.2

The 1.2 API is built as a series of endpoints (urls) that received POST requests and respond with data.  
- All body data should be submitted as either form-data, x-www-form-urlencoded, or JSON (application/json).
- All returned responses will be JSON (application/json).
- All timestamps are formatted as UTC (Coordinated Universal Time).

# How-To

If you are unfamilar how to query APIs our [Quickstart Guide](quickstart/tutorial.md) shows the basics demonstraited with a free tool called PostMan to help you get started.

# API Overview

See the [Overview Document](overview.md) for details about the endpoint structure of the 1.2 API

# Getting Started

## Authentication & Tokens

The SmartPay API accepts queries using a two-phase approach: the authentication handshake and then the actual query itself. In either scenario, the system is queried with a version number, an endpoint (which defines the type of information requested) and a payload containing input parameters (sent by POST), and then returns a resultset.

The URL structure for querying the API is as follows:

```
https://api.smartpay.curexe.com/1-2/authenticate
```

* <b>1-2</b> represents the version number, and <b>authenticate</b> represents the endpoint.

## Authentication Example

The endpoint /authenticate is queried with a api_key.  

<i>Getting an api_key: after registering with SmartPay your api key is available in the <b>Integrate</b> section of the dashboard.</i>

POST /1-2/authenticate
```
{
  api_key: ABC123
}
```

The returned data is either the result (in this case a token), or any errors:

```
{
  "result": {
    "token": "ABC123",
    "expires_on": "2018-01-01 12:00:00"
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

* Tokens will expire within one hour of issue and may be used to query all other endpoints.

## Using Token Example

The token received from /authenticate is used to query all other endpoints for data. 

POST /1-2/get_consumers
```
{
  "token": "ABC123"
}
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