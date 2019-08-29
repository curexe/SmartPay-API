# List Consumers

~~~
GET https://api.smartpay.curexe.com/2-0/consumers
~~~

## Description

Retreives a list of consumers.  Parameters can be used to filter the list. 

Will return up to 100 results at a time.  Use <b>page</b> to retreive the next results in the set.

## Headers

<table>
  <tr>
    <td><b>Header</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>Authentication: Bearer ACCESS_TOKEN</td>
    <td>yes</td>
    <td>the bearer token issued by <a href="..\authenticate\authenticate.md">authenticate</a></td>
  </tr>
</table>

## Query Params (URL Encoded)

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>page</td>
    <td>1</td>
    <td>No</td>
    <td>Defaults to 1 if not specified</td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>custom_consumer_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td>Configurable custom alphanumeric ID, up to a maximum of 32 characters</td>
  </tr>
  <tr>
    <td>order_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>invoice_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>name</td>
    <td>Joh</td>
    <td>No</td>
    <td>Will do partial matches</td>
  </tr>
  <tr>
    <td>email</td>
    <td>john.smith@email.com</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>created_from</td>
    <td>2018-01-01 14:00:00</td>
    <td>No</td>
    <td>UTC (Coordinated Universal Time)</td>
  </tr>
  <tr>
    <td>created_to</td>
    <td>2018-02-01 14:00:00</td>
    <td>No</td>
    <td>UTC (Coordinated Universal Time)</td>
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
  <tr>
    <td>custom_consumer_id</td>
    <td>aBc123</td>
    <td>Configurable custom alphanumeric ID, up to a maximum of 32 characters</td>
  </tr>
  <tr>
    <td>name</td>
    <td>John Smith</td>
    <td></td>
  </tr>
  <tr>
    <td>email</td>
    <td>john.smith@email.com</td>
    <td></td>
  </tr>
  <tr>
    <td>phone</td>
    <td>555-555-5555</td>
    <td>Format will vary depending on user input</td>
  </tr>
  <tr>
    <td>street_address</td>
    <td>123 Street</td>
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
    <td><b>false</b> for live data, <b>true</b> for test 'dummy' data</td>
  </tr>
  <tr>
    <td>number_of_orders</td>
    <td>3</td>
    <td></td>
  </tr>
  <tr>
    <td>amount_purchased</td>
    <td>150.00</td>
    <td></td>
  </tr>
</table>
