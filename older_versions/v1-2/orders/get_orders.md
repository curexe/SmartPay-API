# Get Orders

~~~
https://api.smartpay.curexe.com/1-2/get_orders
~~~

## Description

Retreives a list of orders.  Will return up to 100 results at a time.  Parameters can be used to filter the list. Use <b>page</b> to retreive the next results in the set.

## Parameters

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
    <td>order_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>custom_order_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td>Configurable custom alphanumeric ID, up to a maximum of 32 characters</td>
  </tr>
  <tr>
    <td>consumer_id</td>
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
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>order_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>custom_order_id</td>
    <td>aBc123</td>
    <td>Configurable custom alphanumeric ID, up to a maximum of 32 characters</td>
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
    <td>number_of_invoices</td>
    <td>2</td>
    <td></td>
  </tr>
</table>
