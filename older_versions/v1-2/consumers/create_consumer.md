# Create Consumer

~~~
POST https://api.smartpay.curexe.com/1-2/create_consumer
~~~

## Description

Creates a new consumer.  If any mandatory parameters are omitted it will be rejected.

## Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>custom_consumer_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td>Any alphanumeric ID you choose, up to a maximum of 32 characters</td>
  </tr>
  <tr>
    <td>first_name</td>
    <td>John</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>last_name</td>
    <td>Smith</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>email</td>
    <td>john.smith@demail.com</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>phone</td>
    <td>555-555-5555</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>street_address</td>
    <td>123 Street</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>city</td>
    <td>Toronto</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>province_state</td>
    <td>ON</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>country</td>
    <td>CA</td>
    <td>Yes</td>
    <td><a href="https://en.wikipedia.org/wiki/ISO_4217">ISO 3166-1 alpha-2</a></td>
  </tr>
  <tr>
    <td>postal_code</td>
    <td>M1M 1M1</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>is_dummy</td>
    <td>false</td>
    <td>No</td>
    <td><b>false</b> for live data, <b>true</b> for test 'dummy' data (defaults to false)</td>
  </tr>
</table>

## Result

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
</table>
