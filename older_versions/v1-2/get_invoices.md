# Get Invoices

~~~
https://api.smartpay.curexe.com/1-2/get_invoices
~~~

## Description

The /get_invoices endpoint allows retailers to obtain a list of invoices that are associated with their SmartPay account.

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
    <td>payment_method</td>
    <td>d</td>
    <td>No</td>
    <td>"d" for Debit, "e" for eTransfer</td>
  </tr>
  <tr>
    <td>created_from</td>
    <td>2018-01-01 14:00:00</td>
    <td>No</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>created_to</td>
    <td>2018-02-01 14:00:00</td>
    <td>No</td>
    <td>GMT</td>
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
    <td>payment_method</td>
    <td>d</td>
    <td>"d" for Debit, "e" for eTransfer</td>
  </tr>
  <tr>
    <td>is_dummy</td>
    <td>true</td>
    <td>"true" if enabled, "false" otherwise</td>
  </tr>
  <tr>
    <td>is_enabled</td>
    <td>true</td>
    <td>"true" if enabled, "false" otherwise</td>
  </tr>
  <tr>
    <td>date_paid</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>date_failed</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>date_remitted</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
</table>
