# Modify Order

~~~
https://api.smartpay.curexe.com/1-2/modify_order
~~~

## Description

The /modify_order endpoint allows retailers to modify an existing order in SmartPay. Modifying an order will impact all future invoices, but not prior invoices.

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
    <td>order_id</td>
    <td>aBc123</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>custom_order_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>recurring_amount</td>
    <td>10.00</td>
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
    <td>order_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>custom_order_id</td>
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
    <td>single_amount</td>
    <td>10.00</td>
    <td>CAD</td>
  </tr>
  <tr>
    <td>single_amount_discounted</td>
    <td>10.00</td>
    <td>CAD</td>
  </tr>
  <tr>
    <td>recurring_amount</td>
    <td>10.00</td>
    <td>CAD</td>
  </tr>
  <tr>
    <td>recurring_amount_discounted</td>
    <td>10.00</td>
    <td>CAD</td>
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
    <td>number_of_invoices</td>
    <td>2</td>
    <td></td>
  </tr>
</table>
