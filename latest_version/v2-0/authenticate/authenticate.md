# Authenticate

~~~
GET https://api.smartpay.curexe.com/2-0/authenticate
~~~

## Description

The /authenticate endpoint is required to initiate an API session, and outputs a bearer token which is used for additional queries over the span of an hour. Once a token has expired a new one must be requested by using the /authenticate endpoint.

The endpoint /authenticate receives a <b>basic auth token</b> and issues a <b>bearer token</b> in response.  First you must generate an auth_token, and then you must include it in the Authentication HTTP header with the request sent to /authenticate.

The auth_token is a base64 encoded copy of your public iframe_key, and your secret api_key.  

PHP Example:
```
$auth_token = base64_encode("$iframe_key:$api_key");
```

## headers

<table>
  <tr>
    <td><b>Header</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>Authentication: Basic AUTH_TOKEN</td>
    <td>yes</td>
    <td>base64 encoded iframe_key:api_key (see above)</td>
  </tr>
</table>


## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td colspan="4">- none -</td>
  </tr>
</table>

## Resultset

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>access_token</td>
    <td>ABC123</td>
    <td></td>
  </tr>
  <tr>
    <td>expires_in</td>
    <td>3600</td>
    <td>in seconds</td>
  </tr>
  <tr>
    <td>token_type</td>
    <td>bearer</td>
    <td></td>
  </tr>
</table>
