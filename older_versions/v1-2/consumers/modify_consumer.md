# Modify Consumer

~~~
POST https://api.smartpay.curexe.com/1-2/modify_consumer
~~~

## Description

Modifies a consumer.  This is a patch action and will only change the values submitted.

## Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>custom_consumer_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td>Configurable custom alphanumeric ID, up to a maximum of 32 characters</td>
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
    <td>john.smith@email.com</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>phone</td>
    <td>555-555-5555</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>street_address</td>
    <td>123 Street</td>
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
    <td></td>
  </tr>
  <tr>
    <td>country</td>
    <td>CA</td>
    <td>No</td>
    <td><a href="https://en.wikipedia.org/wiki/ISO_4217">ISO 3166-1 alpha-2</a></td>
  </tr>
  <tr>
    <td>postal_code</td>
    <td>M1M 1M1</td>
    <td>No</td>
    <td></td>
  </tr>
</table>

## Result

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
</table>
