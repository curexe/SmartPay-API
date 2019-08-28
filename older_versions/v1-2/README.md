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

"1-2" represents the version number, and "authenticate" represents the endpoint. All versions and endpoints will be documented here.

# Authentication Example

The API is queried with a key which is obtained from the Integrate page in the SmartPay web application:

```
{
  api_key: ABC123
}
```

The returned data is either the resultset (in this case a session token), or any errors:


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

* Tokens will expire within one hour of issue.

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