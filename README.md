<a href='https://smartpay.curexe.com'><img src="https://smartpay.curexe.com/resources/img/logo.png" width="200" ></a>

Please read this entire document before attempting to interact with the SmartPay API. If this is your first time connecting to an external API, you may wish to begin with the [quick start guide](quickstart/tutorial.md).

# How It Works

The SmartPay API accepts queries using a two-phase approach: the authentication handshake and then the actual query itself. In either scenario, the system is queried with a version number, an endpoint (which defines the type of information requested) and a payload containing input parameters (sent by POST), and then returns a resultset.

The URL structure for querying the API is as follows:

```
https://api.smartpay.curexe.com/1-2/authenticate
```

"1-2" represents the version number, and "authenticate" represents the endpoint. All versions and endpoints will be documented here.

# Authentication Phase

The API is queried with a key which is obtained from the Integrate page in the SmartPay web application:

```
{
  api_key: ABC123
}
```

The returned data is either the resultset (in this case a session token), or any errors:


```
{
  result: [
    token: DEF456,
    expires_on: "2018-01-01 12:00:00"
  ]

  errors: [
    "789": "Incorrect key",
  ],
}
```

* Note that this result set is solely illustrative; a token would never be provided if there were errors, only warnings.

Tokens will expire within one hour of issue.

# Query Phase

The token provided in the authentication phase is used as an input parameter to authenticate phase two: the actual data query. The result set may look something like this:


```
{
  page: 1,
  total_pages: 3,
  result: [
    ...
  ]
}
```


# Daily Rate Limiting

At this time, resultsets are not rate limited but are monitored for excessive use. It is strongly recommended that systems which connect with the API do so asynchronously wherever possible (i.e. not in user real-time). Users who request at greater than reasonable frequency will be disabled to prevent performance degredation for other users.

# Versions

- [v1.2](latest_version/v1-2/overview.md) **Current**
- v1.1 Deprecated
- v1.0 Deprecated

# Errors Codes

[https://smartpay.curexe.com/api_error_codes](https://smartpay.curexe.com/api_error_codes)
