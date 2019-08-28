<a href='https://smartpay.curexe.com'><img src="https://smartpay.curexe.com/resources/img/logo.png" width="200" ></a>

# Getting Started

The SmartPay API requires a registered <a href="https://smartpay.curexe.com">SmartPay Account</a> to use.

## Daily Rate Limiting

At this time the api is not rate limited but is monitored for excessive use. It is strongly recommended that webhooks are used to receive updates and to do data pulls as batch queries only getting the latest data (filtering by timestamps) and keeping a local copy on your own system.  This limits how frequently you need to query the API.  Users who request at greater than reasonable frequency will be disabled to prevent performance degredation for other users.

## Current Verison

<a href="latest_version/v2-0">The current version of the API is v2.0</a>

## Version History

- [v2.0](latest_version/v2-0) **Current**
- [v1.2](older_versions/v1-2) Deprecated (2019-08-29)
- v1.1 Deprecated
- v1.0 Deprecated

## Errors Codes

[https://smartpay.curexe.com/api_error_codes](https://smartpay.curexe.com/api_error_codes)
