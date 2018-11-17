# Modify Consumer

~~~
https://api.smartpay.curexe.com/1-0/modify_consumer
~~~

## Description

The /modify_consumer endpoint allows retailers to update consumer details.

> ***Warning**: This is a write query. Any data sent through this endpoint will be written to the SmartPay database in real-time. There is no undo. Please use with caution.*

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>format</td>
    <td>json</td>
    <td>No</td>
    <td>At this time only JSON format is available</td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>first_name</td>
    <td>John</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>last_name</td>
    <td>Smith</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>email</td>
    <td>name@domain.com</td>
    <td>No</td>
    <td>Must be valid. Must be unique.</td>
  </tr>
  <tr>
    <td>phone</td>
    <td>555-555-5555</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>street_address</td>
    <td>1 Main Street, #100</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>city</td>
    <td>Toronto</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>province_state</td>
    <td>ON</td>
    <td>No</td>
    <td>ISO code</td>
  </tr>
  <tr>
    <td>country</td>
    <td>CA</td>
    <td>No</td>
    <td>ISO code</td>
  </tr>
  <tr>
    <td>postal_code</td>
    <td>M1M 1M1</td>
    <td>No</td>
    <td></td>
  </tr>
</table>

## Resultset

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>name</td>
    <td>John Smith</td>
    <td></td>
  </tr>
  <tr>
    <td>email</td>
    <td>john@smith.com</td>
    <td></td>
  </tr>
  <tr>
    <td>phone</td>
    <td>555-555-5555</td>
    <td>Format will vary depending on user input</td>
  </tr>
  <tr>
    <td>street_address</td>
    <td>1 Main Street, #100</td>
    <td></td>
  </tr>
  <tr>
    <td>city</td>
    <td>Toronto</td>
    <td></td>
  </tr>
  <tr>
    <td>province_state</td>
    <td>ON</td>
    <td></td>
  </tr>
  <tr>
    <td>country</td>
    <td>CA</td>
    <td></td>
  </tr>
  <tr>
    <td>postal_code</td>
    <td>M1M 1M1</td>
    <td></td>
  </tr>
  <tr>
    <td>is_dummy</td>
    <td>false</td>
    <td>true or false</td>
  </tr>
</table>
