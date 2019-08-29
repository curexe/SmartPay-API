# List Invoices

~~~
GET https://api.smartpay.curexe.com/2-0/invoices
~~~

## Description

Retreives a list of invoices.  Parameters can be used to filter the list. 

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
    <td>invoice_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>order_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>payment_method</td>
    <td>d</td>
    <td>No</td>
    <td><b>d</b> for Debit, <b>e</b> for eTransfer</td>
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
    <td>amount</td>
    <td>10.00</td>
    <td>CAD - amount invoiced</td>
  </tr>
  <tr>
    <td>amount_discounted</td>
    <td>10.00</td>
    <td>CAD - amount invoiced, after any discounts applied</td>
  </tr>
  <tr>
    <td>payment_method</td>
    <td>d</td>
    <td><b>d</b> for Debit, <b>e</b> for eTransfer</td>
  </tr>
  <tr>
    <td>is_dummy</td>
    <td>true</td>
    <td><b>false</b> for live data, <b>true</b> for test 'dummy' data</td>
  </tr>
  <tr>
    <td>is_enabled</td>
    <td>true</td>
    <td><b>true</b> if enabled, <b>false</b> otherwise</td>
  </tr>
  <tr>
    <td>date_paid</td>
    <td>2018-01-01 12:00:00</td>
    <td>UTC (Coordinated Universal Time)</td>
  </tr>
  <tr>
    <td>date_failed</td>
    <td>2018-01-01 12:00:00</td>
    <td>UTC (Coordinated Universal Time), null while there are no payment issues</td>
  </tr>
</table>
