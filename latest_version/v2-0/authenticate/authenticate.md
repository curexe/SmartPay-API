# Authenticate

~~~
GET https://api.smartpay.curexe.com/2-0/authenticate
~~~

## Description

The /authenticate endpoint is required to initiate an API session, and outputs a bearer token which is used for additional queries over the span of an hour. Once a token has expired a new one must be requested by using the /authenticate endpoint.

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>api_key</td>
    <td>ABC123</td>
    <td>Yes</td>
    <td></td>
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
    <td>token</td>
    <td>ABC123</td>
    <td></td>
  </tr>
  <tr>
    <td>expires_on</td>
    <td>2018-01-01 13:00:00</td>
    <td>UTC (Coordinated Universal Time)</td>
  </tr>
</table>
