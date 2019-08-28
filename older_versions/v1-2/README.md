# API v1.2

Please read this entire document before attempting to interact with the SmartPay API. If this is your first time connecting to an external API, you may wish to begin with the [quick start guide](quickstart/tutorial.md).

# Overview

See the [Overview Document](overview.md) for details about the endpoint structure of the 1.2 API

# Authentication & Tokens

The SmartPay API accepts queries using a two-phase approach: the authentication handshake and then the actual query itself. In either scenario, the system is queried with a version number, an endpoint (which defines the type of information requested) and a payload containing input parameters (sent by POST), and then returns a resultset.

The URL structure for querying the API is as follows:

```
https://api.smartpay.curexe.com/1-2/authenticate
```

* <b>1-2</b> represents the version number, and <b>authenticate</b> represents the endpoint.

# Authentication Example

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

# Query Phase

The token provided in the authentication phase is used as an input parameter to authenticate phase two: the actual data query. The result set may look something like this:

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