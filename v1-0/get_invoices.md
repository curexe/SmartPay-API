# Get Invoices

~~~
https://smartpay.curexe.com/api/1.0/get_invoices
~~~

## Description

The /get_invoices endpoint allows retailers to obtain a list of invoices that are associated with their SmartPay account.

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>format</td>
    <td>json</td>
    <td>At this time only JSON format is available</td>
  </tr>
  <tr>
    <td>page</td>
    <td>1</td>
    <td>Defaults to 1 if not specified</td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>order_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>invoice_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>created_from</td>
    <td>2018-01-01 14:00:00</td>
    <td>Eastern time</td>
  </tr>
  <tr>
    <td>created_to</td>
    <td>2018-02-01 14:00:00</td>
    <td>Eastern time</td>
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
    <td>invoice_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>order_id</td>
    <td>aBc123</td>
    <td></td>
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
    <td>amount</td>
    <td>10.00</td>
    <td>CAD</td>
  </tr>
  <tr>
    <td>amount_discounted</td>
    <td>10.00</td>
    <td>CAD</td>
  </tr>
  <tr>
    <td>amount_remitted</td>
    <td>10.00</td>
    <td>CAD</td>
  </tr>
  <tr>
    <td>date_failed</td>
    <td>2018-01-01 12:00:00</td>
    <td>Eastern time</td>
  </tr>
  <tr>
    <td>date_paid</td>
    <td>2018-01-01 12:00:00</td>
    <td>Eastern time</td>
  </tr>
  <tr>
    <td>date_remitted</td>
    <td>2018-01-01 12:00:00</td>
    <td>Eastern time</td>
  </tr>
</table>
