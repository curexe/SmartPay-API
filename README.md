<a href='https://smartpay.curexe.com'><img src="https://smartpay.curexe.com/resources/img/logo.png" width="200" ></a>

# Getting Started

The SmartPay API requires a registered <a href="https://smartpay.curexe.com">SmartPay Account</a> to use.

## Daily Rate Limiting

At this time the api is not rate limited but is monitored for excessive use. 

We recommended that data pulls are handled as batch requests only getting the latest data (limiting results using timestamps, e.g. <b>created_from</b>)..  keeping a local copy of required data on your own system.  Webhooks should be used to receive relevant updates so you can pull updated data as needed.  

Users who request at a greater then reasonable frequency will be disabled to prevent performance degredation for other users.

## Current Version

<a href="latest_version/v2-0">The current version of the API is v2.0</a>

## Version History

- [v2.0](latest_version/v2-0) **Current**
- [v1.2](older_versions/v1-2) Deprecated (2019-08-29)
- v1.1 Deprecated
- v1.0 Deprecated

## Errors Codes

[https://smartpay.curexe.com/api_error_codes](https://smartpay.curexe.com/api_error_codes)
